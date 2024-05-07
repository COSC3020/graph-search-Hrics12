[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/M24O3lId)
# Search in Graphs

Recall the pseudocode for Depth-First Search:

Given a graph, a start node, and a node we're looking for:
- starting at the start node, while unvisited nodes remain
    - if current vertex $v$ is the node we're looking for, return it
    - mark $v$ as visited
    - for each edge $(v,w)$
        - recursively process $w$ unless marked visited

Implement the algorithm. You can choose any of the data structures we covered
(adjacency matrix or adjacency list) for the implementation. Your function
should return the list of nodes on the path from the start to the target (not
the list of nodes that you looked at during the search). If start and target are
the same, it should return a list with only that node. If there is no path from
the start to the target, it should return an empty list. Start with the template
I provided in `code.js` and test your new function.

I have not provided any test code, but you can base yours on test code from
other exercises. Your tests must check the correctness of the result of running
the function and run automatically when you commit through a GitHub action.


## Runtime Analysis

What is the worst-case big $\Theta$ complexity of your implementation? Add your
answer, including your reasoning, to this markdown file.


the worst case is going to be $\Theta(V+E)$ V= vertices and E= edges. This algorithm has to visit each node in the graph because the node only get added to the stack if it hasn't been visted. So you get $\theta(V)$ for visiting each node.
the algorithm also lookks at each adjacent nodes so each edge is explored twice getting $\Theta(E)$ so the worst case would be $\Theta(V+E)$

I used chatGPT to help me make the test and workflow for the action. I'm not that familiar with Github to know how to do that
https://aykutsarac.medium.com/graph-search-in-js-depth-first-search-3-4de691159280
## Bonus

Implement and analyze breadth-first search.
