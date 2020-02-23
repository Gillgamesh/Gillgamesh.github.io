---
layout: project
date: 2020-02-03
title: Pathfinder
---

## Pathfinder

### Links
* [Source](https://gitlab.com/Gillgamesh/cse-160-final)

### Description

A JavaFX-based visualizer for pathfinding algorithms on a 2D grid. Weights can be specified per grid square, and the cost to travel between 2 adjacent grids is the average of their weights. Includes a map editor, allows for map files to be saved for later use, and includes a simple-to-use interface for including your own path-finding algorithms (still working on being able to import it into projects easily). Great for visualizing how specific pathfinding algorithms might be
more efficient than others (for example, A\* with a distance heuristic will open the opposite direction less frequently than without a distance heuristic).

The map editor allows you to assign custom travel weights to each grid block/pixel,in addition to walls and the start/end point. After choosing your algorithm from one of the default two, the simulation opens up where you can pause, slow down, fast forward etc. A full list of features and tech specs can be found in the [SRS](https://gitlab.com/Gillgamesh/cse-160-final/blob/master/Pathfinder-SRS.pdf).

For example, heres a visualization of the pathfinding without a distance heuristic--more expansion is performed on the top left corner:

![Pathfinder Dijkstra](/assets/img/pathfinder-dijkstra.gif)

Compared to a weak distance heuristic that is still admissable, which does a slightly better job of not exploring corners that increase your heuristic cost. Keep in mind, that although these examples are using A\*, in reality any shortest-path or path-finding algorithm can be implemented and visualized (and I'm planning on implementing this as a library that can be used on any WeightedGraph<> interface as defined in the source).
Although there are slight differences in the final path, both had the same total cost.

![A\* Distance](/assets/img/pathfinder-astar.gif)
