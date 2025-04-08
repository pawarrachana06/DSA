# Python Code Quality Tools (Layman Style)

## 🍕 Real-Life Analogy

> Imagine you're running a **pizza shop**. You want clean boxes, safe food, and efficiency. Python tools help manage your code like that!

---

## 🧼 `black` — The Pizza Box Folder

**Layman Meaning:**
> "Formats your code to look neat and consistent. Doesn't fix bugs."

**Real-life analogy:** Neatly folds pizza boxes every time, same way.

### ✅ Installation
```bash
pip install black
```

### 🔧 Usage
```bash
black your_script.py
```

### 💡 What It Does
Turns this:
```python
def cook(pizza,time):return pizza*time
```
Into:
```python
def cook(pizza, time):
    return pizza * time
```

---

## 🕵️ `pylint` — The Strict Pizza Inspector

**Layman Meaning:**
> "Scans your code for mistakes, unused stuff, or bad practices. Doesn’t fix, only warns."

**Real-life analogy:** Food inspector that checks hygiene, warns you of risks.

### ✅ Installation
```bash
pip install pylint
```

### 🔧 Usage
```bash
pylint your_script.py
```

### 💡 What It Does
Warns you if you do this:
```python
def cook(pizza, time):
    return pizaa * time  # typo!
```
Error:
> Undefined variable 'pizaa'

Also gives a **score out of 10**.

---

## 🤖 `ruff` — The Fast Robot Assistant

**Layman Meaning:**
> "Combines both black + pylint — auto-fixes style AND catches issues. Super fast!"

**Real-life analogy:** Robot that folds boxes and checks hygiene **together**, fast!

### ✅ Installation
```bash
pip install ruff
```

### 🔧 Usage
```bash
ruff your_script.py          # Just lint
ruff --fix your_script.py    # Auto-fix too
```

### 💡 What It Does
Takes this:
```python
def cook(pizza ,time):return pizza*time
```
And:
- Fixes spacing
- Adds proper indentation
- Warns if a variable is unused

All in one go ⚡

---

## ⚖️ Tool Comparison

| Tool     | Role                     | Fixes Style | Catches Bugs | Speed  | Best For                  |
|----------|--------------------------|-------------|--------------|--------|---------------------------|
| `black`  | Formatter                 | ✅ Yes      | ❌ No         | ⚡ Fast | Simple formatting         |
| `pylint` | Linter                   | ❌ No       | ✅ Yes        | 🐢 Slow | Deep code analysis        |
| `ruff`   | Linter + Formatter       | ✅ Yes      | ✅ Yes        | 🚀 Super fast | All-in-one solution |

---

> 🧠 Want to combine all in one project? Ask me and I’ll help you create a `pre-commit` setup!

