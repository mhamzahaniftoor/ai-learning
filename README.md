# ai-learning

My notes and practice code from an AI learning course, kept as Jupyter notebooks. So far the repo covers week 1: Python fundamentals, from variables through custom exceptions (topics 11 to 47).

## Setup

The project uses [uv](https://docs.astral.sh/uv/) and Python 3.14.

```bash
git clone git@github.com:mhamzahaniftoor/ai-learning.git
cd ai-learning
uv sync
uv run jupyter lab
```

`uv sync` installs Jupyter, which is the only dependency. Open the notebooks from the `week1/` folder so that the file handling examples can find their sample files.

## Layout

```
ai-learning/
├── week1/                 # Python fundamentals notebooks and sample files
├── src/ai_learning/       # Package stub (prints a hello message)
├── pyproject.toml
└── uv.lock
```

## Week 1: Python fundamentals

Each topic has its own notebook, named `Topic NN | <title>.ipynb`. `Python_Course_Topics_11-47.ipynb` collects the notes for all topics in a single notebook.

| Topics | Subject | What is covered |
| --- | --- | --- |
| 11–15 | Basics | Variables and naming conventions, numbers, strings and booleans, lists, tuples, sets and dictionaries, type conversion, operators |
| 16–17 | Conditionals | `if`, `elif` and `else` statements |
| 18–22 | Loops | `for`, `while` and nested loops, looping over strings and dictionaries |
| 23–27 | Functions and modules | Defining and calling functions, parameters and return values, local and global scope, lambda functions, importing modules |
| 28–39 | Object-oriented programming | Classes and objects, `__init__`, instance variables and methods, encapsulation, getters and setters, inheritance, method overriding, polymorphism, special methods |
| 40–43 | File handling | Reading and writing files, read, write and append modes, context managers, handling errors during file operations |
| 44–47 | Exceptions | `try`, `except`, `else` and `finally`, raising exceptions, custom exceptions |

Some notebooks (for example topics 16 and 17) call `input()`, so they wait for you to type a value when run.

### Supporting files

These sit in `week1/` and are read or written by the notebooks:

| File | Used by |
| --- | --- |
| `my_module.py` | Topic 27, as the module to import |
| `demo.txt` | Topics 40, 41, 42 and 45 |
| `student.json`, `students.csv` | Topic 40 |
| `a.txt`, `b.txt`, `c.txt`, `copy.txt`, `notes.txt`, `archive.zip` | Topic 42 |

## Package stub

`src/ai_learning/` is the default package created by `uv init`. It only defines a `main()` entry point:

```bash
uv run ai-learning
# Hello from ai-learning!
```
