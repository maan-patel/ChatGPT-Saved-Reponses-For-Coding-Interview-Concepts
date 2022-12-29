Depth First Search (DFS) is an algorithm for traversing a tree or graph data structure. It starts at the root node and explores as far as possible along each branch before backtracking.

Here is a simple example of a DFS algorithm for traversing a tree using Python:
```python
def dfs(root):
  print(root.value) # visit the root node

  for child in root.children:
    dfs(child) # visit each child node recursively

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

dfs(tree)

# Output: A B D E C F
```


In this example, the ```dfs``` function visits the root node (```A```) and its children (```B``` and ```C```) in turn, and then recursively visits the children of each child node (```D```, ```E```, and ```F```). The output shows the order in which the nodes were visited.

![DFS Traversal Tree](https://upload.wikimedia.org/wikipedia/commons/7/7f/Depth-First-Search.gif)

DFS is often used for tasks such as searching for a specific node in a tree or graph, finding connected components, and topological sorting. It has a time complexity of O(n) for a tree with n nodes.