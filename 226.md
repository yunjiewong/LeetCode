226. Invert Binary 


    def invertTree(self, root):
        
        def invert_help(root):
            if root is None:
                return
            
            root.left, root.right = root.right, root.left
            invert_help(root.left)
            invert_help(root.right)
            
        invert_help(root)
        return root
            
            
            
####
     def invertTree(self, root):

            if root:
                        root.left, root.right = self.invertTree(root.right), self.invertTree(root.left)
            return root
