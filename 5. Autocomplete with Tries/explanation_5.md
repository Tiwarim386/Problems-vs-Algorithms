# Problem 5: Autocomplete with Tries


The solution to this problem was a simple recursive function that returns the word, if the suffix algorithm hits a node with `is_word == True`, and otherwise recrusively follows the Trie to find end points.

The time and complexity of traversing the Trie is best case O(k), where k is the length of the longest word, and worst case O(n), where n is the number of words in the Trie. The best case, all words in the Trie have common letters (like 'a', 'an', 'ant', 'anteater') in which case the algorithm will only take as long as the longest word to traverse. In the worst case where no letters are shared (like with 'dog' and 'ant' and 'burr') then each word will be in a separate branch that must be traversed, taking both O(n) storage and time to traverse. Because the solution is implemented recursively, the call stack will be at its longest when traversing the deepest branch, or the longest word assigned to the dictionary and thus O(k). 