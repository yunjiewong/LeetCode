Tree

    class Node:
      def __init__(self, val):
          self.val = val
          self.left = None
          self.right = None
      

    root = Node(1)
    root.left = Node(2)
    root.left.right = Node(3)

Inorder Traversal:

####
    def inorder(root):
        if(root):
            inorder(root.left)
            print(root.val)
            inorder(root.right)
        
