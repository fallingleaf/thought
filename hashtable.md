## Hash table

**Definition**
- Hash table is data structure storing key value for fast look up.

**Usage**

1. Store previous processed data
    - Longest arithmetic sequence: use hash map to store every possible distance
    for each number.

    - Palindrome pair: find if 2 string can form palindrome, use hash map to store
    all current string with its index, for each string check if its prefix or
    suffix is palindrome and look up in hash map.

    - Word pattern: check if list of words follow the pattern, use hash map to store
    mapping from word to pattern char.

    - Longest repeated substring: use hash map to store substring with its end index,
    for new substring check if it exists in hash map without overlap with previous
    substring.

    - Fraction decimal: use hash map to store remain value with index, if encounter
    same remain value again stop running and put parentheses.

2. Store count of each element in list
    - Substring concatenate all words: use hash map to store count of all words,
    check if substring window contains all words.

    - K frequent elements: store count of each elements, use heap to find K elements.

3. Present graph data structure: node with list of neighbors

4. Group data result
    - Group anagram: count chars of each word, use hash map with key is counter,
    value is list of words.

    - Group shifted string: calculate distance of first char to 'a', shift all
    strings to string starting with 'a', store it in hash map as key.
