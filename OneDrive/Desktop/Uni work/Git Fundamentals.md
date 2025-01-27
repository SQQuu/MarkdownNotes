# Git Fundamentals

## Version Control

Version control helps keep track of how things change over time.

- **Purpose:**
  - Tracks changes and allows reverting to previous versions.
  - Provides a history of all changes.
  - Supports collaboration by handling simultaneous updates and conflicts.
  - Enables off-site data copies via easy synchronization.

## What is Git?

Git is a version control system (VCS):

- **Features:**
  - Fast, modern, and fully featured.
  - Most popular VCS.
  - Open-source and free.
  - Provides version history.
  - Ideal for team collaboration.
  - Distributed: local copy + optional remote copy.

### Basic Git Commands

- `git init` - Initialize a new repository.
- `git add` - Stage files for commit.
- `git status` - Check the status of changes.
- `git commit` - Save changes.
- `git push` - Upload local changes to remote repository.

## Git Components

- **Git Bash:** Command-line interface.
- **Git Server:** Remote storage solutions (e.g., GitHub, GitLab, BitBucket).
- **Graphical UI:** GitHub Desktop, IDE integration.
- **Repository (Repo):** Folder controlled by Git.

## Installing Git

### Single Branch Git Workflow

1. Start by creating a repository and storing files.
2. Commit changes to create different versions.
3. If an experiment fails, revert to earlier versions.

### Multi-Branch Git Workflow

1. Start with a base version.
2. Create separate branches for experiments.
3. If the experiment fails, discard the branch.

## Git Configuration

Configure parameters:

```bash
    git config --global user.name "Your Name"
    git config --global user.email "your.email@example.com"
    git config --global init.defaultBranch main
```

## Creating a Git Repository

```bash
pwd        # Print working directory
mkdir repo_name  # Create a new directory
cd repo_name     # Enter the directory
git init         # Initialize Git repository
notepad .gitignore  # Create a .gitignore file
```

### Example `.gitignore` File

```bash
# Exclude all properties files from repo
*.properties
```

## Staging and Committing Files

- **Working Directory:** Project files in local storage.
- **Staging Area:** Files added using `git add`.
- **Local Repository:** Stores committed versions.

```bash
notepad README.md  # Create a README file
git add README.md  # Add to staging
git commit -m "First commit"  # Commit with a message
git status  # Check current status
```

## Copying a Local Repo to GitHub

1. Create a repository on GitHub.
2. Copy the HTTPS link.
3. Link local and remote repositories:

```bash
git remote add origin <repo_url>
git push origin main
```

### Using SSH Instead of HTTPS

```bash
ssh-keygen -t rsa -b 4096 -C "your.email@example.com"
notepad ~/.ssh/id_rsa.pub  # Copy key to clipboard
```

---

# Python Notes

## Setting Up a Python Project

1. Right-click > New Folder > `PythonProjectSP`
2. Create a Python file `hello.py`
3. Run the file:

```python
print("Hello, world!")
```

## Python Basics

### Data Types

- **Numbers:** `int`, `float`
- **Strings:** `"text"`, `len("hello")`
- **Booleans:** `True`, `False`

```python
print(type(5))  # Output: <class 'int'>
print(bool(0))  # Output: False
```

### Operators

```python
result = 10 % 3  # Modulo operator
print(result)  # Output: 1
```

### String Manipulation

```python
first_name = "John"
last_name = "Doe"
full_name = first_name + " " + last_name
print(full_name)
```

### Control Flow

```python
if 2 == 2:
    print("Numbers are equal")
elif 2 > 3:
    print("Greater")
else:
    print("Not greater")
```

### Lists and Dictionaries

```python
my_list = [1, 2, 3, 4]
my_list.append(5)
print(my_list[0])  # Output: 1

contact_list = {"Alice": "123-456"}
print(contact_list["Alice"])
```

### Loops

```python
for i in range(5):
    print(i)

counter = 0
while counter < 5:
    print(counter)
    counter += 1
```


