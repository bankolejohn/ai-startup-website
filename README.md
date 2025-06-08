# ai-startup-website
first repo for 3mtt devops course

# Hands-On Git Project: Collaborative Website Development with Git and GitHub

## Introduction

This project provides a step-by-step guide to simulating a collaborative development workflow using Git and GitHub. By playing the roles of two developers, Tom and Jerry, you will learn the essential Git commands for creating and managing a simple website project. This hands-on tutorial covers setting up a repository, creating branches for new features, making and committing changes, and pushing those changes to a remote repository.

### Target Audience

This documentation is intended for beginners who are new to Git and GitHub and want to understand the fundamental concepts of version control and collaborative development.

### Learning Objectives

By the end of this project, you will be able to:

* Install and configure Git.
* Create a new repository on GitHub.
* Clone a remote repository to your local machine.
* Create, switch between, and manage branches.
* Stage and commit changes to your local repository.
* Push changes from your local repository to GitHub.
* Simulate a collaborative workflow with multiple branches.

## Prerequisites

Before you begin, ensure you have the following:

* **Git:** A free and open-source distributed version control system.
* **A GitHub Account:** A web-based platform for version control and collaboration.

## Part 1: Setup and Initial Configuration

This section will guide you through the initial setup of your project, including installing Git, creating a GitHub repository, and cloning it to your local machine.

### 1.1 Install Git

Visit the [official Git website](https://git-scm.com/) to download and install the latest version of Git for your operating system. Follow the on-screen instructions to complete the installation.

### 1.2 Create a GitHub Repository

1.  **Sign up or log in** to your [GitHub](https://github.com/) account.
2.  Click the **"+"** icon in the top-right corner of the page and select **"New repository"**.
3.  **Name your repository:** For this project, use `ai-startup-website`.
4.  **Initialize the repository with a README file:** Check the box that says "Add a README file."
5.  Click **"Create repository"**.

### 1.3 Clone the Repository

1.  On your new repository's page on GitHub, click the green **"< > Code"** button.
2.  Copy the **HTTPS URL** provided.
3.  Open your terminal or command prompt.
4.  Create a dedicated folder for your projects and navigate into it. For example:
    ```bash
    mkdir -p Desktop/darey-training/git-project
    cd Desktop/darey-training/git-project
    ```
5.  Clone the repository from GitHub to your local machine using the `git clone` command, followed by the URL you copied:
    ```bash
    git clone <YOUR_REPOSITORY_URL>
    ```
    Replace `<YOUR_REPOSITORY_URL>` with the actual URL.

### 1.4 Initial Commit

1.  Navigate into your newly cloned repository:
    ```bash
    cd ai-startup-website
    ```
2.  Create an `index.html` file. You can do this using the `touch` command:
    ```bash
    touch index.html
    ```
3.  Open the `index.html` file in a text editor and add the following content:
    ```html
    This is the Admin creating an index.html file for Tom and Jerry.
    ```
4.  Check the status of your repository. You will see that `index.html` is an untracked file.
    ```bash
    git status
    ```
5.  Stage the `index.html` file for the next commit. This tells Git you want to include this file in the next snapshot of your project.
    ```bash
    git add index.html
    ```
6.  Check the status again. The file will now be listed under "Changes to be committed" and its name will appear in green.
    ```bash
    git status
    ```
7.  Commit the staged changes to your local repository's history with a descriptive message.
    ```bash
    git commit -m "This is my first commit"
    ```
8.  Push the commit from your local `main` branch to the `origin` (your GitHub repository).
    ```bash
    git push origin main
    ```

## Part 2: Simulating Tom and Jerry's Work

In this part, you'll simulate a collaborative workflow by creating separate branches for two developers, Tom and Jerry.

### 2.1 Tom's Work: Updating the Navigation

<img width="785" alt="Snipaste_2025-06-08_18-51-29" src="https://github.com/user-attachments/assets/45ba9779-66ae-45df-b03b-b5ab9a69b490" />


1.  **Navigate to the project directory** if you are not already there:
    ```bash
    cd ai-startup-website
    ```
2.  **Check the current branch.** You should be on the `main` branch.
    ```bash
    git branch
    ```
3.  **Create and switch to a new branch** for Tom's work. This branch will be for adding a navigation bar to the website.
    ```bash
    git checkout -b update-navigation
    ```
4.  **Verify that you are on the new branch.** The `update-navigation` branch will have an asterisk next to it.
    ```bash
    git branch
    ```
5.  **Modify the `index.html` file.** Open the file and replace its content with the following:
    ```html
    This is Tom adding Navigation to the AI-website
    ```
6.  **Check the status** to see the modified file.
    ```bash
    git status
    ```
7.  **Stage the changes:**
    ```bash
    git add index.html
    ```
8.  **Commit the changes** with a meaningful message:
    ```bash
    git commit -m "Update navigation bar"
    ```
9.  **Push Tom's branch to GitHub:**
    ```bash
    git push origin update-navigation
    ```

### 2.2 Jerry's Work: Adding Contact Information

1.  **Switch back to the `main` branch.** This ensures that Jerry's work starts from the original project state, independent of Tom's changes.
    ```bash
    git checkout main
    ```
2.  **Pull the latest changes from the remote repository.** This step is a good practice to ensure your main branch is up-to-date. *Note: In this specific simulation, there are no new changes to pull to `main` at this point, but in a real-world scenario, this is a crucial step.*
    ```bash
    git pull origin main
    ```
3.  **Create and switch to a new branch** for Jerry's work.
    ```bash
    git checkout -b add-contact-info
    ```
4.  **Modify the `index.html` file.** Open the `index.html` file. Notice it has the original content. Replace it with the following:
    ```html
    This is Jerry adding contact information.
    ```
5.  **Stage the changes:**
    ```bash
    git add index.html
    ```
6.  **Commit the changes** with a descriptive message:
    ```bash
    git commit -m "Add contact information"
    ```
7.  **Push Jerry's branch to GitHub:**
    ```bash
    git push origin add-contact-info
    ```

## Part 3: Merging the Work (On GitHub)

After Tom and Jerry have pushed their branches to GitHub, the next step in a real-world project would be to merge these changes into the `main` branch. This is typically done through a **Pull Request**.

### 3.1 Creating a Pull Request for Tom's Branch

1.  Go to your `ai-startup-website` repository on GitHub.
2.  You will see a notification that a new branch (`update-navigation`) has been pushed. Click the **"Compare & pull request"** button.
3.  Give the pull request a title (e.g., "Feature: Update Navigation Bar") and a brief description of the changes.
4.  Click **"Create pull request"**.
5.  On the next page, you would typically have a team member review your changes. For this project, you can merge it yourself. Click **"Merge pull request"** and then **"Confirm merge"**.
6.  You can now safely delete the `update-navigation` branch on GitHub.

### 3.2 Creating a Pull Request for Jerry's Branch

1.  Go back to the main page of your repository on GitHub.
2.  Click on the **"Pull requests"** tab and then click the **"New pull request"** button.
3.  For the `base` branch, select `main`. For the `compare` branch, select `add-contact-info`.
4.  You will notice that GitHub detects a **merge conflict**. This is because both Tom and Jerry edited the same lines in `index.html`.
5.  **Resolving the Conflict:**
    * Click the **"Resolve conflicts"** button.
    * GitHub will show you the conflicting code. You need to manually edit the file to decide what the final version should look like. For example, you might decide to keep both changes:
        ```html
        This is Tom adding Navigation to the AI-website
        This is Jerry adding contact information.
        ```
    * Once you have resolved the conflict, click **"Mark as resolved"** and then **"Commit merge"**.
6.  Now you can proceed to **"Merge pull request"** and **"Confirm merge"**.

## Conclusion

Congratulations! You have successfully simulated a collaborative Git workflow. You have learned how to:

* Set up a local and remote Git repository.
* Use branches to work on features in isolation.
* Stage, commit, and push your changes.
* Understand and resolve merge conflicts, a common occurrence in collaborative projects.

This project provides a solid foundation for using Git and GitHub in real-world development environments.

## Glossary of Git Terms

* **Repository (Repo):** A directory where your project's files and their revision history are stored.
* **Clone:** To create a local copy of a remote repository.
* **Branch:** A parallel version of a repository. It allows you to work on different features without affecting the main codebase.
* **`main` branch:** The default branch in a repository. It is considered the definitive version of the project.
* **`git add`:** The command to stage changes, preparing them to be committed.
* **`git commit`:** The command to save your staged changes to the local repository's history.
* **`git push`:** The command to upload your committed changes to a remote repository.
* **`git pull`:** The command to fetch and download content from a remote repository and immediately update the local repository to match that content.
* **`git checkout`:** The command to switch between different branches.
* **Merge:** The process of combining the changes from different branches.
* **Pull Request (PR):** A request to merge the changes from one branch into another, allowing for code review and discussion before merging.
* **Merge Conflict:** An event that occurs when Git is unable to automatically resolve differences in code between two commits.


<img width="624" alt="Screenshot 2025-06-03 at 11 28 36 AM" src="https://github.com/user-attachments/assets/484dbdf9-d674-4de6-a2ee-e79b795f29b5" />

## Screenshots

### Repository

<img width="933" alt="Snipaste_repo" src="https://github.com/user-attachments/assets/1133ec1e-de26-4738-b92a-eb6d99809130" />



<img width="698" alt="Screenshot 2025-06-03 at 11 31 44 AM" src="https://github.com/user-attachments/assets/4c95909d-ce95-43a7-9a6a-0b0250ce585c" />
