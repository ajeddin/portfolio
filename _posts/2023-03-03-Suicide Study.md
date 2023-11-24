---
title: Suicide Analysis
date: 2023-03-01 12:00:00 -500
categories: [projects, python, data]
tags: [devmountain, python, data] # TAG names should always be lowercase
# pin: true
---

Welcome to my Data project. It is a analysis on the suicide rates worldwide based on gender.

## Features

- Ability to clearly see the number of suicides worldwide
- Compare suicides based on gender and deduct reasoning
- Compare 2 datasets (suicides and U.S. Happiness) to better explain hypothesis
<iframe 
    align="center"
    width="850"
    height="500"
    src="https://www.youtube.com/embed/6AisX8I2yKs"
    frameborder="0"
    allow="autoplay; encrypted-media"
    allowfullscreen
>
</iframe>

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

<!-- PROJECT LOGO -->

  <p align="center">
    <br />
    <a href="https://github.com/ajeddin/specsCapstone"><strong>Open GitHub Repo »</strong></a>
    <br />
    <br />
    <a href="https://ajeddin-specscapstone-homepage-czg3s7.streamlit.app/">View Demo</a>
    ·
    <a href="https://github.com/ajeddin/specsCapstone/issues">Report Bug</a>
    ·
    <a href="https://github.com/ajeddin/specsCapstone/issues">Request Feature</a>
  </p>

### Built With

- ![Anaconda][anaconda]
- ![Pandas][pandas]
- ![Plotly][plotly]
- ![Jupyter Notebook][jupyter notebook]

<!-- ROADMAP -->

## Function used to plot correlation

```python
def corrfunc(x, y, **kwargs):
    def pvalue_stars(p):
        if 0.05 >= p > 0.01:
            return '*'
        elif 0.01 >= p > 0.001:
            return '**'
        elif p <= 0.001:
            return '***'
        else:
            return ''
    cmap = kwargs['cmap']
    norm = kwargs['norm']
    ax = plt.gca()
    ax.grid(False)
    r, p = pearsonr(x, y)
    facecolor = cmap(norm(r))
    ax.set_facecolor(facecolor)
    lightness = (max(facecolor[:3]) + min(facecolor[:3])) / 2
    ax.annotate(f"{r:.2f}{pvalue_stars(p)}", xy=(.5, .5), xycoords=ax,
                color='white' if lightness < 0.7 else 'black',
                size=18, ha='center', va='center')

g = sns.PairGrid(masterCat, height=1.5, diag_sharey=False)
g.map_lower(sns.scatterplot)
g.map_upper(corrfunc,
            cmap=plt.get_cmap('RdBu_r'),
            norm=plt.Normalize(vmin=-1, vmax=1))
g.add_legend()
plt.show()
```

## A graph used in the analysis

```python

suicides_gender_USA = px.line(test, x='year',y='percapita')
suicides_gender_USA.data[0].name="Male"
suicides_gender_USA['data'][0]['line']['color']='rgb(23, 54, 255)'
suicides_gender_USA.update_traces(showlegend=True)

suicides_gender_USA.add_scatter( x=testWomen['year'],y=testWomen['percapita'],name='Women')
suicides_gender_USA['data'][1]['line']['color']='rgb(237, 9, 9)'

```

<img src='/scatterUSA.png' alt="Suicides and GDP per Capita USA">

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[contributors-shield]: https://img.shields.io/github/contributors/ajeddin/specsCapstone.svg?style=for-the-badge
[contributors-url]: https://github.com/ajeddin/specsCapstone/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/ajeddin/specsCapstone.svg?style=for-the-badge
[forks-url]: https://github.com/ajeddin/specsCapstone/network/members
[stars-shield]: https://img.shields.io/github/stars/ajeddin/specsCapstone.svg?style=for-the-badge
[stars-url]: https://github.com/ajeddin/specsCapstone/stargazers
[issues-shield]: https://img.shields.io/github/issues/ajeddin/specsCapstone.svg?style=for-the-badge
[issues-url]: https://github.com/ajeddin/specsCapstone/issues
[license-shield]: https://img.shields.io/github/license/ajeddin/specsCapstone.svg?style=for-the-badge
[license-url]: https://github.com/ajeddin/specsCapstone/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/ajedev
[product-screenshot]: images/screenshot.png
[next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[next-url]: https://nextjs.org/
[react.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[react-url]: https://reactjs.org/
[vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[vue-url]: https://vuejs.org/
[angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[angular-url]: https://angular.io/
[svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[svelte-url]: https://svelte.dev/
[laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[laravel-url]: https://laravel.com
[bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[bootstrap-url]: https://getbootstrap.com
[jquery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[jquery-url]: https://jquery.com
[javascript]: https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E
[java]: https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=java&logoColor=white
[nodejs]: https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white
[postgres]: https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white
[css3]: https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white
[html5]: https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white
[pandas]: https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white
[plotly]: https://img.shields.io/badge/Plotly-%233F4F75.svg?style=for-the-badge&logo=plotly&logoColor=white
[matplotlib]: https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black
[anaconda]: https://img.shields.io/badge/Anaconda-%2344A833.svg?style=for-the-badge&logo=anaconda&logoColor=white
[jupyter notebook]: https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white
