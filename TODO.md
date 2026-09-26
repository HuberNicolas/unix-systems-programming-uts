# TODO

Open tasks before the repository is made public. The full original state is kept in the private repository
`unix-systems-programming-uts-archive`.

## 1. Clean-up

- [x] Remove the assignment specification and the lecture examples written by the teaching staff
- [x] Remove `ansible.log` (internal UTS lab infrastructure log) and the shell histories
- [x] Remove byte-identical duplicates and rename `Summaries/` to `summaries/`
- [x] Add a uv project (Python 3.12, standard library only) and check that `assignment/locale.py` runs

## 2. Before publishing

- [x] Add the MIT license
- [x] Add the course context (subject, institution, semester) to the README
- [x] Rewrite the history: old email addresses to `nicolas.huber.dev@gmail.com`, removed UTS material and
      `ansible.log` out of all commits
- [ ] Rename the repository on GitHub to `unix-systems-programming-uts`, then run
      `git remote set-url origin git@github.com:HuberNicolas/unix-systems-programming-uts.git`
- [ ] Force-push `main`
- [ ] Set the GitHub description and topics
