---
layout: post
title: "Snake"
date: 2017-10-02
excerpt: "~Fruity~"
tags: [C++, assignment, university]
comments: true
published: true
---

## Snake

So the idea of snake as a game is that the player has control over the snake who, by moving around the gameboard, will eat apples (or some kind of fruit) in order to grow in length.
If the snake runs into itself a life is lost or in some cases the game ends and the aim is to see how long you can make the snake before the game ends. In some versions of the game the snake
can't touch the sides of the 'map' otherwise the game would end or a life would be lost, however in other versions the snake could disappear off one side and return on the same axis on the 
other side of the map. 
While the game is reletively simple to play the logic behind it is much less simple.


> An apple a day... ~

## The Logic

In order for the snake to move the computer needs to register an input, in my case this was via keyboard. The arrowkeys are a simple and convenient tool to allow the player to move something across
the screen with little to no trouble. Using an update function the game will then need to register each frame to allow the snake to continue moving in a single direction after the key press. For example 
once the left arrow is pressed the snake should continue to move in that direction even after the player has removed their hand from the key.

Once this is set up the game mechanics need to be implimented, a fruit would need to be spawned in a random unoccupied space within the map. In order to do this a random generator would likely need ot be used
to then give numbers to the x and y axis values for the fruit. This fruit would also need to interact with the snake, simple enough through an if statment specifying that if the snakes head reaches a 
fruit the player score increases and a new sprite of the snakes tail is spawned in position of the last piece. This allows for the snake to grow with little over complicating. 

A lives and score counter will be needed to allow the player to keep track of how many attempts they have left within one game and a score counter to keep the player updated with how well they are 
doing. Both of which would be simple enough using if statments to update an onscreen score and tally, scaling or declining as the game progresses, which would then be updated each frame. 

In terms of the map in order to allow the snake to continue from one side of the map to the other as they run out of space, the snake head sprite would simply need to have its x or y axis position
(depending on which axis of the map the snake has go off of) and reset it to 0. This would simply mean that the snake would continue within the endless confines of the given perameters.

> Seems relatively simple...


## Put into practice

Having all this in mind within the three weeks this project has been worked on so far, I've had nothing but trouble understanding the framework we were given to work with. After assigning key presses
to register when pressed and giving each key an assigned game action I'm finding it increasingly difficult to get the program to register the key press and cause the sprites to move. 
While this is the case the sprite itself is shown and can be edited and moved to any given starting point whithin the game window, it's simply that for whatever reason the key presses aren't 
allocating the new position for the sprite (changed within an if statment to add or subtract along the x and y axis) preventing it from moving..

>I'm sure I must have missed something...
