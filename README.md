# CS50 Final Project, Portal Checkers

**_Portal Checkers_** is a puzzle game developed in Lua, using as inspiration the [Board Game Ricochete Robots by Alex Randolph](https://en.wikipedia.org/wiki/Ricochet_Robot). Although the game has similar mechanics, the board and the playstyle has major differences.

## The Pieces and the Board

In Portal Checkers, similary to the classic version of Ricochete Robots, you have 4 differents pieces, in this game they are called **_Blocks_**, and their colors are:
- Yellow(N1)
- Red(N2)
- Green(N3)
- Blue(N4)

The _Blocks_ are placed in a 8x8 **_Board_**, and if we divided the board in four, their initial position can be at their color zones:

![Imgur](https://i.imgur.com/qE0BHge.png)

The **_Walls_** has a chance to appear in the purple zone, while the brown zones near the center will always spawn:

![Imgur](https://i.imgur.com/lGzh0qa.png)

The last piece is the **_Portal_**. Only one portal will spawn, and their position will be in a position depending their color:

![Imgur](https://i.imgur.com/ZHNREVI.png)

In this version, the Blocks, the Walls and the Portal positions are choosed aleatory by the game, each time it loads a new Board.

## Gamemode and Mechanics

Each time you start a game, it's going to trigger a 60 seconds countdown. In that time your objective is to move as many as possible Blocks to their respective Portal color. Past the 60 seconds, the game will check if you beat your Highscore, and if did, save this value.

To move the block tough, you have to respect the following mechanic:
> Blocks can only move in straight lines, and will stop only if collides with a wall or another block.

## Interface

First we will explore the interface when you start the game:

![Imgur](https://i.imgur.com/sJ48P3K.png)
In the right side, shows the command to **__Start a New Game(Enter)__**, the **__Help(H)__** that opens a quick guide to play the game and **__Highscore__** that shows your highscore. Note that the Highscore will be saved even if you close the game, so at the next time you start the game, will show your all time highscore.

Now when you start the game:

![Imgur](https://i.imgur.com/TIkRBVY.png)
The right side now will show how many **__Time__** do you have remaining and how many **__Moves__** you have done in this playthrough.

When the countdowns reach 0, will be displayed the final game interface:
![Imgur](https://i.imgur.com/jATIH7i.png)
In this screen will be shown your current Highscore and how many level you complete in this run.

## Controls

For the controls we have a few when you start the game:

* '1': select the yellow Block
* '2': select the red Block
* '3': select the green Block
* '4': select the blue Block
* Tab: select the next Block(order: 1, 2, 3, 4, 1, 2, 3, 4, 1...)
* Arrow keys: move the Block to the arrow's sense
* 'A': skip the map*

*Note: When you skip a map, you're total maps completed is **__Reduced by One__**.

#