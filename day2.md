# LazyVim Day 2 — Visual Mode & LazyVim Superpowers

---

## Visual Mode — Selecting Text

```
v        → character select (select letter by letter)
V        → line select (select whole lines)
Ctrl+v   → block select (select a rectangle/column)
```

After selecting:
```
d        → delete selection
y        → copy selection
c        → change selection (delete + insert)
>        → indent right
<        → indent left
```

---

## LazyVim Superpowers

> `Space` is your leader key. Almost everything starts with `Space`.

### File Finding
```
Space Space  → find files in project (like Ctrl+P in VSCode)
Space /      → search text inside all files (like Ctrl+Shift+F)
Space e      → toggle file explorer
Space E      → file explorer (current file location)
```

### Window Splits
```
Space |      → split vertically
Space -      → split horizontally
Ctrl+h       → move to left split
Ctrl+l       → move to right split
Ctrl+j       → move to bottom split
Ctrl+k       → move to top split
```

### Buffers (open files)
```
Space b b    → switch between open files
Space b d    → close current file
H            → previous open file
L            → next open file
```

### Code Actions (LSP)
```
g d          → go to definition
g r          → find references
g h          → show hover docs
Space c a    → code actions
Space c r    → rename symbol
K            → show documentation popup
```

### Git
```
Space g g    → open lazygit
Space g b    → git blame current line
```

### Terminal
```
Ctrl+/       → toggle floating terminal
```

---

## VSCode → LazyVim Reference

| VSCode | LazyVim |
|---|---|
| `Ctrl+P` | `Space Space` |
| `Ctrl+Shift+F` | `Space /` |
| `Ctrl+Shift+E` | `Space e` |
| `F12` | `gd` |
| `Shift+F12` | `gr` |
| `Ctrl+.` | `Space ca` |
| `Ctrl+Z` | `u` |
| `Ctrl+\`` | `Ctrl+/` |
| Split editor | `Space |` |
| Close tab | `Space bd` |
| Rename symbol | `Space cr` |
