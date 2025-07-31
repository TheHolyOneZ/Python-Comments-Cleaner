# Python-Comments-Cleaner
These regex patterns are **better than most VS Code or VSCodium extensions** for removing comments, as they allow for more control and precision.



## 1. Full-Line Comments

### Regex Pattern:
```regex
^\s*#.*$
```

### Description:
Deletes entire lines that contain only comments, including those with leading spaces.

## 2. In-Line Comments

### Regex Pattern:
```regex
(?<=\s)#\s+.*$
```
---

## 3. Trailing (Inline) Comments After Code

### Regex Pattern:
```regex
(?<=\S)\s{2,}#.*$
```

### Description:
Deletes comments that appear after code, but only if there are **at least two spaces** before the `#`.

---

## 4. Strict Docstring Matching (One-Liner)
### Regex Pattern:
```
"""[^"]+"""
```
Description:
Matches strict one-line docstrings enclosed by triple quotes (""") in function definitions. This ensures it doesn't accidentally match strings or comments.

---

## Usage in VS Code or VSCodium 

1. **Open Find/Replace** (Ctrl+H)
2. **Turn on Regex mode** (the `.*` button)
3. **Paste the pattern in the "Find" field**
4. **Leave "Replace" blank** (empty)
5. **Click "Replace All"**
