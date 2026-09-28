---
title: "Deep Q-learning for Sokoban Game"
excerpt: "<img src='/images/sokoban.gif'>"
permalink: /projects/dqn_for_sokoban_game
collection: projects
---

[Codes](https://github.com/akarimoon/dqn-for-sokoban)

## What is "Sokoban"?
Sokoban is a game where the player pushes the crates around the warehouse, trying to get them to the goal, "their storage locations".

## What did I do?
I used deep Q-learning using keras to train the agent to navigate itself and push the crates in the correct direction. I used [pyxel](https://github.com/kitao/pyxel) for visualization.

<img src='/images/sokoban.gif'>

## Model
The NN architecture consists of
* 3 Conv layers + ReLU
* 2 Linear layers + ReLU
* log cosh loss function

I used Adam for the optimizer.
