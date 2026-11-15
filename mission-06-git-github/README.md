# Mission 6 — Git and GitHub

## 1. Task / objective

Understand version control and practise staging, committing,
and reviewing changes. Create a branch named update-about,
update the project's main README, and open a Pull Request into main.

## 2. Work completed

### Task 6.1 — Basic Git Workflow

| Git operation | Command | What it does |
|---------------|---------|--------------|
|Check repository status| `git status` | Shows the current branch and files with changes. |
| Stage selected changes | `git add mission-06-git-github/README.md` | Selects this README's current contents for the next commit. |
| Create a commit | `git commit -m "Document Git and GitHub concepts"` | Records staged changes in the local repository. |
| View commit history | `git log --oneline -5` | Shows the five most recent commits in a compact format. |

**Difference between staging and committing**

Staging selects the changes to include in the next commit.
Committing records those selected changes as a snapshot in the
local repository. Pushing uploads local commits to GitHub.

### Task 6.2 — Create and Use a Branch

A branch allows changes to be developed separately from main.

The required branch is update-about. On that branch, the root
README.md must receive a section titled “My Learning” describing
two or three things learned during the assignment.

The workflow is:

1. Commit the Mission 6 documentation on main.
2. Create and switch to update-about.
3. Add My Learning to the root README.md.
4. Review, stage, and commit the README change.
5. Push update-about to GitHub.

**Create and switch to the branch**

```bash
git switch -c update-about
```

**Review the root README change**

```bash
git diff -- README.md
```

**Stage the change**

```bash
git add README.md
```

**Commit the change**

```bash
git commit -m "Add My Learning section to README"
```

**Publish the branch**

```bash
git push -u origin update-about
```

The -u option connects the local branch to its remote counterpart
for future pushes and pulls.

Branch activity status: Pending.

### Task 6.3 — Create a Pull Request

A Pull Request proposes bringing changes from one branch into
another. It allows the changes to be reviewed before merging.

For this activity:

- Repository: digital-detective-8465
- Base branch: main
- Compare branch: update-about
- Proposed change: Add My Learning to the root README.
- PR title: Add My Learning section to README

After pushing the branch, open the repository on GitHub and create
a Pull Request. Check that the base is main and the compare branch
is update-about. Add a short description and review Files changed.

Merge only if the instructor has asked for a merge. Otherwise,
leave the PR open and record its status.

If the PR is merged, return to the local main branch and retrieve
the changes:

git switch main

git pull --ff-only origin main

**Why branches and Pull Requests are useful**

Branches keep proposed changes separate from the main version.
Pull Requests let people review and discuss those changes.
Pushing a branch does not automatically create or merge a PR.

Pull Request status: Not yet created.

### Task 6.4 — Git Command Glossary

**Initialise a repository — git init**

Starts Git tracking in a local directory. This is unnecessary
after cloning an existing repository.

**Check status — git status**

Shows the current branch and staged, unstaged, and untracked files.

**Stage changes — git add**

Selects file contents for the next commit.

**Commit changes — git commit**

Records staged changes in the local repository.

**View history — git log**

Displays recorded commits and their details.

**Create a branch — git branch branch-name**

Creates a branch without switching to it.

**List branches — git branch**

Lists local branches and marks the current branch.

**Switch branches — git switch branch-name**

Switches to an existing branch.

**Create and switch — git switch -c branch-name**

Creates a branch and switches to it.

**Publish changes — git push**

Uploads local commits to a remote repository.

**Retrieve remote changes — git fetch**

Downloads remote changes without integrating them into the
current branch.

**Retrieve and integrate changes — git pull**

Fetches remote changes and integrates them into the current branch
according to the options and configuration.

## 3. Commands / tools used

- Git: Manages version history and branches.
- GitHub: Hosts the repository and supports Pull Requests.
- Terminal: Provides the interface for entering Git commands.
- Visual Studio Code: Edits README files.
- Markdown: Formats documentation.


## 4. My understanding

Git records project changes locally. GitHub hosts the repository
online and provides collaboration tools.

Staging, committing, and pushing are separate actions.
Staging selects changes, committing records them locally, and
pushing uploads commits.

A branch provides a separate line of development. A Pull Request
proposes adding its changes to another branch. The changes enter
the target branch only when the PR is merged or otherwise integrated.

## 5. Difficulties faced

I initially thought pushing changes automatically created a
Pull Request. I also needed to distinguish the Mission 6 README
from the project's root README.

## 6. How I resolved them

I learned that pushing uploads commits, while creating a Pull
Request is a separate action on GitHub.

The Mission 6 README documents the activity. The root README is
the file that receives the My Learning section on update-about.

## 7. Evidence / files

- mission-06-git-github/README.md: Git explanations and activity plan.
- Root README.md: Will contain My Learning on update-about.
- GitHub branch and Pull Request: To be created and verified.

## 8. Commit details

 commit:
 