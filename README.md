# n-queens
This is a project I completed as a student at [hackreactor](http://hackreactor.com). For this project I solved the classic n-queens problem with a pair.

## The problem in a nutshell
Given an n x n chessboard, how many different ways can you place n queens, such that none of them are attacking each other?

## Helpful Groundwork
This repo contains a Backbone app to visualize your algorithms. To make use of it, open BoardViewer.html. You'll be implementing the conflict detection functions in src/Board.js as stepping stones to your solution.

## Bare Minimum Requirements
Some of the helper functions in src/Board.js have been completed for you, and some have not. You should only need to edit the functions listed below.

Open src/Board.js and fix the incomplete helpers (look for the 'start here' section) such that the specs in spec/BoardSpec.js pass. To see if your specs are passing, open SpecRunnner.html and look at the 'Board' section. Doing so will help you understand the problem more thoroughly, and will make the visualizer show any conflicts on the board.

* hasRowConflictAt(): test if a specific row on this board contains a conflict
* hasAnyRowConflicts(): test if any rows on this board contain a conflict
* hasColConflictAt(): test if a specific column on this board contains a conflict
* hasAnyColConflicts(): test if any columns on this board contain a conflict
* hasMajorDiagonalConflictAt(): test if a specific major diagonal on this board contains a conflict
* hasAnyMajorDiagonalConflicts(): test if any major diagonals on this board contain a conflict
* hasMinorDiagonalConflictAt(): test if a specific minor diagonal on this board contains a conflict
* hasAnyMinorDiagonalConflicts(): test if any minor diagonals on this board contain a conflict

Fill in the functions in src/solvers.js. Fill them out so they accomplish the stated goals and pass the tests in spec/solversSpec.js

* findNRooksSolution(): returns a single solution to the n-rooks problem
* countNRooksSolutions(): returns a count of the total number of solutions to the n-rooks problem
* findNQueensSolution(): returns a single solution to the n-queens problem
* countNQueensSolutions(): returns a count of the total number of solutions to the n-queens problem

Identify the time complexity of each of your helper methods, as well as for each of your working solutions

## Helpful Info
Don't reinvent wheel where you don't have to. Use the Board constructor you build out in src/Board.js in your code. You can also access it within the Chrome console easily after opening BoardViewer.html

Create new board instances that have access to all the helper methods you write in src/Board.js
example: var board = new Board({n:5})
Rather than setting or getting object properties directly with plain JavaScript, Backbone provides the get and set methods. Play with the getters and setters that Backbone provides
example: board.get(3) will return the 3rd row of the instance board (assuming that instance exists)
Rows run horizontally, left to right

Columns run vertically, top to bottom
Major Diagonals run diagonally, top-left to bottom-right
Minor Diagonals run diagonally, top-right to bottom-left

In chess the rook piece moves and attacks horizontally (along rows) or vertically (along columns), through any number of unoccupied squares

In chess the queen piece moves and attacks horizontally (along rows), vertically (along columns), or diagonally (along major and minor diagonals), through any number of unoccupied squares
