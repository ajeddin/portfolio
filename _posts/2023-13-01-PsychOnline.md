---
title: Psych Online
date: 2022-12-29 12:00:00 -500
categories: [projects, javascript]
tags: [foundations, devmountain, javascript, postgres,servers] # TAG names should always be lowercase
pin: true
---

Welcome to my project, Psych Online. A website that analyzes the user's expression, returns quotes and GIFs based on the emotion, and a place to store your favorite quotes.

<iframe 
    align="center"
    width="850"
    height="500"
    src="https://awevideo.s3.amazonaws.com/video-13761407-168f6f28.mp4?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJSCJQ2NM3XLFPVKA%2F20230123%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20230123T215443Z&X-Amz-Expires=86400&X-Amz-SignedHeaders=host&X-Amz-Signature=d2158158df2b1fffd88374b5d7b54cf0439fdf9a05fee3201297da64ae2767ff"
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
    <a href="https://github.com/ajeddin/foundations_capstone"><strong>Open GitHub Repo »</strong></a>
    <br />
    <br />
    <a href="https://psychonline.herokuapp.com/">View Demo</a>
    ·
    <a href="https://github.com/ajeddin/foundations_capstone/issues">Report Bug</a>
    ·
    <a href="https://github.com/ajeddin/foundations_capstone/issues">Request Feature</a>
  </p>

### Built With

* ![NodeJS][NodeJS]
* ![JavaScript][JavaScript]
* ![HTML][HTML5]
* ![CSS][css3]




<!-- ROADMAP -->
## Features

- Analyze User Expression using face-api.js
- Get 3 top gifs using GIPHY api based on emotion
- Get qoute based on emotion
- Ability to add/delete qoutes
- View all qoutes
## Some of the logic in the project
```javascript
function ifFloat(emotions) {
    newEmotionArr = []
    for (i=0;i<emotions.length;i++){
        let numStr = String(emotions[i]);
        if (numStr.indexOf('e') === -1) {
            newEmotionArr.push(emotions[i])}}
            return newEmotionArr}
```



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/ajeddin/foundations_capstone.svg?style=for-the-badge
[contributors-url]: https://github.com/ajeddin/foundations_capstone/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/ajeddin/foundations_capstone.svg?style=for-the-badge
[forks-url]: https://github.com/ajeddin/foundations_capstone/network/members
[stars-shield]: https://img.shields.io/github/stars/ajeddin/foundations_capstone.svg?style=for-the-badge
[stars-url]: https://github.com/ajeddin/foundations_capstone/stargazers
[issues-shield]: https://img.shields.io/github/issues/ajeddin/foundations_capstone.svg?style=for-the-badge
[issues-url]: https://github.com/ajeddin/foundations_capstone/issues
[license-shield]: https://img.shields.io/github/license/ajeddin/foundations_capstone.svg?style=for-the-badge
[license-url]: https://github.com/ajeddin/foundations_capstone/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/ajedev
[product-screenshot]: images/screenshot.png
[Next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[Next-url]: https://nextjs.org/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com 
[JavaScript]: https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E
[Java]:https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=java&logoColor=white
[NodeJS]:https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white
[Postgres]:https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white
[CSS3]:https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white
[HTML5]:https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white