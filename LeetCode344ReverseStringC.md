# LeetCode: #344 Reverse String (C++)

### Description
Write a function that reverses a string. The input string is given as an array of characters char[].

Do not allocate extra space for another array, you must do this by modifying the input array in-place with O(1) extra memory.

You may assume all the characters consist of printable ascii characters.

Example 1:

Input: ["h","e","l","l","o"]
Output: ["o","l","l","e","h"]
Example 2:

Input: ["H","a","n","n","a","h"]
Output: ["h","a","n","n","a","H"]

```
class Solution {
public:
    void reverseString(vector<char>& s) 
    {
        int start = 0;
        int end = s.size()-1;
        char temp;
        
        while(start < end)
        {
            temp = s[start];
            
            s[start]=s[end];
            
            s[end]=temp;
            
            ++start;
            --end;
        }
    }
};
```

### Process
My first Leetcode problem, I started with a simple reverse string algorithm type of problem. I began this problem by setting the start and end of the string to get the places within the array. After I made a "while" statement that simply swaps the start with the end until all values of the array are finished.


### Results

Runtime: 56 ms, faster than 12.07% of C++ online submissions for Reverse String.

Memory Usage: 15.2 MB, less than 93.90% of C++ online submissions for Reverse String.