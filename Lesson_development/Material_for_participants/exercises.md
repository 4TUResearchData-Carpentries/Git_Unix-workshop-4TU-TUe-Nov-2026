# Challenge: Your first research project with Git

**Duration:** 25–30 minutes  
**Goal:** Create a small research project and document how it evolves using Git.

### Scenario

You are starting a new research project. As your ideas evolve, you want to keep a record of what changed, why it changed, and which files belong together.

Your mission is to create a Git repository containing **three meaningful commits**.

### Part 1 : Start your research project

1. Create a new directory called `research-diary` and initialize it as a Git repository.

   **Tip:** Make sure you have stepped outside your current `patients` repository first!

2. Create two files inside your new repository:

   - `me.txt` — Write three lines introducing yourself (or a fictional researcher), your research field, and an interesting research question.
   - `research.txt` — Write the sentence: `Science is awesome`.

3. Check the status of your repository. How does Git describe these two files?

4. Stage **only `me.txt`** and check the status again. What changed?

5. Now stage `research.txt` as well. Check the status once more.

6. Create **one commit containing both files**, using a meaningful commit message.

**Checkpoint:** How many files were included in your first commit? How can you verify this?


<details>
<summary>🔍 Click here for hints!</summary>

- Use `pwd` to check your current location.
- Use `cd ..` to navigate to the parent directory. Make sure you are outside your previous Git repository!
- Create a directory with `mkdir directory_name`.
- Navigate into it using `cd directory_name`.
- Initialize a Git repository with `git init`.
- Create or edit a file with `nano filename.txt`.
- Use `git status` to inspect the state of your repository.
- Stage a specific file with `git add filename.txt`.
- Remember: you can run `git add` multiple times before committing!
- Commit your staged changes with `git commit -m "meaningful message"`.
- Use `git show --stat HEAD` to inspect which files were included in your latest commit.

</details>


### Part 2 — Research evolves!

After some experiments, you realize science is more complicated than you initially thought.

1. Modify `research.txt`, replacing its sentence with `Science is messy`.
2. Modify one existing line in `me.txt` and add a fourth line describing something new you have learned.
3. Before staging anything, inspect the differences between your working files and the last commit.

   **Question:** Can you identify the deleted, modified, and added lines?

4. Stage **only `me.txt`**.

5. Now investigate your repository using:

   - `git status`
   - `git diff`
   - `git diff --staged`

   **Think before continuing:**
   - Which changes are staged?
   - Which changes are still unstaged?
   - If you committed now, would both files be included? Why?

6. Stage your remaining changes and review what will be included in the next commit.
7. Create **one commit containing the changes to both files**.

**Checkpoint:** How can you confirm that both files were included in your second commit?


<details>
<summary>🔍 Click here for hints!</summary>

- Open an existing file for editing with `nano filename.txt`.
- Use `git status` to identify modified and staged files.
- Use `git diff` to compare unstaged changes with the staging area.
- Stage one file at a time using `git add filename.txt`.
- Use `git diff --staged` to inspect changes already staged for the next commit.
- Run `git diff` and `git diff --staged` after staging only one of your modified files. Notice the difference!
- You can stage multiple files before making a single commit.
- Commit your staged changes with `git commit -m "meaningful message"`.
- Use `git log -1 --stat` to see which files were included in your latest commit.

</details>


### Part 3 — Not everything belongs in Git!

Your research project is growing, and you need a place to store raw experimental data.

1. Create a directory called `raw-data`.
2. Run `git status`.

   **Surprise!** Does Git recognize your new directory? Why or why not?

3. Inside `raw-data`, create a file called `observations.csv`, containing:

   `sample,value`  
   `A,42`  
   `B,37`

4. Check `git status` again. What changed?
5. Imagine these raw data files are too large or sensitive to store in your Git repository. Configure Git to ignore the entire `raw-data` directory.
6. Verify that Git is ignoring the files as intended.
7. Stage and commit your `.gitignore` file.

**Checkpoint:** Is your `raw-data` directory still on your computer? Is its content tracked by Git?


<details>
<summary>🔍 Click here for hints!</summary>

- Create a directory with `mkdir directory_name`.
- Create a file inside a directory using `nano directory_name/filename.csv`.
- Use `git status` to inspect untracked files.
- Remember: Git tracks files, not empty directories.
- To ignore files or directories, create a file called `.gitignore` in your repository.
- Open it using `nano .gitignore`.
- Add `raw-data/` to `.gitignore` to ignore the directory and its contents.
- Use `git status` to check whether Git still reports the raw data files as untracked.
- Stage and commit your `.gitignore` file.

</details>


### Part 4 — Explore your project's history

You should now have **exactly three commits**.

1. Display the history of your repository, starting with the most recent commit.
2. Find a way to display the history in a compact format, showing one line per commit.
3. Verify that your working directory is clean.
4. Identify which files Git is currently tracking.

**Final reflection:** Can you identify which commit introduced each change, and explain why grouping related changes into meaningful commits is useful?


<details>
<summary>🔍 Click here for hints!</summary>

- Display the full history with `git log`.
- Use `git log --oneline` for a compact history.
- Each commit has a unique identifier (hash) and a commit message.
- Use `git show COMMIT_HASH` to inspect the changes introduced by a particular commit.
- Use `git show --stat COMMIT_HASH` to see which files were changed in a commit.
- Use `git status` to check whether your working directory is clean.
- Use `git ls-files` to display the files Git currently tracks.
- Press `q` to exit the history viewer if necessary.

</details>




## 2 GitHub GUI 

- Browse to your `recipes` repository on GitHub.
- Under the Code tab, find and click on the text that says “XX commits” (where “XX” is some number). You should see the history log.
- Click on, the **three buttons** to the right of each commit.
- What information can you gather/explore from these buttons?
- How would you get that same information in the shell? 


## Assignment: Collaboration practices


**Assignment:**

1. Write an Issue in your `patients-analysis` repo. Options:

   * Add a multiplication function
   * Improve `calculate_mean` with full documentation
   * Create a `README.md` file

2. Pair up:

   * Clone or fork each other’s repositories. (Instructor can decide which teams clone and which fork, then we should compare the two approaches and discuss the pros and cons of each.)
   * Create a branch, solve the issue.
   * Open a Pull Request with your changes.

3. Review and integrate PRs if possible.

4. Reflect:

   * What worked well?
   * What was confusing?
   * Did you encounter merge conflicts?
   * How would you improve the process next time?
