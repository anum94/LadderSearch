# Word Ladder 
https://en.wikipedia.org/wiki/Word_ladder

Word Ladder is a game in which the player tries to get from one word (“start word”) to another (“goal word”) using minimal steps. 
In each step, the player can either add one letter to the word or take one letter away, rearrange the letters to make a new word.

Example: croissant to baritone

croissant

( - C )
arsonist

( - S )
aroints

( + E ) 
notaries

( + B )
baritones

( - S )
baritone

##Solution using breadth-first search algorithm:


- Each node represents a word and the children (actions) of this node are the words that can follow in the next step.
- You should implement a search algorithm to find the shortest ladder between a start word and a goal word. 
- All words in between must exist in the file wordList.txt 

####Explanation:
- In this breadth first search, as an initial step, all words are created first that are one hop away from the start_word (also a valid dictionary word)and added into a que. 
- Once all the words have been added, the algo compares the que elements in FIFO order. 
- If the output word is not found one hop away, the algo computes ladders (two/three hops away) from all the elements of the que and so on until goalword is found. 
- If all the possible search results have been exhausted, and the goal_word is not found, the search concludes.

# Usage

python ladders.py startword goalword

Note: startword and goalword should be words present in wordList.txt