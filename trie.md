## Trie

**Definition**
- Trie is tree where each node represents a character in word and has 26 children.

**Usage**
- Trie is used to store all words/strings to process all at same time.

**Questions**
- Search auto complete: store all words with their frequency in trie, if search
ends, add new word into trie and reset current node to root.

- Word search in matrix: store all words in trie, run backtracking at each index
x, y and trie root node, if find a word, add it to result and remove from trie.

- Word filter by suffix and prefix: for each word in dictionary, we store
suffix + '#' + word in trie
