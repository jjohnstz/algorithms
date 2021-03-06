# Binary Trees (BT)
A "leaf node" has no subtrees, otherwise it is an "internal" node. Binary trees should not be confused with [B-trees](https://en.wikipedia.org/wiki/B-tree).
## Binary Search Tree (BST)
A "binary search tree" (BST) is also known as a "ordered binary tree." Elements to the left are less-or-equal (<=) to a given node. Elements to the right are greater (>) to the node.
## Depth First Traversals
### Pre-Order Traversal (NLR)
Pre-order traversal evaluates nodes in Node, Left, Right order.
```
void main()
   preOrder(root)

void preOrder(node)
   if (node == null) return
   doSomething(node)
   preOrder(node.left)
   preOrder(node.right)
```
### In-Order Traversal (LNR)
In-order traversal evaluates nodes in Left, Node, Right order.
```
void main()
   inOrder(root)

void inOrder(node)
   if (node == null) return
   inOrder(node.left)
   doSomething(node)
   inOrder(node.right)
```
### Post-Order Traversal (LRN)
Post-order traversal evaluates nodes in Left, Right, Node order.
```
void main()
   postOrder(root)

void postOrder(node)
   if (node == null) return
   postOrder(node.left)
   postOrder(node.right)
   doSomething(node)
```
## Breadth First Traversals
### Level-Order Traversal
Level order traversal evaluates nodes at each height/level, starting with the root node.
```
void levelOrder()
   queue.offer(root)
   while (!queue.isEmpty())
      node = queue.poll()
      doSomething(node)
      if (node.left != null)
         queue.offer(node.left)
      if (node.right != null)
         queue.offer(node.right)
```
