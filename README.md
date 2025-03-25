# Valid Parentheses

## Problem Statement
Given a string `s` containing just the characters `'('`, `')'`, `'{'`, `'}'`, `'['`, and `']'`, determine if the input string is **valid**.

### A string is considered valid if:
- Open brackets must be closed by the **same type** of brackets.
- Open brackets must be closed in the **correct order**.
- Every closing bracket has a corresponding **open bracket** of the same type.

## Examples

### Example 1:
**Input:**
```python
s = "()"
```
**Output:**
```python
True
```

### Example 2:
**Input:**
```python
s = "()[]{}"
```
**Output:**
```python
True
```

### Example 3:
**Input:**
```python
s = "(]"
```
**Output:**
```python
False
```

### Example 4:
**Input:**
```python
s = "([])"
```
**Output:**
```python
True
```

## Constraints
- `1 <= s.length <= 10^4`
- `s` consists of only the characters `'('`, `')'`, `'{'`, `'}'`, `'['`, and `']'`.

## Approach
1. **Use a stack** to track open brackets.
2. **Iterate** through the string:
   - Push open brackets `(`, `{`, `[` onto the stack.
   - For closing brackets, check if the **top of the stack** is the matching open bracket.
3. **Validate** if the stack is empty at the end (indicating all brackets are properly closed).


## Complexity Analysis
- **Time Complexity:** `O(n)` – Each character is processed once.
- **Space Complexity:** `O(n)` – Space for the stack to store open brackets.

## Usage
To validate parentheses, call the function with a string:
```python
s = "()[]{}"
print(isValid(s))  # Output: True
```

## Related Topics
- Stack Data Structure
- String Manipulation
- Validations
