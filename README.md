# Problem Ladders

Ladders is a word game where a player tries to get from one word (the “start word”) to another (the
“goal word”) in as few steps as possible. In each step, the player must either add one letter to the word
from the previous step, or take away one letter, and then rearrange the letters to make a new word.

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

This can be modeled as a search problem, where each node represents a word and the children (actions)
of this node are the words that can follow in the next step. You should implement a search algorithm to
find the shortest ladder between a start word and a goal word. All words in between must exist in the
file wordList.txt provided in Moodle in the folder example solution.
Implementation of the Ladder Search game in python using Breadth Search to find a ladder from start word to end word given a dictionary

#My Solution

* My solution is breadth first search, in my algo all those words are created first that are one hop away from the start_word (and are also a valid dictionary word) and added into a que. Once all the words have been added, the algo compares the que elements in FIFO order to the goal_order. If the output is not found, the algo computes ladders (two/three hops away or se) from all the elements of the que and so on until the correct ladder is found. If all the possible search results have been exhausted and the goal_word is not found, it is concluded.
* I also used certain optimization techniques in order to reduce the search time

# Usage

python ladders.py startword goalword

where startword and goalword should be words present in wordList.txt