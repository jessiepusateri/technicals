# Queue

### Time Complexity:

- enqueue: O(1)
    
- dequeue: O(1)
    
- peek: O(1)
    
- is_empty: O(1)
    
- size O(1)


### Implementation
```python
class Queue():
    def __init__(self):
        self.items = []

    # adds an item
    def enqueue(self, value):
        self.items.insert(0, value)

    # removes and returns the next item in line
    def dequeue(self):
        return self.items.pop()

    # returns the item at the front of the queue, without removing it
    def peek(self):
        return self.items[len(self.items) - 1]

    # returns true if the queue is empty, False otherwise
    def is_empty(self):
        if len(self.items) == 0:
            return True
        else:
            return False
            
    # returns the size of the queue
    def size(self):
        return len(self.items)
```   

