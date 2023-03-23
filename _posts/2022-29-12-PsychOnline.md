---
title: PsychOnline
date: 2022-12-29 12:00:00 -500
categories: [projects, javascript]
tags: [foundations, devmountain, javascript, postgres, servers] # TAG names should always be lowercase
# pin: true
---

Welcome to my project, Psych Online. A website that analyzes the user’s expression, returns quotes and GIFs based on the emotion, and has a place to store your favorite quotes.

## Features

- Analyze User Expression using face-api.js
- Get 3 top gifs using GIPHY api based on emotion
- Get qoute based on emotion
- Ability to add/delete qoutes
- View all qoutes
<iframe 
    align="center"
    width="850"
    height="500"
    src="https://www.youtube.com/embed/ioWOTGysj0U"
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

- ![NodeJS][nodejs]
- ![JavaScript][javascript]
- ![HTML][html5]
- ![CSS][css3]

<!-- ROADMAP -->

## Some of the logic in the project

```javascript
function ifFloat(emotions) {
  newEmotionArr = [];
  for (i = 0; i < emotions.length; i++) {
    let numStr = String(emotions[i]);
    if (numStr.indexOf("e") === -1) {
      newEmotionArr.push(emotions[i]);
    }
  }
  return newEmotionArr;
}
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
