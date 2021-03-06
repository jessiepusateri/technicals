# Tries (Prefix Trees)

### Time Complexity

| Function      | Time Complexity        | Space Complexity |
| ------------- |:----------------------:|:----------------:|
| Insert        | O(w) - w = len(word)   | O(1)             |
| Search        | O(w)                   | O(1)             |
| Delete        |                        |                  |
| Starts With   | O(p) - p = len(prefix) | O(1)             |
| Words         |                        |                  |
| Is Empty      |                        |                  |
| Count         |                        |                  |

- delete (deletes a word)
- count (returns a count of the keys)
- words (returns a list of the words in the tree)
- is_empty (returns whether the trie is empty)

## Dictionary-in-Dictionary Method



## Reference Method (Children referenced by dictionary)

```python
class TrieNode:
    def __init__(self):
        self.children = defaultdict(TrieNode)
        self.end_word = False

class Trie(object):
    def __init__(self):
        self.root = TrieNode()
    
    def insert(self, word):
        curr = self.root
        for letter in word:
            curr = curr.children[letter]
        curr.end_word = True

    def search(self, word):
        """
        Returns if the word is in the trie.
        """
        curr = self.root
        for letter in word:
            curr = curr.children.get(letter)
            if curr is None:
                return False
        return curr.end_word == True

    def startsWith(self, prefix):
        """
        Returns if there is any word in the trie that starts with the given prefix.
        """
        curr = self.root
        for letter in prefix:
            if letter not in curr.children:
                return False
            else:
                curr = curr.children[letter]
        return True
```
