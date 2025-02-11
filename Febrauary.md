Date: 11-02-2025

1910. Remove All Occurrences of a Substring

📝 Simple Explanation
🔹 We have a string s and need to remove all occurrences of part until it no longer exists.
🔹 Find the first occurrence of part in s.
🔹 Remove it by slicing the string before and after part.
🔹 Repeat this process until part is gone.
🔹 Finally, return the modified string.

Example 🔍
📝 Input: s = "daabcbaabcbc", part = "abc"

🔄 Steps:
1️⃣ "daabcbaabcbc" → Remove "abc" → "dabaabcbc"
2️⃣ "dabaabcbc" → Remove "abc" → "dabcbc"
3️⃣ "dabcbc" → Remove "abc" → "dbc"
4️⃣ "dbc" → No "abc" left, so stop.

✅ Final Output: "dbc"

```python

class Solution(object):
    def removeOccurrences(self, s, part):
        """
        :type s: str
        :type part: str
        :rtype: str
        """
        while True:
            if part in s:
                temp=s.find(part)
                s = s[:temp]+s[temp+len(part):]
            else:
                break
        return s

```
