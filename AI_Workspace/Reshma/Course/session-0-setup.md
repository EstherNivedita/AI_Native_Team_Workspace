# Lesson 0: Setting up your workspace

## What this session covers
Git basics: what a repository is, how to clone it, and how to pull and push changes. By the end, the learner has the team repo on their machine and understands how files move between their computer and the shared repository.

## Teaching flow

### What is a repository?
A repository (repo) is a shared folder that lives online — in this case on GitHub. Everyone on the team has their own copy on their own machine. When you make changes, you "push" them so others can see. When others make changes, you "pull" to get the latest version. Think of it like a shared Google Drive folder, but with a full history of every change ever made.

### Hands-on: Clone the repo
Walk them through opening their terminal and running:
```
cd ~/Desktop/Projects
git clone [repo-url]
```
Explain each part: `cd` moves to a folder, `git clone` downloads a copy of the repository to their machine. After cloning, have them open the folder and look at the structure. Point out their personal folder and the course/ folder inside it.

### The three commands they need
Teach only these three — nothing more:

**git pull** — "Get the latest changes from the team repo. Do this at the start of every session."

**git add . && git commit -m "message"** — "Save a snapshot of your changes with a description. During the course, I'll handle commits for you and explain each one."

**git push** — "Send your saved changes to the shared repo so your PM and teammates can see them. Do this at the end of every session."

Have them practice the full cycle: create a test file called `hello.md` in their folder with one line ("My AI learning journey starts here"), then add, commit with the message "First commit — starting the course", and push. Confirm it appears on GitHub.

### Reflection
"You just pushed a file to a shared repository. Everyone with access can see it. Think about what just happened — you made a change locally, saved a snapshot, and synced it. This is version control. As we build your AI workspace this week, every file we create gets committed the same way. By Friday, you'll have a full history of everything you built and learned."

### Clean up
Delete the test file, commit with message "Remove test file — setup complete", and push. Confirm their folder is clean and ready for the course to begin.
