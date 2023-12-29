Learning Git Commands
Welcome to my Git learning repository! This repository serves as my personal space to practice and document various Git commands, workflows, and concepts while I explore the world of version control.

Contents
Commands: Examples and explanations of essential Git commands.
Workflows: Documenting different branching models, merging strategies, and rebasing techniques.
Best Practices: Notes on Git best practices, tips, and tricks.
Exercises: Practical exercises to reinforce understanding and proficiency.
Scripts: Useful scripts or automation tools related to Git operations.
Purpose
This repository is a hands-on playground where I experiment with Git's features, aiming to solidify my understanding and proficiency in version control. It's an evolving resource that I'll continuously update as I progress in my Git learning journey.

Getting Started
Feel free to explore the folders and files within this repository. Dive into the various sections to grasp different aspects of Git commands and workflows. Don't hesitate to contribute or suggest improvements!

Feedback
Your feedback, suggestions, or corrections are highly appreciated! If you spot any mistakes or have ideas to enhance this repository, please raise an issue or submit a pull request. Let's learn Git together!

------------------------------------------------------------------------------------------------------------------------------------

Pull changes from main:

git pull origin main

------------------------------------------------------------------------------------------------------------------------------------

To display only the name of the current branch you're on:

git rev-parse --abbrev-ref HEAD

------------------------------------------------------------------------------------------------------------------------------------

### Working with Local and Remote Repositories

#### Clone a Repository

```bash
git clone <repository_url>
```

#### Add Changes to Staging Area

```bash
git add .
```

#### Commit Changes

```bash
git commit -m "Commit message"
```

#### Push Changes to Remote Repository

```bash
git push origin <branch_name>
```

### Branching and Merging

#### Create a Branch

```bash
git branch <branch_name>
```

#### Switch to a Branch

```bash
git checkout <branch_name>
```

#### Merge Branches

```bash
git merge <branch_name_to_merge_into>
```

### Rebasing

#### Rebase Commits

```bash
git rebase <base_branch>
```

### Conflict Resolution

#### Resolve Conflicts

```bash
# After resolving conflicts, add changes and commit
git add .
git commit -m "Merge conflict resolution"
```

### Stashing

#### Stash Changes

```bash
git stash
```

#### Apply Stashed Changes

```bash
git stash apply
```

### Tagging

#### Create a Tag

```bash
git tag <tag_name>
```

### Cherry-picking

#### Cherry-pick Commits

```bash
git cherry-pick <commit_hash>
```

### Gitignore

#### Create Gitignore File

```bash
# Create a .gitignore file and add patterns to ignore
nano .gitignore
```

### Submodules

#### Add a Submodule

```bash
git submodule add <repository_url>
```

### Bisect

#### Use Bisect

```bash
git bisect start
git bisect bad <commit_hash>
git bisect good <commit_hash>
```

### Reflog

#### View Reflog

```bash
git reflog
```

### Hooks

#### Set Up Hooks

Hooks are custom scripts placed in `.git/hooks` directory and named accordingly (pre-commit, post-commit, etc.). There's no direct GitHub command for this; it's a local configuration.


------------------------------------------------------------------------------------------------------------------------------------


### Resolve Merge Conflicts

#### Step 1: Identify Conflicts

```bash
# Checkout the branch where the merge is happening
git checkout <your_branch>

# Start the merge
git merge <branch_to_merge>

# You'll see a message about conflicts

# Identify conflicted files
git status
```

#### Step 2: Manually Resolve Conflicts

Open the conflicted files in your code editor. You'll see markers indicating the conflicting changes. Manually edit the files to keep the desired changes and remove conflict markers (<<<<<<<, =======, >>>>>>>).

#### Step 3: Add Resolved Changes

```bash
# After resolving conflicts, add the modified files
git add <conflicted_files>
```

#### Step 4: Commit Changes

```bash
# Commit the resolved changes
git commit -m "Resolved merge conflicts"
```

#### Step 5: Complete the Merge

```bash
# Complete the merge
git merge --continue
```
