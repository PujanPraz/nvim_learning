# LazyVim Day 1 Notes — Survival Mode

---

## The Most Important Concept — Modes

Vim has **modes**. This is the biggest difference from every other editor.

| Mode | Purpose |
|---|---|
| NORMAL | Default mode — for moving around (NOT for typing) |
| INSERT | For typing text like a normal editor |
| VISUAL | For selecting text |
| COMMAND | For running commands like save, quit |

> **Rule #1 — When lost or confused, press `Esc`.**

---

## Switching Modes

```
i        → NORMAL to INSERT (start typing)
Esc      → back to NORMAL (use this constantly)
v        → NORMAL to VISUAL
:        → NORMAL to COMMAND
```

---

## Basic Movement (never use arrow keys)

```
h        → left
j        → down
k        → up
l        → right
```

---

## Word Movement

```
w        → jump forward one word
b        → jump backward one word
e        → end of current word
0        → go to start of line
$        → go to end of line
gg       → go to top of file
G        → go to bottom of file
```

### Count + Motion trick

```
5j       → move down 5 lines
5k       → move up 5 lines
3w       → jump 3 words forward
4b       → jump 4 words backward
10j      → move down 10 lines
```

---

## Searching in a File

```
/word    → search forward for "word"
n        → next match
N        → previous match
*        → search for word under cursor
```

---

## Basic Editing in NORMAL Mode

```
x        → delete character under cursor
dd       → delete entire line
u        → undo
Ctrl+r   → redo
o        → new line below + enter INSERT
O        → new line above + enter INSERT
A        → jump to end of line + enter INSERT
```

---

## Operators + Motions — The Most Powerful Concept

Vim commands follow this pattern:

```
OPERATOR + MOTION = ACTION
```

### Operators

```
d        → delete (stay in NORMAL mode)
c        → change (delete + go to INSERT mode)
y        → yank (copy)
p        → paste after cursor
P        → paste before cursor
```

### Combinations

```
dw       → delete one word
d$       → delete to end of line
dd       → delete entire line
cw       → change one word (delete + enter INSERT)
cc       → change entire line
yy       → copy entire line
yw       → copy one word
```

### Delete vs Change

```
dw       → delete word, stay in NORMAL
cw       → delete word, start typing replacement immediately
```

> Use `c` when you want to replace something — it's faster than `d` + `i`.

---

## Save and Quit

```
:w       → save
:q       → quit
:wq      → save and quit
:q!      → quit without saving
:qa      → quit all open files
```

---

## Full Cheat Sheet

```
MODES
i            → insert
Esc          → normal
:            → command

MOVEMENT
h j k l      → left down up right
w / b / e    → next / prev word / end of word
0 / $        → line start / end
gg / G       → file top / bottom
5j / 3w      → move by count

SEARCH
/word        → search
n / N        → next / prev match
*            → search word under cursor

OPERATORS
d            → delete
c            → change (delete + insert)
y            → yank (copy)
p / P        → paste after / before

COMBINATIONS
dw / cw / yw → word
dd / cc / yy → whole line
d$ / c$      → to end of line

FILE
:w           → save
:q           → quit
:wq          → save + quit
:q!          → force quit
```

---

## What NOT to do on Day 1

- Don't try to configure anything
- Don't install more plugins
- Don't use the mouse
- Don't use arrow keys
