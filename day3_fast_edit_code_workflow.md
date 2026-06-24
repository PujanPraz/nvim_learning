# LazyVim Day 2 — Fast Editing & Real Coding Workflow

---

## Text Objects — The Most Powerful Vim Feature

Pattern:
```
operator + i/a + object
```

`i` = inside (excludes surrounding characters)
`a` = around (includes surrounding characters)

```
viw          → select inside word
vaw          → select word + space around it
vi"          → select inside " "
va"          → select " " and the quotes too
vi(          → select inside ( )
vi{          → select inside { }
vit          → select inside html tag
vi[          → select inside [ ]
```

Replace `v` with `d` to delete, `c` to change:
```
diw          → delete word
ciw          → change word (delete + insert)
di"          → delete inside quotes
ci{          → change inside { }
dit          → delete inside html tag
cit          → change inside html tag
```

---

## Indentation

```
>>           → indent line right
<<           → indent line left
V + j + >    → indent multiple lines
=            → auto indent
gg=G         → auto indent entire file
```

---

## Marks — Bookmarks Inside a File

```
ma           → set mark at current position (named 'a')
`a           → jump back to mark 'a'
``           → jump to last position
Ctrl+o       → jump back (like browser back button)
Ctrl+i       → jump forward
```

---

## Fast Navigation in Project

```
Space Space  → find file by name
Space /      → search text in all files
Space s g    → live grep (search as you type)
Space s r    → search recent files
gd           → go to definition
gr           → go to references
Ctrl+o       → go back after jumping to definition
```

---

## LSP Features — Code Intelligence

```
K            → show documentation
gd           → go to definition
gr           → find all references
gi           → go to implementation
Space c a    → code actions (fix errors, imports)
Space c r    → rename symbol everywhere
Space c d    → show diagnostics (errors/warnings)
]d           → jump to next error
[d           → jump to previous error
```

---

## Full Cheat Sheet

```
TEXT OBJECTS
viw / diw / ciw    → word
vi" / di" / ci"    → inside quotes
vi{ / di{ / ci{    → inside {}
vi( / di( / ci(    → inside ()
vit / dit / cit    → inside html tag

INDENT
>>  /  <<          → indent right / left
gg=G               → auto indent whole file

NAVIGATION
Ctrl+o             → jump back
Ctrl+i             → jump forward
gd                 → go to definition
gr                 → find references

LSP
K                  → docs
Space c a          → code actions
Space c r          → rename
]d / [d            → next / prev error
```
