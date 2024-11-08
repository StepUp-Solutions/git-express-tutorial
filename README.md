# An express start guide for Git

A quick ToThePoint guide covering the core and advanced concepts and typical examples on how to use Git using a graphical interface (GUI).
The recommended software is Git Extensions. TortoiseGit and Gittyup are good alternatives, a more modern alternative can be RelaGit. All of them are (obviously) open-source.
Most software already include a minimalist Git interface ofthen called Source Control (Vs Code, Node-RED, Git for Kicad, ...).
But you should understand those core concepts before using it.
This guide is written for Git beginners and covers all the essentials topics.

## 1. Core concepts

### Repositories (Repo)

* **What:** A Git Repository (Repo) is the central location where all your project's files, history, and metadata are stored.
* **Why:** Having a single source of truth enables collaboration, version control, and tracking of changes.
* **Analogy:** Think of a repository as a project's file cabinet, where all documents (files) are kept, and every action (change) is recorded.

**Setting up a Repository with your Git GUI:**

1. Create a new folder for your project.
2. Open your Git GUI and click on "Create new repository."
3. Select the project folder and initialize the repository.

### Commits

* **What:** A Commit is a snapshot of your project's files at a particular point in time, accompanied by a descriptive message.
* **Why:** Commits allow you to track changes, identify who made modifications, and revert to previous states if needed.
* **Analogy:** Think of a commit as saving a document; you're capturing its current state, with a note (commit message) explaining what changed.

**Components of a Commit:**

* **Staged Changes:** Selected files to be included in the commit.
* **Commit Message:** A brief description of the changes made.
* **Author:** The person making the commit (you).

**Committing Changes with your Git GUI:**

1. Make changes to files in your project folder.
2. Open your Git GUI and navigate to the "Commit" tab.
3. Review the changes in the "Unstaged changes" area.
4. Select the files you want to commit and click "Stage selected files."
5. Enter a meaningful commit message and click "Commit."

### Branching

* **What:** A Branch is an independent line of development in your repository, allowing parallel work without disrupting the main project.
* **Why:** Branches enable feature development, testing, and experimentation without risking the stable main branch.
* **Analogy:** Think of branches as separate workbenches; you can build and test a new feature (branch) without affecting the main production line (main branch).

**Key Branching Concepts:**

* **Main Branch (Master/Main):** The primary, stable branch.
* **Feature Branch:** A secondary branch for developing new features or fixes.

**Creating and Managing Branches with your Git GUI:**

1. To create a new branch, click on "Branch" in your Git GUI and select "Create new branch."
2. Provide a branch name and select the base branch (usually "master" or "main").
3. Make changes and commit them to the new branch.
4. To merge the branch back into the main branch, switch to the main branch and click "Merge."

### Remote Repositories

* **What:** A Remote Repository is a copy of your repository hosted on an external server (e.g., GitHub, GitLab), enabling collaboration and backup.
* **Why:** Remote repositories facilitate teamwork, provide a backup, and offer additional features (e.g., issue tracking, pull requests).
* **Analogy:** Think of a remote repository as a cloud-based file cabinet; it's an identical copy of your local repository, accessible to others.

**Connecting to a Remote Repository with your Git GUI:**

1. Click on "Remote" in your Git GUI and select "Add remote repository."
2. Enter the remote repository URL and click "Save."
3. To push your changes to the remote repository, click "Push" and select the remote repository.
4. To pull changes from the remote repository, click "Pull" and select the remote repository.

### Conflicts and Merging

* **What:** Conflicts occur when changes from different branches or collaborators clash. Merging resolves these conflicts by combining the changes.
* **Why:** Merging enables the integration of changes from various sources, ensuring the repository remains up-to-date.
* **Analogy:** Think of conflicts as overlapping puzzle pieces; merging helps you find the correct fit.

**Resolving Conflicts with your Git GUI:**

1. When a conflict occurs, your Git GUI will highlight the conflicting files.
2. Open the conflicting files and look for conflict markers (<<<<<<<, =======, >>>>>>>).
3. Resolve the conflicts by choosing the appropriate changes and removing the conflict markers.
4. Stage the resolved files and commit the changes.

**Continuing the Crash Course: Git for Technical Professionals (Using your Git GUI)**

### Git Status and File States

* **What:** Git Status shows the current state of your repository, including file changes and branch information. File States indicate the status of individual files (e.g., tracked, modified, staged).
* **Why:** Understanding Git Status and File States helps you navigate your repository, identify changes, and prepare for commits.
* **Analogy:** Think of Git Status as a dashboard for your repository, and File States as labels on files indicating their current lifecycle stage.

**Common File States:**

* **Tracked:** Files already in the repository, being monitored for changes.
* **Untracked:** New files not yet added to the repository.
* **Modified:** Tracked files with local changes.
* **Staged:** Modified files selected for the next commit.

**Viewing Git Status and File States with your Git GUI:**

1. Open your Git GUI and navigate to the "Status" tab.
2. Review the repository overview, including branch information and file changes.
3. Expand the "Unstaged changes" and "Staged changes" sections to view file states.

### Git Log and Commit History

* **What:** Git Log displays a record of all commits made to the repository, showing changes, authors, and timestamps. Commit History allows you to navigate and inspect past commits.
* **Why:** Exploring Git Log and Commit History helps you understand project evolution, identify who made changes, and revert to previous states if needed.
* **Analogy:** Think of Git Log as a version control diary, and Commit History as a time machine for your repository.

**Key Git Log Features:**

* **Commit Hash:** A unique identifier for each commit.
* **Author and Timestamp:** Information about who made the commit and when.
* **Commit Message:** A brief description of the changes made.

**Viewing Git Log and Commit History with your Git GUI:**

1. Open your Git GUI and navigate to the "Log" tab.
2. Browse the commit history, using the commit hash to identify specific commits.
3. Double-click on a commit to view detailed changes and file modifications.

### Git Reset and Revert

* **What:** Git Reset updates the current branch to a specified commit, optionally discarding changes. Git Revert creates a new commit that undoes changes from a previous commit.
* **Why:** Using Git Reset and Revert helps you correct mistakes, remove unwanted changes, or revert to a previous project state.
* **Analogy:** Think of Git Reset as a "rewind" button, and Git Revert as an "undo" feature for your repository.

**Key Differences:**

* **Git Reset:** Updates the branch pointer, potentially discarding changes.
* **Git Revert:** Creates a new commit, preserving the commit history.

**Using Git Reset and Revert with your Git GUI:**

1. **Reset:**
   * Navigate to the "Log" tab and find the desired commit.
   * Right-click on the commit and select "Reset current branch to this commit."
   * Choose the reset type (e.g., "Soft" to preserve changes).
2. **Revert:**
   * Navigate to the "Log" tab and find the commit to revert.
   * Right-click on the commit and select "Revert commit."
   * Review the changes and commit the revert.

### Git Stash and Temporary Changes

* **What:** Git Stash temporarily saves unresolved changes, allowing you to switch branches or work on other tasks without committing incomplete work.
* **Why:** Using Git Stash helps you manage unfinished changes, avoid mixing work, and maintain a clean repository.
* **Analogy:** Think of Git Stash as a temporary shelf for your work-in-progress.

**Using Git Stash with your Git GUI:**

1. Make changes to your files, but don't commit them.
2. Open your Git GUI and navigate to the "Stash" tab.
3. Click "Stash changes" to save the temporary changes.
4. Switch branches or work on other tasks.
5. To reapply the stashed changes, click "Apply stash" and select the desired stash.

### Git Tags and Releases

* **What:** Git Tags create bookmarks for specific commits, often used to mark releases, versions, or milestones. Releases are a way to package and distribute your project's software.
* **Why:** Using Git Tags and Releases helps you identify key project milestones, facilitate collaboration, and provide a clear changelog for users.
* **Analogy:** Think of Git Tags as ribbons on a timeline, highlighting important events, and Releases as nicely wrapped packages for your project's deliverables.

**Types of Tags:**

* **Lightweight Tags:** Simple bookmarks for a commit.
* **Annotated Tags:** Include additional metadata, like author and message.

**Creating and Managing Tags with your Git GUI:**

1. Navigate to the "Log" tab and find the commit to tag.
2. Right-click on the commit and select "Create tag".
3. Choose the tag type (Lightweight or Annotated) and enter the tag name and optional message.

### Git Push and Pull

* **What:**
  + **Git Push:** Uploads local changes to a remote repository.
  + **Git Pull:** Downloads changes from a remote repository and integrates them into your local copy.
* **Why:** Using Push and Pull enables collaboration, ensures repository consistency, and facilitates backup.

**Push and Pull Workflow:**

1. **Push:**
   * Make local changes and commit them.
   * Push the updated branch to the remote repository using "Push".
2. **Pull:**
   * Ensure your local copy is up-to-date by pulling changes from the remote repository using "Pull".
   * Resolve any conflicts that arise during the pull process.

**Using Push and Pull with your Git GUI:**

1. **Push:**
   * Navigate to the "Repository" tab.
   * Click "Push" and select the branch to push.
   * Choose the remote repository and click "Push".
2. **Pull:**
   * Navigate to the "Repository" tab.
   * Click "Pull" and select the branch to pull.
   * Choose the remote repository and click "Pull".

### Git Fetch and Remote Branches

* **What:**
  + **Git Fetch:** Downloads changes from a remote repository without integrating them into your local copy.
  + **Remote Branches:** Branches that exist on a remote repository, which can be tracked locally.
* **Why:** Using Fetch and understanding Remote Branches helps you:
  + Stay up-to-date with remote repository changes without modifying your local copy.
  + Collaborate with others by tracking and working with remote branches.

**Using Fetch with your Git GUI:**

1. Navigate to the "Repository" tab.
2. Click "Fetch" and select the remote repository.
3. Review the fetched changes in the "Log" tab.

**Tracking Remote Branches with your Git GUI:**

1. Navigate to the "Branch" tab.
2. Click "Track Remote Branch" and select the remote branch to track.
3. Choose a local branch name to track the remote branch.

**Additional Concepts (Optional but Recommended)**

* **Git Bisect:** A tool for finding the commit that introduced a bug.
* **Git Archive:** Creates an archive of your repository at a specific point in time.
* **Git Subtree:** A way to merge another repository into your project as a subdirectory.

**Simulation Exercises (Choose One or More)**

1. **Rebase Conflict Resolution:** Simulate a rebase conflict and practice resolving it.
2. **Push-Pull Collaboration:** Work with a partner to simulate a collaborative workflow using Push and Pull.
3. **Fetch and Remote Branches:** Practice fetching changes and tracking remote branches in a simulated repository.

Here are the additional concepts that were missed earlier:

### Git Ignore (.gitignore)

* **What:** A `.gitignore` file specifies files or directories that Git should ignore in a repository.
* **Why:** Using `.gitignore` helps keep unwanted files out of your repository, reducing clutter and maintaining focus on relevant code.

**Key `.gitignore` Concepts:**

* **Patterns:** Use glob patterns to specify files or directories to ignore (e.g., `*.log`, `node_modules/`).
* **Negation:** Use `!` to negate a pattern and include a file/directory despite a preceding ignore rule.

**Creating and Managing `.gitignore` with your Git GUI:**

1. **Create `.gitignore` File:** Add a new file named `.gitignore` in your repository's root directory.
2. **Add Ignore Rules:** Edit the `.gitignore` file to include patterns for files/directories to ignore.
3. **Commit `.gitignore`:** Commit the updated `.gitignore` file to apply the ignore rules.

**Example `.gitignore` File:**

```bash
# Ignore log files
*.log

# Ignore node_modules directory
node_modules/

# But include a specific file within node_modules
!node_modules/.keep
```

### Pull Requests

* **What:** A Pull Request (PR) is a proposed change to a repository, submitted for review and approval by others.
* **Why:** Using Pull Requests facilitates collaborative development, code review, and quality control.

**Key Pull Request Concepts:**

* **Source and Target Branches:** Specify the branch with changes (source) and the branch to merge into (target).
* **PR Description and Comments:** Provide context and discuss changes with reviewers.

**Creating and Managing Pull Requests with your Git GUI (assuming a GitHub, GitLab, or similar repository host):**

1. **Create a New Branch:** Make changes in a new, topic-specific branch (e.g., `feature/new-feature`).
2. **Commit and Push Changes:** Commit your changes and push the branch to the remote repository.
3. **Submit a Pull Request:**
   * Navigate to the repository on the hosting platform (e.g., GitHub, GitLab).
   * Click "New Pull Request" and select the source and target branches.
   * Add a PR description, reviewers, and optional assignees.
4. **Review and Discuss:**
   * Reviewers examine the changes, comment, and request modifications if needed.
   * Address comments, update the branch, and push changes to the remote repository.
5. **Merge the Pull Request:**
   * Once approved, merge the Pull Request into the target branch.

**Best Practices for Pull Requests:**

1. **Keep PRs Focused:** Limit changes to a single, specific feature or fix.
2. **Write Clear Descriptions:** Provide concise, informative PR descriptions.
3. **Engage in Constructive Discussion:** Encourage open, respectful communication during review.

**Simulation Exercises (Choose One or More)**

1. **Create and Manage `.gitignore`:** Practice creating and updating a `.gitignore` file.
2. **Submit and Review a Pull Request:** Simulate the Pull Request process with a partner or a fictional scenario.

## Core Concepts for Git LFS

LFS stand for Large File Storage: if you have large files, you will only get a pointer for the file (a placeholder) on your machine, the file will be downlaoded when accessed.
There is no difference in day to day usage to use. Note that some GUIs do not support it fully.

### Git LFS Basics

* **What:** Git LFS (Large File Storage) is an extension for managing large files in Git repositories.
* **Why:** Using Git LFS helps reduce repository size while keeping all inputs and outputs tracked.

**Using Git LFS in a repo:**

1. **Install Git LFS:** Not installed by default with Git. Visit https://git-lfs.com/ for install instructions.
2. **Initialize Git LFS in your repo:**
   ```bash
   cd /path/to/your/repo
   git lfs install
   ```
3. **Track Large Files:** Configure Git LFS to track specific large file types (e.g., `.psd`, `.zip`).
   ```bash
   git lfs track "*.psd" "*.zip" "*.mp4"
   ```
4. **Commit the .gitattributes:**
   ```bash
   git add .gitattributes
   git commit -m "Track large files with Git LFS"
   ```

## Main Workflows

1. **Cloning and Initial Setup:**
   You begin by cloning the main repository (`Clone Repository` in your Git GUI). This creates a local copy.  Then, you'll likely set up your username and email address in your Git GUI's settings; essential for identifying your commits. *(Clone -> Configure User Settings)*
2. **Feature Branch Creation and Development:**
   You create a new branch for your task (`Create new branch` in your Git GUI). You then make your changes and commit them frequently (`Commit` in your Git GUI), with clear commit messages.  *(Create Branch -> Make Changes -> Commit)*
3. **Pushing to Remote and Creating a Pull Request:**
   Once your changes are ready, you push your feature branch to the remote repository (`Push` in your Git GUI).  Then you navigate to your repository hosting service (e.g., GitHub, GitLab) to create a Pull Request (PR), selecting your feature branch. This starts the review process. *(Push -> Create Pull Request)*.
4. **Reviewing Pull Requests (Others' Code):**
   You often review others' PRs. This involves understanding their changes (looking at the diffs), providing feedback in comments, and requesting modifications if necessary. *(Review PR -> Add Comments -> Request Changes (optional))*
5. **Addressing Review Feedback and Updating PR:**
   Reviewers provide feedback on your PR. You address these comments by making further changes, creating new commits, and pushing the updates to your feature branch. the changes are automatically updated in your PR. *(Address Comments -> Make Changes -> Commit -> Push)*.
6. **Merging Completed Pull Requests:**
   After a successful review and final approval, your PR is merged (`Merge Pull Request` on the hosting platform).  This integrates your changes into the main branch.  *(Merge into main (automatic merging))*.
7. **Pulling Updates from Main:**
   To keep your local repository synced and avoid conflicts, periodically pull updates from the main (or `develop`) branch (`Pull` in your Git GUI). This downloads the latest changes from the remote repository. This frequently results in a merge operation.  *(Pull -> Merge (automatic merge most of the time) -> manual merge, chose strategy and manually edit (rarely))*.
8. **Resolving Merge Conflicts:**
   If you have conflicting changes with changes others have made, Git will warn you in the merge process.  You'll need to open the conflicting files, manually review changes, and resolve the conflicts; merging usually involves simply saving your edited file; the merge is complete when the conflict markers are removed. Afterwards, commit the merge. *(Automatic Merge -> Merge Conflicts: Manual Edit -> Merge Commit)*.
9. **Working with Multiple Branches:**
   For complex tasks, you'll likely manage multiple feature branches simultaneously. Keeping the branches organized and their purposes clear will help with a better developer experience.
10. **Undoing Commits (Before Push):**
    If you make a mistake *before* pushing, you can undo or amend your last commit. Using `git reset --soft HEAD^` (command line) is one way to move back one commit and adjust your mistakes before pushing the updates. *(Make mistake -> git reset --soft HEAD^ -> Adjust -> Commit)*.
11. **Reverting Commits (After Push):**
    After a commit is pushed, reversing it is usually safer as revert instead of `git reset`. To correct past commits, use "Revert commit" in your Git GUI. This adds a *new* commit that undoes the previous mistake without altering the shared history.  *(Make a mistake in a pushed commit -> Revert Commit -> Commit)*
12. **Amending the Last Commit:**
    For minor adjustments to your last *unpushed* commit, use 'Amend' commit option in your Git GUI. This cleans up history by updating the last commit.  *(Minor mistakes in the last unpushed commit -> Amend Commit)*

## Advanced concepts

### Git Submodules

* **What:** Git Submodules allow you to include other Git repositories within your project, enabling modular dependencies and external collaborations.
* **Why:** Using Submodules helps you manage complex projects, include third-party libraries, and maintain a clear dependency graph.
* **Analogy:** Think of Submodules as LEGO blocks; each block is a self-contained unit that fits into the larger project structure.

**Key Submodule Concepts:**

* **Submodule Repository:** The external Git repository included in your project.
* **Submodule Path:** The directory where the submodule is checked out.

**Adding and Managing Submodules with your Git GUI:**

1. Navigate to the "Submodules" tab.
2. Click "Add submodule" and enter the submodule repository URL and path.
3. Update the submodule to the latest commit using "Update submodule".

### Git Hooks

* **What:** Git Hooks are custom scripts that execute automatically at specific points during the Git workflow (e.g., pre-commit, post-merge).
* **Why:** Using Git Hooks helps you enforce coding standards, automate testing, and enhance the development workflow.
* **Analogy:** Think of Git Hooks as guardians of your repository, ensuring consistency and quality.

**Common Hook Types:**

* **Client-Side Hooks:** Run on the developer's machine (e.g., pre-commit).
* **Server-Side Hooks:** Run on the remote repository server (e.g., pre-receive).

**Configuring Git Hooks with your Git GUI:**

1. Navigate to the "Settings" tab.
2. Click "Hooks" and select the hook type (e.g., "Pre-commit").
3. Enter the script or command to execute for the chosen hook.

### Git Cherry-Picking and Rebasing

* **What:** Git Cherry-Picking applies a single commit from one branch to another. Git Rebasing replays commits from one branch onto another, maintaining a linear history.
* **Why:** Using Cherry-Picking and Rebasing helps you integrate specific changes, maintain a clean history, and simplify conflict resolution.
* **Analogy:** Think of Cherry-Picking as a precise cherry selection, and Rebasing as reorganizing a book's chapters for a cleaner narrative.

**Using Cherry-Picking and Rebasing with your Git GUI:**

1. **Cherry-Picking:**
   * Navigate to the "Log" tab and find the commit to cherry-pick.
   * Right-click on the commit and select "Cherry-pick".
2. **Rebasing:**
   * Navigate to the "Branch" tab and select the branch to rebase.
   * Right-click on the branch and select "Rebase onto" and choose the target branch.

**Continuing the Crash Course: Git for Technical Professionals (Using your Git GUI)**

### Git Rebase

* **What:** Git Rebase replays commits from one branch onto another, maintaining a linear history.
* **Why:** Using Rebase helps you:
  + Maintain a clean, linear commit history.
  + Avoid unnecessary merge commits.
  + Simplify conflict resolution.

**Rebase Workflow:**

1. **Rebase Onto:** Rebase your feature branch onto the latest main branch.
2. **Resolve Conflicts:** Address any conflicts that arise during the rebase process.
3. **Continue Rebase:** Once conflicts are resolved, continue the rebase process.
4. **Force Push:** After a successful rebase, force push the updated branch to the remote repository.

**Using Rebase with your Git GUI:**

1. Navigate to the "Branch" tab and select the branch to rebase.
2. Right-click on the branch and select "Rebase onto" and choose the target branch.
3. Resolve any conflicts that arise during the rebase process.
4. Once complete, force push the updated branch using "Push" with the "--force" option.
