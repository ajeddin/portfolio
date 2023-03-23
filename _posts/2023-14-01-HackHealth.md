---
title: HackHealth
date: 2023-01-21 12:00:00 -500
categories: [projects, javascript]
tags: [servers, hackathon, javascript, postgres]
# pin: true
---

Welcome to my project, HackHealth. A website that tracks patients prescriptions, allows them to add/delete prescriptions, make appointments with doctors at selected time slots.

## Features

- Sign up/login page for patients
- Prescription Management (adds/deletes)
- Tracks frequency of medication and dosage
- View available doctor with their photo/specialty/working hours
- Ability to create appointments with the selected doctors
<iframe
    width="850"
    height="500"
    src="https://www.youtube.com/embed/d-vUMf9xHKc"
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
    <a href="https://github.com/ChiemekaAnunkor/hackhealth"><strong>Open GitHub Repo »</strong></a>
    <br />
    <br />
    <!-- <a href="http://23.22.42.11/">View Demo</a> -->
    <!-- · -->
    <a href="https://github.com/ChiemekaAnunkor/hackhealth/issues">Report Bug</a>
    <!-- · -->
    <a href="https://github.com/ChiemekaAnunkor/hackhealth/issues">Request Feature</a>
  </p>

### Built With

- ![NodeJS][nodejs]
- ![JavaScript][javascript]
- ![HTML][html5]
- ![CSS][css3]

## Accomplishments that I am proud of

- Interactive time slots for appointments
- Excellent front-end design
- Ability for patient to input their current medication/prescription and easily manage them

<!-- ROADMAP -->

## Some of the logic in the project

```javascript
const findDoctor = (e) => {
  e.preventDefault();
  let doctor_id = parseInt(doctor.value);
  axios
    .post("http://localhost:4000/getDoctorsAvaiblity", {
      doctor_id: doctor_id,
      date: date.value,
    })
    .then(({ data: doctorsAvaiblity }) => {
      let doctorTime = avaiblity.map((t, index) => {
        if (doctorsAvaiblity.length > 0) {
          for (let i = 0; i < doctorsAvaiblity.length; i++) {
            if (doctorsAvaiblity[i].time != t) {
              docstime.push(t);
              return `<option value="${usTime[index]}">${usTime[index]}</option>`;
            }
          }
        } else {
          docstime.push(t);
          return `<option value="${usTime[index]}">${usTime[index]}</option>`;
        }
      });
      timeContainer.innerHTML = doctorTime;
    });
};
```

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[contributors-shield]: https://img.shields.io/github/contributors/ChiemekaAnunkor/hackhealth.svg?style=for-the-badge
[contributors-url]: https://github.com/ChiemekaAnunkor/hackhealth/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/ChiemekaAnunkor/hackhealth.svg?style=for-the-badge
[forks-url]: https://github.com/ChiemekaAnunkor/hackhealth/network/members
[stars-shield]: https://img.shields.io/github/stars/ChiemekaAnunkor/hackhealth.svg?style=for-the-badge
[stars-url]: https://github.com/ChiemekaAnunkor/hackhealth/stargazers
[issues-shield]: https://img.shields.io/github/issues/ChiemekaAnunkor/hackhealth.svg?style=for-the-badge
[issues-url]: https://github.com/ChiemekaAnunkor/hackhealth/issues
[license-shield]: https://img.shields.io/github/license/ChiemekaAnunkor/hackhealth.svg?style=for-the-badge
[license-url]: https://github.com/ChiemekaAnunkor/hackhealth/blob/master/LICENSE.txt
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
