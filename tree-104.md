104. Maximum Depth of Binary Tree

#### Recursion
    def maxDepth(self, root: Optional[TreeNode]) -> int:
        if not root:
            return 0

        return 1 + max(self.maxDepth(root.left), self.maxDepth(root.right))


#### iterative dfs
    def maxDepth(self, root: Optional[TreeNode]) -> int:
        stack = [[root, 1]]
        res = 0
        while stack:
              node, depth = stack.pop()
              res = max(res, depth)
              stack.append([node.left, depth + 1])
              stack.append([node.right, depth + 1])
       return res
    
