# GitHub Reference for CSC600 Students
*Compiled by Justin Puno — Cycles 1 & 2, Spring 2026*

> Personal reference guide. Not actively maintained — use it as a starting point, not a source of truth.

---

## The Mental Model

Git tracks changes to your files over time. Every "commit" is a saved snapshot with a note explaining what you did. GitHub hosts those snapshots online so two people can work on the same project without overwriting each other.

---

## Setting Up

1. Create a new repo on GitHub — check "Add a README"
2. Clone it locally: `git clone https://github.com/your-username/repo-name.git`
3. Add your partner: **Settings → Collaborators → Add people**

---

## Repo Structure

Keep it simple and organized from the start:

```
your-project/
├── README.md
├── .gitignore
├── data/
│   ├── raw/          ← never edit these
│   └── processed/
├── notebooks/
├── paper/
└── figures/
```

Your README should answer: what is this, what data does it use, and how do you reproduce it.

---

## Daily Workflow

```bash
git pull origin main        # always start here
# ... do your work ...
git add .
git commit -m "Describe what you actually changed"
git push origin main
```

**Always pull before you push.** This prevents most conflicts before they happen.

---

## Commit Messages

Write them like you're leaving a note for your partner.

| ❌ | ✅ |
|----|----|
| `update` | `Add vig-stripping function to data cleaning script` |
| `fix stuff` | `Fix implied probability calculation for negative odds` |
| `changes` | `Draft introduction section with research question` |

---

## Resolving Merge Conflicts

When two people edit the same part of a file, Git flags it like this:

```
<<<<<<< HEAD
your version of the code
=======
your partner's version
>>>>>>> branch
```

To fix it: open the file, decide what it should say, delete the conflict markers, then:

```bash
git add filename
git commit -m "Resolve merge conflict in [file]"
git push origin main
```

**Practice this before it happens in your real repo.** Make a test conflict on purpose and walk through it with your partner.

---

## Resources

- [GitHub Quickstart](https://docs.github.com/en/get-started/quickstart) — start here
- [Oh Shit, Git!](https://ohshitgit.com/) — plain-language fixes for common disasters
- [Missing Semester — Version Control](https://missing.csail.mit.edu/2020/version-control/) — best conceptual explanation

---

*Spring 2026*
