*Building a Version-Controlled DevOps Project with Git*

The objective is to manage a DevOps project using Git best practices, utilizing Git for version control, and GitHub for hosting the project. This will involve setting up Git, creating appropriate branches, managing commits, using pull requests, and documenting the project tasks. Below is a step-by-step guide to building and managing the project.

---

*Objective:*
- Used *Git* for version control.
- Used *GitHub* as a hosting platform.

*Tools:*
- *Git*:  used for local version control.
- *GitHub*:  used for remote repository hosting.
- *Text editor(Sublime Text)

---

*Step-by-Step i used to complete this task*

---

Firstly Launch an ec2 instance with following steps

==>Log into the AWS Management Console
==>Navigate to EC2 Dashboard
==>Launch a New EC2 Instance
==>Choose an Amazon Machine Image (AMI)
==>Choose an Instance Type
==>choose t2.micro instance (1 vCPU, 1 GB RAM)
==>configure security group
==>select key pair
==>launch an instance to use

*Step 1: Setting Up Git*

1. *Installed Git*:
   - used command **yum install git -y**
   
2. *Configured Git* (initial setup):
   - Open command prompt and configured my username and email for Git commits.
     ```bash
     git config --global user.name "Bharath"
     git config --global user.email bharaththokala5806@gmail.com"
     ```
3. *Created a Project Directory*:
   -  Also In terminal created a new directory for my task
     ```bash
     mkdir my-devOps-task4
     cd my-devOps-task4
     ```
4.*Initialized Git Repository*:
   - Initialized a new Git repository in the directory.
     ```bash
     git init
     ```
5.*Created `.gitignore` File*:
   - This file specifies which files Git should ignore.
     ```bash
     touch .gitignore
     ```
6.*Created README.md File*
  -Logged to GitHub(https://github.com/) and created a new repository (named it `devOps-task4`).

7.*Linked Local Repo to GitHub*:
   - Copied the GitHub repository URL (HTTPS).
   - In terminal, runned the  commands to link my local Git repo to GitHub:
     ```bash
     git remote add origin https://github.com/Bharath5806/devOps-task4.git
     git branch -M main
     git push -u origin main
     ```
 8.Setted Up Git Branching*

1. *Created the `dev` Branch*:
   - The `dev` branch will be used for ongoing development and feature integration.
   ```bash
   git checkout -b dev
   git push -u origin dev
   ```

2. *Created a `feature` Branch*:
   - Feature branches will be created for implementing new features.
   - I added a feature (`authentication`):
     ```bash
     git checkout -b feature/authentication
     git push -u origin feature/authentication
     ```

3. *Merged Feature Branch into `dev`*:
   - After completing a feature, merged it into the `dev` branch.
   ```bash
   git checkout dev
   git merge feature/authentication
   git push origin dev
   ```

4. *Created the `main` Branch*:
   - `main` is the stable branch that contains production-ready code.

9 Merged the `dev` branch into `main` when you are ready for release.
      ```bash
     git checkout main
     git merge dev
     git push origin main
     ```
     
10. Used Pull Requests (PRs)*

*Created a Pull Request for Merging*:
   - On *GitHub*, created a Pull Request (PR) to merge a feature branch into the `dev` branch.
     - Go to the GitHub repository.
     - Click on "Pull Requests" > "New Pull Request."
     - Select the feature branch and the `dev` branch for merging.
Verification

To verify the setup:

Clone the repository:
```bash
git clone https://github.com/Bharath5806/devOps-task4.git
```
Check branches:
```bash
git branch -a
```
*Conclusion*

By following these steps, i have created a version-controlled DevOps project using *Git* and *GitHub*. This workflow ensures a smooth collaboration process and allows easy tracking of tasks and releases through proper version control and documentation.
