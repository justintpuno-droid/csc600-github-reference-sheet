# GitHub Reference for CSC600 Partner Projects
Justin Puno
\n 5/28/26

## The Mental Model

Git tracks changes to your files over time. Therefore, you can think of every "commit" as a saved snapshot of your project with a note explaining what you did or changed. GitHub hosts those snapshots online so two or more people can work on the same project without overwriting each other.

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
│   ├── raw/          
│   └── processed/
├── notebooks/
├── paper/
└── figures/
```

Your README should provide a brief overview of your project and answer some key questions: what is this, what data does it use, and how do you reproduce it.

---

## Daily Workflow

```bash
git pull origin main        # start here
# ... do your work ...
git add .
git commit -m "Describe what you actually changed"
git push origin main
```

**Always pull before you push.**

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

When two people edit the same part of a file, Git gives an error message it like this:

```
<<<<<<< HEAD
your version of the code
=======
your partner's version
>>>>>>> branch
```

To fix it: open the file, decide what it should say, then:

```bash
git add filename
git commit -m "Resolve merge conflict in [file]"
git push origin main
```

**Practice this before it happens in your real repo.** Make a test conflict on purpose and walk through it with your partner.

---

## Resources

- [Nick's Github Resources](https://github.com/nzufelt/resources_for_students/blob/master/git.md)
- [GitHub Quickstart](https://docs.github.com/en/get-started/quickstart)
- [Oh Shit, Git!](https://ohshitgit.com/)
- [Missing Semester — Version Control](https://missing.csail.mit.edu/2020/version-control/)

---
