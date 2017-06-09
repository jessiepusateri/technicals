# Min-Heap

### Time Complexity:


### Implementation:
```python
class MinHeap():
    def __init__(self):
        self.heap_list = [0]
        self.current_size = 0
        
    def perc_up(self, i):
        while i / 2 > 0:
            if self.heap_list[i/2] > self.heap_list[i]:
                tmp = self.heap_list[i/2]
                self.heap_list[i/2] = self.heap_list[i]
                self.heap_list[i] = tmp
            i = i / 2
    
    def insert(self, k):
        self.heap_list.append(k)
        self.current_size += 1
        self.perc_up(self.current_size)
        
   def min_child(self, i):
        # if there is no right child, the min child is the left child
        if (i * 2 + 1) > self.current_size:
            return i * 2
        else:
            if self.heap_list[i * 2] > self.heap_list[i * 2 + 1]:
                return i * 2 + 1
            else:
                return i * 2
```

