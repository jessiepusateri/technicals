# Min-Heap

### Time Complexity:

- insert: O(log n)*

*This is worst-case since we need at most one swap on each level of a heap on the path from the inserted node to the root.

- delete_min: O(log n)**

**Similar to insert, this is worst-case.

- build_heap: O(n)

### Implementation:
```python
class MinHeap():
    def __init__(self):
        self.heap_list = [0]
        self.current_size = 0
    
    # --- INSERT --- 
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
        
   # --- DELETE MIN ---
   def min_child(self, i):
        # if there is no right child, the min child is the left child
        if (i * 2 + 1) > self.current_size:
            return i * 2
        else:
            if self.heap_list[i * 2] > self.heap_list[i * 2 + 1]:
                return i * 2 + 1
            else:
                return i * 2
   
   def perc_down(self, i):
        # while there's at least a left child to work with
        while (i * 2) <= self.current_size:
            mc = self.min_child(i)
            if self.heap_list[i] > self.heap_list[mc]:
                tmp = self.heap_list[i]
                self.heap_list[i] = self.heap_list[mc]
                self.heap_list[mc] = tmp
            i = mc
    
    def del_min(self):
        ret_val = self.heap_list[1]
        self.heap_list[1] = self.heap_list[self.current_size]
        self.current_size -= 1
        self.heap_list.pop()
        self.perc_down(1)
        return ret_val
    
   
```

