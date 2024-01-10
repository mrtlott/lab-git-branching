## Objective

- creating branches
- merging changes
- managing branches in Git 

## Prerequisites

- A GitHub account.
- Git installed on your local machine.

## Steps

### 1. Fork the Repository

- From this GitHub repository.
- Click on "Fork" above to create a copy in your GitHub account.

### 2. Clone the Forked Repository

Clone the forked repository to your local machine:

```bash
git clone [URL of your forked repository]
```

*Replace `[URL of your forked repository]` with the actual URL of your fork.*

### 3. Create and Work on Branch A

Navigate to your repository:

```bash
cd [repository name]
```

Check the current branch using the command below (should be `main`):

```bash
git branch
```

Create and switch to branch A:

```bash
git checkout -b branch-a
```

Confirm you are on branch A:

```bash
git branch
```

Manually open and add "feature 1" to a text file. For example, using a text editor:

```bash
open feature.txt
```

*Add the text "feature 1" to the file, save and close the editor.*

Go back to your terminal and check the status of your branch:

```bash
git status
```

Add and commit the change:

```bash
git add feature.txt
git commit -m "Add feature 1"
```

### 4. Create and Work on Branch B

Switch to the main branch and check the current branch:

```bash
git checkout main
git branch
```

Create and switch to branch B:

```bash
git checkout -b branch-b
git branch
```

Again, manually open the text file and add "feature 2":

```bash
open feature.txt
```

*Add the text "feature 2" to the file, save and close the editor.*

Add and commit the change:

```bash
git add feature.txt
git commit -m "Add feature 2"
```

### 5. Merge Branch B into Branch A

Switch to branch A and merge branch B into it:

```bash
git checkout branch-a
git merge branch-b
```

*Resolve any conflicts if they arise and commit the changes.*

### 6. Merge Branch A into Main

Switch to the main branch:

```bash
git checkout main
git merge branch-a
```

### 7. Delete Feature Branches

Delete branches A and B locally:

```bash
git branch -d branch-a
git branch -d branch-b
```

### 8. Push Main Branch and Create a Pull Request

Push the main branch to your forked repository:

```bash
git push origin main
```

On GitHub, navigate to your forked repository and create a pull request to the original repository.

