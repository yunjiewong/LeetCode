543. Diameter of Binary Tree

    Input: root = [1,2,3,4,5]
    Output: 3
    Explanation: 3 is the length of the path [4,2,1,3] or [5,2,1,3].
    
####
    solution: recursion
    if a node has left and right, path =2
    for each node it returns 1+ max(left, right)
####
    def diameterOfBinaryTree(self, root):
        d = [0]

        def dfs(root):
            if not root:
                return -1
             left = dfs(root.left)
             right = dfs(root.right)
             d[0] = max(d[0], 2 + left + right)
             return 1 + max(left, right)

        dfs(root)
        return d[0]
