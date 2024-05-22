**58.Given a string s consisting of words and spaces, return the length of the last word in the string.**
**Решение:**
```cpp
class Solution {
public:
    int lengthOfLastWord(string s) {
        int length = 0;
        int i = s.length() - 1;
        
        while (i >= 0 && s[i] == ' ') {
            i--;
        }
        
        while (i >= 0 && s[i] != ' ') {
            length++;
            i--;
        }
        
        return length;
    }
};
```
**Задача:**
**70.Each time you can either climb 1 or 2 steps. In how many distinct ways can you climb to the top?**
**Решение:**
```cpp
class Solution {
public:
    int climbStairs(int n) {
       if (n == 1) {
return 1;
}
int first = 1;
int second = 2;
for (int i = 3; i <= n; i++) {
int third = first + second;
first = second;
second = third;
}
return second; 
    }
};
```
**Задача:**
**136.Given a non-empty array of integers nums, every element appears twice except for one. Find that single one.**
**Решение:**
```cpp
class Solution {
public:
    int singleNumber(vector<int>& nums) {
      int result = 0;
        for (int num : nums) {
            result ^= num;
        }
        return result;  
    }
};
```