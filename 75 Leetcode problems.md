Web link: [leetcode grind75](https://www.techinterviewhandbook.org/grind75)
Link: [[Data structures & Algorithms]]
### [Two sum](https://leetcode.com/problems/two-sum)
**Good solution: using Map
   - One-pass Hash table -> Create Map with values first and then check.
   - Two-pass Hash table -> Create empty Map and then add value to check when iterate through the array.
### [Valid Parentheses](https://leetcode.com/problems/valid-parentheses)
**Good solution: using Stack**
### [Merge two sorted linked lists](https://leetcode.com/problems/merge-two-sorted-lists/)
**Solution: using while loop or recursive**
Don't care which list will merge to which. if the value of list1 is equal or smaller than list2. Then the `list1.next` will be list2.
- [Recursive solution](https://authorslog.com/blog/oXmSPEGRc3?title=21-merge-two-sorted-lists)
- Loop solution
### [Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock)
Best solution: using two pointers
1. Left < Right  => Max(left - right, result)
2. Left >= Right => leftPtr = rightPtr
### [Valid Palindrome](https://leetcode.com/problems/valid-palindrome)
Best solution: turn string into vaild string and then 
`return string == reverse(string)`
### [Invert Binary Tree](https://leetcode.com/problems/invert-binary-tree)
Best solution: Breadth First Search
1. Push root into `Queue`
2. Swap `Left node` with `Right node`
3. Continue BFS
### [Valid Anagram](https://leetcode.com/problems/valid-anagram)
Solution: Using map
1. Add key is character and + value is number of character in s 
2. Add key is character and - value is number of character in t
3. If value in map is not 0 then false