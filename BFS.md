Breadth First Search (BFS) is an algorithm for traversing a tree or graph data structure. It starts at the root node and explores the neighbor nodes first, before moving on to the next level neighbors.

Here is a simple example of a BFS algorithm for traversing a tree using Python:

```python
from collections import deque

def bfs(root):
  queue = deque([root]) # initialize the queue with the root node

  while queue:
    current = queue.popleft() # get the next node from the queue
    print(current.value) # visit the current node

    for child in current.children:
      queue.append(child) # add the child nodes to the queue

# Example tree:
#      A
#     / \
#    B   C
#   / \   \
#  D   E   F

class Node:
  def __init__(self, value, children=[]):
    self.value = value
    self.children = children

tree = Node("A", [
  Node("B", [
    Node("D"),
    Node("E")
  ]),
  Node("C", [
    Node("F")
  ])
])

bfs(tree)
# Output: A B C D E F
```

In this example, the bfs function visits the root node (A) and its children (B and C) in turn, and then visits the children of each child node (D, E, and F). The output shows the order in which the nodes were visited.

BFS tree traversal
![BFS Traversal Tree](https://upload.wikimedia.org/wikipedia/commons/5/5d/Breadth-First-Search-Algorithm.gif)

BFS is often used for tasks such as finding the shortest path in a graph, or for exploring all nodes reachable from a given starting point. It has a time complexity of O(n) for a tree with n nodes.