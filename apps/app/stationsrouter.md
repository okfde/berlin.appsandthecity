---
layout: app
category: app
slug: stationsrouter
title: Station Router
image:
description: A* routing to find your way around a station

---

The problem is with many interchange stations, where to get in on a train and get out and how to find
your way to the connecting train as fast as possible. This looks like a rather tricky problem.

This solution represents stations as graphs with uniform stretches being edges and change points
(elevators, stairs, road crossings) represented by nodes. Once a station has been represented as a 
correct graph, routing from one part of it to another is trivial.

Here is a rough proof of concept of A* routing for a graph model of a Yorkcstraße to be able to find your way 
from one part of the station to the other: https://gist.github.com/4172489

Determining which part of an edge an arriving train falls on should not be too difficult.

To be done:

* Better A* representation
* Special graph weights for road crossing, stairs, escalators and elevators
* See if using a cartesian grid search (instead of a graph search) using the GPS coordinates is easier and yields more accuracy
* Javascript port for web demo

