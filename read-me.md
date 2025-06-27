# A Guide to Collaborative Git Workflow using Pull Requests

This document outlines the standard process for contributing to this project using a feature-branch and Pull Request (PR) workflow in Git and GitHub. Following these steps ensures that all changes are reviewed, potential conflicts are managed, and the `main` branch remains stable.

---

## 📖 Table of Contents

- [Understanding the Workflow](#-understanding-the-workflow)
- [Part 1: Creating a Pull Request (First Contributor)](#-part-1-creating-a-pull-request-first-contributor)
- [Part 2: Reviewing and Merging the Pull Request](#-part-2-reviewing-and-merging-the-pull-request)
- [Part 3: Updating and Merging Concurrent Work (Second Contributor)](#-part-3-updating-and-merging-concurrent-work-second-contributor)

---

### 🌐 Understanding the Workflow

A **Pull Request (PR)** is a feature on GitHub that allows you to notify team members about changes you've pushed to a specific branch in a repository. It is a formal request to review your work and merge it into the main project (`main` branch). This process is central to collaborative development, as it provides a platform for discussion and review before any changes are integrated.

The general process involves:
1.  Creating a feature branch for your work.
2.  Pushing your completed work to that branch on GitHub.
3.  Creating a Pull Request to merge your feature branch into the `main` branch.
4.  Reviewing the changes with the team.
5.  Merging the Pull Request into the `main` branch.

---

### Part 1: Creating a Pull Request (First Contributor)

Let's walk through an example. A developer, **Tom**, has been assigned a task and is working on a branch named `update-navigation`. Once his work is complete, he needs to create a pull request.

**1. Navigate to Your GitHub Repository:**
   - Open your web browser and go to the GitHub page for the project.

**2. Switch to Your Branch:**
   - If you've recently pushed your branch, GitHub will often show a yellow banner with a "Compare & pull request" button. You can click this.
   - Alternatively, use the branch dropdown menu (usually says `main`) to select your branch, in this case, `update-navigation`.
<img width="440" alt="Snipaste_2025-06-27_11-09-46" src="https://github.com/user-attachments/assets/28d58bee-7861-40ff-830a-ed1ce5191726" />


**3. Initiate the Pull Request:**
   - Click the **"New pull request"** or **"Compare & pull request"** button.
   - GitHub will take you to a new page to open a pull request. It will automatically set the `base` branch to `main` and the `compare` branch to yours (`update-navigation`).

<img width="326" alt="Snipaste_2025-06-27_11-56-06" src="https://github.com/user-attachments/assets/902f7f94-1e2d-48fa-8127-595652ceb3ae" />

**4. Review Your Changes:**
   - Before submitting, carefully review the changes displayed on the screen. GitHub shows a "diff" (the differences) between the `main` branch and your branch. This is a great opportunity to double-check your work for any mistakes.

**5. Create the Pull Request:**
   - If everything looks correct, click the **"Create pull request"** button.
   - Provide a concise and descriptive **title**.
   - Write a clear **description** explaining what changes you made and why they are needed.
   - Click **"Create pull request"** again to officially open it.

---

### Part 2: Reviewing and Merging the Pull Request

Once Tom's pull request is created, it becomes visible to the team.
- **Code Review:** Other team members can now review the changes, leave comments with feedback, and request modifications if necessary. This is a key part of our collaborative process.
- **Merging:** When the team agrees that the changes are ready, a team member with merge permissions will click the **"Merge pull request"** button. This action incorporates the changes from Tom's `update-navigation` branch into the `main` branch, completing the cycle for his feature.

---

### Part 3: Updating and Merging Concurrent Work (Second Contributor)

While Tom was working, another developer, **Jerry**, was working on a different feature in his `add-contact-info` branch. Now that Tom's changes are in the `main` branch, it is essential for Jerry to update his branch *before* creating his own pull request. This ensures compatibility and reduces the chance of merge conflicts.

**1. Switch to Your Local Branch:**
   - On the command line, Jerry first ensures he is on his feature branch:
     ```bash
     git checkout add-contact-info
     ```

**2. Pull the Latest Changes from the `main` Branch:**
   - This command fetches the latest version of the `main` branch (which now includes Tom's changes) from the remote repository (`origin`) and merges it into Jerry's local `add-contact-info` branch.
     ```bash
     git pull origin main
     ```
   - **Purpose:** This step is crucial for ensuring that any updates made to the main project are included in Jerry's work. It helps avoid conflicts and ensures his feature integrates smoothly.

**3. Push the Updated Branch to GitHub:**
   - If there were no conflicts from the pull, Jerry's local branch is now up-to-date. He needs to push this updated branch to GitHub.
     ```bash
     git push origin add-contact-info
     ```
   - This command uploads Jerry's changes, which now reflect both his own work and the latest updates from the `main` branch.

**4. Create and Merge Jerry's Pull Request:**
   - Jerry can now follow the same steps as Tom (in Part 1) to create a pull request for his `add-contact-info` branch.
   - Once the PR is reviewed and approved, it can be safely merged into the `main` branch.
