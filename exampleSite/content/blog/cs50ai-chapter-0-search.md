+++
author = ["Timothy Chung"]
categories = ["Artificial Intelligence", "Computer Science"]
date = 2020-07-12T16:00:00Z
description = ""
image = "/images/9a83a37b-d420-4bde-88ac-df1c4d1e7161.jpeg"
tags = ["Nodes", "Python"]
title = "CS50AI Chapter 0: Search"

+++
Search Problems are a core part of AI. Whenever you intend to compute something, there can be many outcomes, but only a select few are the ones you are looking for. Real life examples include Google Maps trying to find the shortest path between two places, solving puzzles like tic-tac-toe, etc.

Before we go on, here are some definitions:

**Agent:** An entity that perceives its environment and acts upon it

**State:** A configuration of the agent and its environment.

**Actions:** Choices that can be made in a state

**Transition Model:** The result of performing a certain, possible action in a state.

**State Space:** The set of all the states reachable from its initial state by any sequence of actions.

**Goal Test:** Determine if the given state is a goal state, or the state that we are looking for.

**Path Cost:** Numerical cost of a given path.

**Node:** A data structure that keeps track of a:

* a state
* a parent (node that generated this node)
* an action (applied to parent to reach this node)
* a path cost (from initial state to node)

### The Algorithm

You can visualise nodes as being interconnected together in a decentralised net. The idea is, you want to start with the initial node or initial state, and find the shortest path to the goal state. Then pick adjacent nodes that aren’t explored and see if they’re the one that is the goal state.

This is how the algorithm works, in more detail:

1. Start with a frontier that contains the initial state.
2. Start with an empty explored set.
3. Repeat:
   1. If the frontier is empty, there is no solution
   2. Remove a node from the frontier.
   3. If the node is the goal state, return the solution.
   4. Add the node to the explored set.
   5. Expand the node, adding more nodes to the frontier if they are not in the explored set.