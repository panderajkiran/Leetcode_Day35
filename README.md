# Leetcode_Day35
# 🚀 Day 35 — Palindrome Number

## 🧩 Problem
**LeetCode 9 — Palindrome Number**

**Difficulty:** Easy

Given an integer `x`, return `true` if `x` is a palindrome, otherwise return `false`.

A palindrome reads the same from left to right and right to left.

### Examples

- `121` → `true`
- `-121` → `false`
- `10` → `false`

---

## 💡 Approach

I solved this problem by reversing the number and comparing it with the original number.

### Steps:
1. Store the original number in a temporary variable.
2. Extract the last digit using `x % 10`.
3. Build the reversed number using:
   `res = res * 10 + digit`
4. Remove the last digit using:
   `x = x / 10`
5. Finally, compare the reversed number with the original number.

If both are equal, the number is a palindrome.

---

## 💻 Java Solution

```java
class Solution {
    public boolean isPalindrome(int x) {
        int temp = x;
        int res = 0;

        while (temp > 0) {
            int digit = temp % 10;
            res = res * 10 + digit;
            temp /= 10;
        }

        return res == x;
    }
}
⏱️ Complexity
Time Complexity: O(log n)
Space Complexity: O(1)
📚 What I Learned

Today's problem helped me practice digit extraction and number reversal using % and /.

The important idea was that we don't always need to convert a number into a string to check its properties. Sometimes, simple mathematical operations are enough.

🌱 Day 35 Takeaway

A simple problem can still teach an important technique.
The more comfortable I become with the basics, the easier it becomes to approach bigger problems.
