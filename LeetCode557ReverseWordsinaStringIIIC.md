# LeetCode: #557 Reverse Words in a String III(C++)

### Description
Given a string, you need to reverse the order of characters in each word within a sentence while still preserving whitespace and initial word order.

Example 1:
Input: "Let's take LeetCode contest"

Output: "s'teL ekat edoCteeL tsetnoc"

### Solution
```
class Solution {
public:
    string reverseWords(string s) {
        
        int start = 0;
        int end = 0;
        int k = s.size();

        while(start < k && end < k)
        {
           while (end < k && s[end] != ' ')
            {
            end++;
            }
                for(int i = start, j = end - 1; i < j; i++, j--)
                {
                swap(s[i], s[j]);
            }
            start = ++end;
        }
        return s;
    }
};
```

### Process

To begin this problem I took the same approach as Leetcode question 344. I set the start and end and a integer to set the size. I then made my first while statement that checks if the entire string is finished or not based on comparison statement. After that statement is the next while loops that accounts for spaces in the string, if a space is found then it will increase its place in the string array. In the last loop it is where the actual swapping letters happen to reverse the string. Putting a simple swap() statement can make this possible. I was getting some errors with the statement "start = ++end", I originally put end++ but that didn't work because  it was a post increment and not a pre-increment. 

### Results

Runtime: 20 ms, faster than 86.57% of C++ online submissions for Reverse Words in a String III.

Memory Usage: 11.6 MB, less than 100.00% of C++ online submissions for Reverse Words in a String III.