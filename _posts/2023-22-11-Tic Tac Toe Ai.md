---
title: Tic Tac Toe AI
date: 2023-11-22 12:00:00 -500
categories: [projects,c]
tags: [c,algorithms] # TAG names should always be lowercase
# pin: true
---

# Tic-Tac-Toe with Minimax Algorithm

## Overview

The project is a console-based implementation of the classic game Tic-Tac-Toe, with an option to play against an AI opponent that employs the Minimax algorithm. The game allows players to choose between a Player vs. Player (PvP) mode and a Player vs. AI mode. In PvP mode, two human players take turns to make their moves, and in Player vs. AI mode, the player competes against an AI opponent that uses the Minimax algorithm to make optimal decisions.

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

<!-- PROJECT LOGO -->

  <p align="center">
    <br />
    <a href="https://github.com/ajeddin/TicTacToeMinimaxC"><strong>Open GitHub Repo »</strong></a>
    <br />
    <br />
    <!-- <a href="http://23.22.42.11/">View Demo</a> -->
    <!-- · -->
    <a href="https://github.com/ajeddin/TicTacToeMinimaxC/issues">Report Bug</a>
    <!-- · -->
  </p>

### Built With

- ![c][c]

## Features

- **Game Modes:**
  - **PvP:** Two human players take turns making moves.
  - **Player vs. AI:** The player competes against an AI opponent using the Minimax algorithm.

- **Dynamic Board Display:**
  - The game board is dynamically displayed after each move, providing a clear visual representation of the current state.

- **Input Validation:**
  - Player inputs are validated to ensure they are within the valid range of 1-9, and the chosen location is not already occupied.

- **Win Detection:**
  - The game checks for a winning condition after each move and announces the winner or a tie.

- **AI Opponent:**
  - The AI opponent uses the Minimax algorithm to make intelligent moves, aiming to maximize its chances of winning or force a tie.

- **Play Again Option:**
  - After each game, the player is prompted to play again, enhancing the user experience.

## Minimax Algorithm

The Minimax algorithm is a decision-making algorithm used in two-player games to find the optimal move for a player, assuming that the opponent is also playing optimally. The algorithm evaluates possible future moves, assigns a score to each, and selects the move with the highest score for the maximizing player and the lowest score for the minimizing player.

## Code Snippet
A small snippet of the logic regarding writing to the DirectoryService which allows for persistant data even if app was closed

```c
int minimax(char board[3][3],int depth, bool isMaxingorMining){
    int result =   checkWin(board); //upon run of the recursive function minimax, 
    //if game reached a terminal state, result is returned.
    if (result !=-2){
        return result;
    }
    if (isMaxingorMining){ // minimax function in this project is trying to
    //maximize the score for the ai and minimize it for the human player. 
        int bestScore = INT_MIN;
 for (int row = 0;row<3;row++){
for (int col = 0;col<3;col++){
if (board[row][col]<59){

        char initial = board[row][col];
        board[row][col] = 'O';
        int score = minimax(board,depth+1,false);
        board[row][col] = initial;
        if (score > bestScore){
            bestScore=score;
        }

        }
        }} 
        return bestScore;
    }
    else //choosing the minimal score for the human. 
    {
 int bestScore = INT_MAX;
 for (int row = 0;row<3;row++){
        for (int col = 0;col<3;col++){
        if (board[row][col]<59){
        char initial = board[row][col];

        board[row][col] = 'X'; 
        int score = minimax(board,depth+1,true); 

        if (score < bestScore){ 
            bestScore=score;
        }

        }}} 
        return bestScore;
    }
}
```



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[contributors-shield]: https://img.shields.io/github/contributors/ajeddin/selfCheck.svg?style=for-the-badge
[contributors-url]: https://github.com/ajeddin/TicTacToeMinimaxC/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/ajeddin/selfCheck.svg?style=for-the-badge
[forks-url]: https://github.com/ajeddin/TicTacToeMinimaxC/network/members
[stars-shield]: https://img.shields.io/github/stars/ajeddin/selfCheck.svg?style=for-the-badge
[stars-url]: https://github.com/ajeddin/TicTacToeMinimaxC/stargazers
[issues-shield]: https://img.shields.io/github/issues/ajeddin/selfCheck.svg?style=for-the-badge
[issues-url]: https://github.com/ajeddin/TicTacToeMinimaxC/issues
[license-shield]: https://img.shields.io/github/license/ajeddin/selfCheck.svg?style=for-the-badge
[license-url]: https://github.com/ajeddin/TicTacToeMinimaxC/blob/master/LICENSE.txt
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
[c]: https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white
[Swift]: https://img.shields.io/badge/Swift-FA7343?style=for-the-badge&logo=swift&logoColor=white
[html5]: https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white
