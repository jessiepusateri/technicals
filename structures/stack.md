# Stack

Time Complexity:

- push: O(1)
    
- pop: O(1)
    
- peek: O(1)
    
- is_empty: O(1)
    
- size O(1)


```python
class Stack():
    def __init__(self):
        # bottom of stack is beginning of list
        # top of stack is end of list
        self.items = []

    # adds an item
    def push(self, value):
        self.items.append(value)

    # removes and returns the item from the stop of the stack
    def pop(self):
        return self.items.pop(value)
        
    # returns the item at the top of the stack, without removing it
    def peek(self):
        return self.items[len(self.items) - 1]

    # returns true if the stack is empty, False otherwise
    def is_empty(self):
        if len(self.items) == 0:
            return True
        else:
            return False
            
    # returns the size of the stack
    def size(self):
        return len(self.items)
```   

