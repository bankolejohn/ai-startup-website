# Merging Changes in a Collaborative Git Project

## 📌 Overview
This guide explains how to merge changes from multiple contributors (e.g., Tom and Jerry) into the `main` branch using **Pull Requests (PRs)**. It covers:
- Creating and reviewing PRs.
- Updating branches to avoid conflicts.
- Best practices for collaborative Git workflows.

---

## 🚀 Workflow Summary
1. **Developers push changes** to their branches (e.g., `update-navigation` and `add-contact-info`).
2. **Pull Requests (PRs)** are opened for review.
3. **Team reviews** and approves changes.
4. **PRs are merged** into `main`.
5. **Branches are synced** with `main` to prevent conflicts.

---

## 🔧 Step-by-Step Guide

### 1️⃣ Creating a Pull Request (PR)
#### For Tom’s Branch (`update-navigation`)
1. **Navigate to the GitHub repo** → Branch dropdown → Select `update-navigation`.
2. Click **"New pull request"**.
3. Set:
   - **Base branch**: `main` (target).
   - **Compare branch**: `update-navigation` (source).
4. **Review changes** in the diff view.
5. Add a **title** (e.g., "Update navigation menu") and **description**.
6. Click **"Create pull request"**.

#### For Jerry’s Branch (`add-contact-info`)
- Repeat the same steps for `add-contact-info`.

---

### 2️⃣ Reviewing & Merging a PR
1. **Team members review**:
   - Comment on code.
   - Request changes (if needed).
   - Approve the PR.
2. **Resolve discussions** (update branch if requested).
3. **Merge the PR**:
   - Click **"Merge pull request"**.
   - Choose a merge strategy (e.g., "Create a merge commit").
4. **Delete the branch** (optional but recommended).

---

### 3️⃣ Updating a Branch Before Merging
If `main` has new changes (e.g., after Tom’s PR was merged), Jerry must update his branch:

#### Locally:
```bash
git checkout add-contact-info       # Switch to Jerry’s branch
git pull origin main               # Merge latest `main` changes
git push origin add-contact-info   # Push updated branch

---

#### screenshots

<img width="440" alt="Snipaste_2025-06-27_11-09-46" src="https://github.com/user-attachments/assets/d1e5be62-45d7-4003-8d80-f78baa8d5358" />

<img width="875" alt="Snipaste_2025-06-27_11-55-17" src="https://github.com/user-attachments/assets/1b7d8220-7aa0-4ee8-b434-71e9ec825cb5" />


<img width="950" alt="Snipaste_2025-06-27_11-57-38" src="https://github.com/user-attachments/assets/a8a37239-896e-4064-b0fc-16d89093f6ad" />

<img width="610" alt="Screenshot 2025-04-30 at 4 47 17 PM" src="https://github.com/user-attachments/assets/1d78651f-5d40-427e-9542-64b86cdd4a61" />
