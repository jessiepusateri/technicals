# Level-Order Traversal

## Method 1: Keon
```python
def level_order(root):
    output = [] # final list
    if not root:
        return output # empty
    prev_level_nodes = [root]
    while prev_level_nodes:
        unpacked_vals = []
        next_level_nodes = []

        # unpack prev_nodes into list and prepare next_level's nodes
        for node in prev_level_nodes:
            unpacked_vals.append(node.val)
            if node.left:
                next_level_nodes.append(node.left)
            if node.right:
                next_level_nodes.append(node.right)
            # pass off children nodes to unpack in the next loop
            prev_level_nodes = next_level_nodes
            output.append(unpacked_vals)
    return output
```

## Method 2: Keyan - Use a Queue
This is essentially the same as Method 1 except it uses a queue instead
of copying over lists.

```python
def level_order_queue(root):
    output = [] # final list
    
    if not root:
        return output # empty
    
    queue = []
    queue.insert(0, root)
    
    while queue:
        unpacked_vals = []
        num_nodes_in_this_level = len(queue)
        
        for _ in range(num_nodes_in_this_level):
            node = queue.pop()
            
            if node.left:
                queue.insert(0, node.left)
            if node.right:
                queue.insert(0, node.right)
            # pass off children nodes to unpack in the next loop
            unpacked_vals.append(node.val)
        output.append(unpacked_vals)
    
    return output
```

