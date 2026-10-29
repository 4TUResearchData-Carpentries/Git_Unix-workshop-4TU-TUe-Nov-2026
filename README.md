# Introduction to version control with Git 

Welcome to the **Git & Unix workshop**! for Eindhoven University of Technology, on 18-19 November, 2026.  This repository contains instructions for the two-day hands-on workshop focused on **how to interact with the Unix terminal**, **version control with Git**, **collaborative best practices**, and **getting to know [4TU.ResearchData](data.4tu.nl)**.

[![schema.org Course](https://img.shields.io/badge/schema--org-Course-blue.svg)](./schema-course.jsonld)

**Links:**

<!-- - Mentimeter Git Intro- https://edu.nl/cma84 -->
- Collaborative notes- https://hackmd.io/W5GSXeJ_RJOE0DE0UsW5AA (FIX THIS)

## 🚀 Workshop Overview

This workshop is designed to introduce participants to **Git and version control**, helping them to:
- Set up and manage a **local and remote Git repository**.
- Track changes, collaborate, and resolve conflicts effectively.
- Use **4TU.ResearchData** repository for their research outputs.

## 📅 Schedule

| **Day** | **Time**    | **Session**                                                                                 |
| ------- | ----------- | ------------------------------------------------------------------------------------------- |
| Day 1   | 09:30–09:45 | Welcome, installation check & housekeeping                                                  |
|         | 09:45–10:30 | Introducing the Unix Shell                                                                  |
|         | 10:30–11:15 | Working with Files and Directories                                                          |
|         | 11:15–11:30 | **Break**                                                                                   |
|         | 11:30–12:00 | Pipes, Loops and Shell scripts                                                              |
|         | 12:00–13:00 | **Lunch**                                                                                   |
|         | 13:00–14:45 | Version Control with Git (Local Repositories)                                               |
|         | 14:45–15:00 | **Break**                                                                                   |
|         | 15:00–16:30 | Tracking Changes & Commit History                                                           |
|         | 16:30–End   | Wrap-up and End                                                                             |
| Day 2   | 09:30–09:45 | Recap of local Git                                                                          |
|         | 09:45–10:15 | Remotes in Git                                                                              |
|         | 10:15–10:45 | Push/Pull to GitHub                                                                         |
|         | 10:45–11:00 | **Break**                                                                                   |
|         | 11:00–12:00 | Collaboration practices                                                                     |
|         | 12:00–13:00 | **Lunch**                                                                                   |
|         | 13:00–16:00 | Getting to know 4TU.ResearchData: The repository for Natural Sciences and Engineering in NL |
|         | 16:00–16:30 | Post workshop survey                                                                        |
|         | 16:30–End   | Wrap-up and End                                                                             |


## 🛠 Prerequisites
Before attending the workshop, please ensure you have:
- A **GitHub account** ([sign up here](https://github.com/))
- Installed **Git** on your system ([installation guide](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git))
- A **terminal** or **Git Bash** (Windows users should install [Git for Windows](https://gitforwindows.org/))
- A basic understanding of Unix shell commands. See [here](https://swcarpentry.github.io/shell-novice/02-filedir.html)

### Why teach Git on the command-line (Unix shell) rather than with a GUI (Graphical User Interface)?:

- **Deep conceptual understanding** (the CLI forces you to perform each Git operation explicitly, so you see exactly how things work, whereas GUIs often bundle actions behind buttons, obscuring the underlying mechanics.)

- **Environment-agnostic skills** (the Unix-shell CLI is consistent across Linux, macOS, Windows (via WSL) and remote/headless systems(HPC servers), while each GUI client has its own interface and may not be available in all environments.)

- **Scriptability for reproducibility and automation**: (CLI commands can be composed into scripts or integrated into automated pipelines—key for reproducible research)


## 📖 Workshop Materials

- **[Unix Lesson](Lesson_development/unix.md)** : Introduction to Unix to navigate your file system , create documents , visualize data, make loops and scripts. 

- **[Git Lesson](Lesson_development/git_lesson_verbosed_structure.md)**: Introduction to Git, tracking changes, and collaborating on research projects.

- [Collaborative document](https://edu.nl/htaw9)

## Quarto slides Prerequisites
 
Rendering the slides locally requires:
 
- [Quarto](https://quarto.org/docs/get-started/)
- A recent web browser for previewing slides
 
Verify your installation:
 
```bash
quarto check
```

### Working on the slides

```bash
quarto preview unix.qmd   # live preview of one deck
quarto render                      # build everything into _site/
```

* Shared options (theme, logo, size, transitions) live in `_quarto.yml`.
* Colours, boxes and layout helpers live in `styles.scss`.
* A new deck is a new `NN-name.qmd` with only a `title` and `subtitle` in its header.
  Add it to `index.qmd`.
* Images go in `images/<deck>/`; things used by several decks go in `images/shared/`.

### Automatic build

`.github/workflows/publish.yml` renders the whole project on every push.
The rendered site is attached to the run as the `slides` artifact.
On `main` it is also published to GitHub Pages
(Settings → Pages → Source: *GitHub Actions*).


## 🔗 Resources

- [Software Carpentry Unix lesson](https://swcarpentry.github.io/shell-novice/index.html)
- [Software Carpentry Git lesson](https://swcarpentry.github.io/git-novice/index.html)
- [Git Documentation](https://git-scm.com/doc)
- [4TU.ResearchData](https://data.4tu.nl/)

## 💡 License
This workshop material is licensed under **GNU AFFERO GENERAL PUBLIC LICENSE Version 3**. Feel free to share and modify the lesson according your needs.

## 🙌 Acknowledgments
This workshop is based on the [Software Carpentry](https://software-carpentry.org/) Git curriculum.

