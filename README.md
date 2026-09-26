<div align="center">

# UNIX Systems Programming

**Coursework · 32547 UNIX Systems Programming · University of Technology Sydney · Autumn 2024**

![Python](https://img.shields.io/badge/Python-3.12-3776AB?logo=python&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?logo=gnubash&logoColor=white)
![Markdown](https://img.shields.io/badge/Notes-Markdown-000000?logo=markdown&logoColor=white)
![Ruff](https://img.shields.io/badge/Ruff-D7FF64?logo=ruff&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-yellow)

[Contents](#contents) · [Getting started](#getting-started) · [Related repositories](#related-repositories)

</div>

My notes, tutorial answers and the assignment from the UNIX Systems Programming subject I took during an exchange
semester at UTS: shell basics, pipes and redirection, `grep` and regular expressions, and Python scripting on UNIX.

> [!NOTE]
> Unofficial study material, kept as submitted in 2024. Nothing is corrected, so answers can be wrong or incomplete.
> The repository is not developed further. Assignment specifications, slides and lecture examples from the teaching
> staff are not included.

## Course

| | |
|---|---|
| Subject | 32547 UNIX Systems Programming |
| Institution | University of Technology Sydney, Faculty of Engineering and IT |
| Semester | Autumn 2024 (February to June), exchange semester from the University of Zurich |

## Contents

| Folder | Topic | Files |
|---|---|---|
| [`summaries/`](summaries/) | Course summaries and a cheat sheet | [UNIX summary](summaries/unix-summary.md), [lecture summary](summaries/unix-lecture-summary.md), [cheat sheet](summaries/unix-cheat-sheet.md), [Python summary](summaries/python-summary.md) |
| [`exercises/week2/`](exercises/week2/) | Scripting basics, files and permissions | [Tutorial](exercises/week2/Unix%202%20-%20Scripting%20basics.md), [exercises](exercises/week2/exercises.md) |
| [`exercises/week3/`](exercises/week3/) | Pipes and redirection | [Tutorial](exercises/week3/Unix%203%20-%20Piping%20and%20Redirections.md) |
| [`exercises/week4/`](exercises/week4/) | `grep` and regular expressions | [Tutorial](exercises/week4/Unix%203%20-%20GREP.md) |
| [`exercises/grep/`](exercises/grep/) | Revised `grep` notes and example commands | [Revised notes](exercises/grep/Unix%203%20-%20GREP%20%28revised%29.md), [examples](exercises/grep/examples.txt) |
| [`exercises/python/`](exercises/python/) | Python on UNIX: `sys.argv`, stdin, lookup tables, functions | `ex1.*.py`, `l3_*.py`, `l4_*.py`, `lists.py` |
| [`exercises/python/re/`](exercises/python/re/) | Regular expressions with the `re` module | One script per concept (`match`, `search`, `findall`, `sub`, groups, flags) |
| [`exercises/python/snippets/`](exercises/python/snippets/) | Small scripts from the lab and screenshots of their output | `*.py`, `*.png` |
| [`assignment/`](assignment/) | Assignment: `locale.py`, a command-line tool that lists locales and charmaps from an argument file | [`locale.py`](assignment/locale.py), [test files](assignment/data/) |

## Getting started

You need [uv](https://docs.astral.sh/uv/). The scripts only use the Python standard library.

1. Create the environment:

   ```bash
   uv sync
   ```

2. List all locales in a test file:

   ```bash
   uv run python assignment/locale.py -a assignment/data/test_argument_file.csv
   ```

3. Show the locales and charmaps for one language:

   ```bash
   uv run python assignment/locale.py -l English assignment/data/test_argument_file.csv
   ```

The other options are `-m` (charmaps) and `-v` (author details). The assignment required the name `locale.py`, which
is also the name of a standard library module, so run it as a script and do not import it.

| Task | Command |
|---|---|
| Lint the scripts | `uv run ruff check .` |

## Data

The files in [`assignment/data/`](assignment/data/) are small test inputs I wrote for the assignment (type, language,
file name per line). There are no external datasets.

## Related repositories

Other subjects from the same exchange semester at UTS:

| Subject | Repository |
|---|---|
| 32130 Fundamentals of Data Analytics | [data-analytics-uts](https://github.com/HuberNicolas/data-analytics-uts) |
| 42037 IoT Security | [iot-security-uts](https://github.com/HuberNicolas/iot-security-uts) |
| Python Programming for Data Processing | [python-data-processing-uts](https://github.com/HuberNicolas/python-data-processing-uts) |
| 32547 UNIX Systems Programming | this repository |

## License

My own code and notes are licensed under the [MIT License](LICENSE). Material from the course that is quoted in the
notes (task descriptions) belongs to the University of Technology Sydney.

## Author

Nicolas Huber ([@HuberNicolas](https://github.com/HuberNicolas)), exchange student at UTS in Autumn 2024.
