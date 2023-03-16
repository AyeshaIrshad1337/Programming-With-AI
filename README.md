# Programming-With-AI
In this repository i will be sharing my python code from beginning to depth as their is no end xD
<h2>BFS </h2>
<code>class Node:
  def __init__(self, value,left=None,right=None):
    self.value=value
    self.left=left
    self.right=right
  def __str__(self):
    return "Node: "+str(self.value)
def bfs(node,queue):
  queue.append(node)
  while len(queue) > 0:
    node = queue.pop(0)
    
    if node is not None:
      queue.append(node.left)
      queue.append(node.right)  
      print(node)

mytree= Node('A',Node('B',Node('D'),Node('E')),Node('C',Node('F'),Node('G')))
print(bfs(mytree,[]))
</code>
<h2>DFS</h2>
<h3>One Way</h3>
<code>
def walk(tree):
  if tree is not None:
    print(tree)
    walk(tree.left)
    walk(tree.right)
mytree= Node('A',Node('B',Node('D'),Node('E')),Node('C',Node('F'),Node('G')))

walk(mytree)
</code>
<h3>Second Way</h3>
<code>
def walk2(tree,stack):
  stack.append(tree)
  while len(stack)>0:
    node=stack.pop()
    if node is not None:
      print(node)
      stack.append(node.right)
      stack.append(node.left)
walk2(mytree,[])      
</code>
