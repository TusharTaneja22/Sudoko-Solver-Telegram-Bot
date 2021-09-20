# Sudoku Solver - Telegram Bot

<img src="https://ai.github.io/size-limit/logo.svg" align="right"
     alt="Size Limit logo by Anton Lovchikov" width="120" height="178">

This is a telegram bot which solves the Sudoku problem. All we need to do is to capture the image of Sudoku and send it to this bot. The bot will respond in the form of image by overlaying the solution on the input image.

## Technologies Used

* [Telegram bot API](https://core.telegram.org/bots/api)
* [OpenCV](https://opencv.org)
* [Tensorflow](https://www.tensorflow.org)
* CNN Model

## How It Works

1. After receiving the image of sudoku from the user, the Sudoku is located in the
   image by finding the biggest square with the help of contuors and crop that part from the image. 
2. Next task is to find the atomic box in the sudoku. Same contour logic is used again to get all the boxes containing digits and empty boxes. 
3. Then the digit in each non-empty cell/box of the sudoku is predicted by using LeNet-5 model trained to predict the digits. 
4. Finally sudoku is converted to a 2-D array form and algorithm solves the sudoku problem.
5. The digits required to fill in the empty boxes are written on the image and is sent to the user.

## Screenshots

Sudoku Solver: Telegram Bot
<p align="center">
  <img src="./bot.jpg" alt="bot" width="250">
</p>


Uploading Sudoku Problem Image (Input)
<p align="center">
  <img src="./Demo1.jpg" alt="Demo1" width="250">
</p>


Solution Image (Output)
<p align="center">
  <img src="./Demo2.jpg" alt="Demo2" width="250">
</p>
