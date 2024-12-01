![image](https://github.com/user-attachments/assets/a6fdd769-7fa2-4491-b04d-b06bc5f5a0b4)


# SYSADM1 -- Git Basics

Answer the following research questions about Git, GitLab desktop and
GitHub.

1.  What is Git, and why is it important in software development?

Git is a DevOps tool for source code management. It is a free and
open-source version control system used to efficiently handle small to
very large projects. Git tracks changes in the source code, enabling
multiple developers to work together on non-linear development.

2.  How does Git track changes in a project?

Git tracks change using snapshots of the project files. Every time you
commit changes, Git creates a snapshot of the files and records this
snapshot along with metadata (such as a commit message, author, and
timestamp). Git uses structured data called a commit to store these
snapshots in a tree-like structure. Each commit points to its parent
commit, forming a history of change and allowing developers to view,
compare, and revert changes over time.

3.  What is the difference between a local repository and a remote
    repository in Git?

A remote repository is hosted on a server (either online, off-site or on
the same machine in a different location) and is shared by multiple team
members. A local repository, on the other hand, is stored on an
individual\'s local machine.

4.  What are the basic Git commands?

-   Git init

-   Git clone

-   Git add

-   Git commit

-   Git status

-   Git push

-   Git pull

-   Git branch

-   Git merge

-   Git log

5.  How do you check the status of a Git repository?

You can check the status of a Git repository with the 'git status'
command. It shows which changes are staged, which are not, and which
files are untracked by Git.

6.  What is the purpose of branches in Git, and how do you create and
    switch between them?

In Git, branches are an essential part of the development workflow. A
branch acts as a pointer to a snapshot of your changes. Whenever you
want to add a new feature or fix a bug---regardless of size---you create
a new branch to isolate your work.

When creating a new branch, you first use the command git branch
\[branch-name\], and then switch to that branch with git checkout
\[branch-name\]. Alternatively, you can combine both actions by using
the command git checkout -b \[branch-name\].

7.  What are GitLab Desktop and GitHub, and how are they different from
    Git?

Despite their similar names, GitHub and GitLab are owned by different
companies---GitHub by Microsoft and GitLab by the GitLab Inc.
organization. Both platforms provide spaces for developers to manage Git
repositories, collaborate, and share their work. Git, GitHub, and GitLab
together to streamline the software development process, each offering
distinct features. GitHub is widely known for supporting open-source
projects and community collaboration, while GitLab distinguishes itself
as an all-in-one DevOps platform with built-in CI/CD pipelines and
robust security features.

8.  How do you connect a local Git repository to a GitLab or GitHub
    repository?

To connect a local Git repository to a remote repository on GitLab or
GitHub, start by initializing the local repository with the command 'git
init'. Next, add the remote URL using 'git remote add origin
\[repository-URL\]'. Finally, push your local changes to the remote
repository with 'git push -u origin master'.

9.  What are the steps to collaborate with others using GitLab or
    GitHub?

To collaborate with others using GitLab or GitHub, start by cloning the
remote repository to your local machine with the command 'git clone
\[repository-URL\]'. Then, create a new branch for your work using 'git
checkout -b \[new-branch-name\]'. Afterward, make the necessary changes
by modifying or adding files. Once you\'ve made your changes, stage them
with 'git add \[file-name\]' and commit the changes using 'git commit -m
\"Commit message\"'. Next, push your changes to the remote repository
with 'git push origin \[branch-name\]'. After pushing, open a pull
request (on GitHub) or a merge request (on GitLab) to propose your
changes for review. Finally, once the changes have been reviewed, they
can be merged into the main branch.

10. How do you resolve merge conflicts in Git?

To resolve merge conflicts in Git, start by identifying the conflicted
files using git status. Next, open the conflicting files and manually
resolve the differences. Once the conflicts are resolved, stage the
files using git add \[file-name\]. Then, commit the changes with git
commit to finalize the merge. Finally, push the resolved changes to the
remote repository using git push origin \[branch-name\].

11. What is a pull request, and why is it used in GitHub?

A pull request is a proposal to merge changes from one branch into
another. It allows collaborators to review, discuss, and approve the
changes before they are merged into the main codebase.

12. What are some best practices for writing commit messages?

-   Be clear and descriptive: Summarize what the commit does in a
    concise, informative way.

-   Use the Imperative Mood: Write commit messages as commands, not past
    tense.

-   Keep It Short and Focused: The subject line should be under 50
    characters. If necessary, use the body of the message to explain why
    the change was made.

-   Use Bullet Points for Multiple Changes: If the commit includes
    several changes, list them clearly with bullet points or separate
    lines.

-   Reference Issues: If the commit addresses a specific issue, mention
    the issue number in the message.
