```python
def mergeTrees(root1, root2):
    root = None
    if root1 and root2:
        root = TreeNode(root1.val + root2.val)
    else:
        root = root1 if root1 else root2
    if root:
        if root1 and root2:
            root.left = self.mergeTrees(root1.left, root2.left)
            root.right = self.mergeTrees(root1.right, root2.right)
        elif root1 or root2:
            root.left = root1.left if root1 else root2.left
            root.right = root1.right if root1 else root2.right
    return root
```