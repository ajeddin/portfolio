---
title: Self Check
date: 2023-06-10 12:00:00 -500
categories: [projects, swift]
tags: [apple developer academy, swift] # TAG names should always be lowercase
# pin: true
---

Self Check is a iOS app that focuses on self care and mindfulness. The app has a intuitive and straightforward design and includes a progress bar as you finish you daily tasks

## Features

- Mindful breathing feature
- Self Care checklist
- Progress Bar that tracks checked tasks
- Persistant 


[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

<!-- PROJECT LOGO -->

  <p align="center">
    <br />
    <a href="https://github.com/ajeddin/selfCheck"><strong>Open GitHub Repo »</strong></a>
    <br />
    <br />
    <a href="">Coming to TestFlight Soon</a>
    ·
    <a href="https://github.com/ajeddin/selfCheck/issues">Report Bug</a>
    ·
    <a href="https://github.com/ajeddin/selfCheck/issues">Request Feature</a>
  </p>

### Built With

- ![CSS][swift]

<!-- ROADMAP -->
### App Photos
- <img  width="155" height="120" src="/selfcheckImages/hp.png">,<img  width="155" height="120" src="/selfcheckImages/hp2.png">,<img  width="155" height="120" src="/selfcheckImages/breath.png">, <img  width="155" height="120" src="/selfcheckImages/addTask.png">





## Code Snippet
A small snippet of the logic regarding writing to the DirectoryService which allows for persistant data even if app was closed

```swift
  func readTasks(model: [dailyTask])-> [dailyTask]{
        do {
            return try DirectoryService.readModelFromDisk()


        } catch {
            print(error.localizedDescription)
            return []
        }
    }
    func removeTask(at index: Int) {
        tasks.remove(at: index)
        do {
            try DirectoryService.writeModelToDisk(tasks)

        } catch {
            print(error.localizedDescription)
        }
    }

    func addTask(){
        if (!taskInput.isEmpty){
            tasks.append(dailyTask(taskGut: taskInput, isCompleted: false))
            taskInput=""

            do {
                try DirectoryService.writeModelToDisk(tasks)

            } catch {
                print(error.localizedDescription)
            }}

    }
```

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[contributors-shield]: https://img.shields.io/github/contributors/ajeddin/selfCheck.svg?style=for-the-badge
[contributors-url]: https://github.com/ajeddin/selfCheck/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/ajeddin/selfCheck.svg?style=for-the-badge
[forks-url]: https://github.com/ajeddin/selfCheck/network/members
[stars-shield]: https://img.shields.io/github/stars/ajeddin/selfCheck.svg?style=for-the-badge
[stars-url]: https://github.com/ajeddin/selfCheck/stargazers
[issues-shield]: https://img.shields.io/github/issues/ajeddin/selfCheck.svg?style=for-the-badge
[issues-url]: https://github.com/ajeddin/selfCheck/issues
[license-shield]: https://img.shields.io/github/license/ajeddin/selfCheck.svg?style=for-the-badge
[license-url]: https://github.com/ajeddin/selfCheck/blob/master/LICENSE.txt
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
[Swift]: https://img.shields.io/badge/Swift-FA7343?style=for-the-badge&logo=swift&logoColor=white
[html5]: https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white
