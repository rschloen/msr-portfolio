---
layout: post
title:  "Baxter Plays Checkers"
featured-img: baxter_checkers
date:   2019-12-28 14:46:01 -0600
categories: jekyll update
---

This project was completed as the final project for ME 495: Embedded Systems in Robotics. Given the theme of recreational robots, my group chose to teach Rethink's Baxter robot how to play checkers. We created a ROS package to control the Baxter robot and wrote nodes for the major components of the project: computer vision, game logic and artificial intelligence, manipulation, and a state machine.


# Computer vision
Using the camera at the end of one of the Baxter robot's arms, our group used computer vision to identify the color and position of each checkers piece on the game board at the beginning of Baxter's turn.


# Game logic and AI
Using the information about the game board captured by the computer vision, Baxter's potential moves or the winner, if the game was over, could be determined. Baxter's move was selected using the Minimax algorithm with alpha beta pruning optimization.


# Manipulation
Once Baxter's move was selected, MoveIt!, a motion planning framework used in ROS, was used to plan and execute the movements to pick up the checkers pieces and place them in the correct square on the game board or discard pieces that had been jumped.


# State Machine
Our group used a state machine to integrate the different components of our package and easily control Baxter's commands throughout the course of a full game of checkers.



The package we created allows you to play a full, competitive game of checkers against Baxter as demonstrated in this video:
<iframe width="560" height="315" src="https://www.youtube.com/embed/6ZOXy3TKYeM" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"> </iframe>

To see the full details and documentation pertaining to this project, please visit this [Github repository](https://github.com/rschloen/final-project-checkers).

The group members involved in this project where: Maurice Rahme, Jordan Zeeb, and Taoran Zhang
