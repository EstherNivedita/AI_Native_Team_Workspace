# Lesson 0: Setting up your workspace

## What this session covers
Git basics: what a repository is, how to clone it, and how changes sync between their computer and GitHub. By the end, the learner has the repo on their machine and has seen their first file created, committed, and pushed — all done by you (the AI tutor) while explaining each step.

## Teaching flow

### What is a repository?
A repository (repo) is a shared folder that lives online — in this case on GitHub. Everyone on the team has their own copy on their machine. When changes are made, they get "pushed" so others can see. When others make changes, you "pull" to get the latest version. Think of it like a shared Google Drive folder, but with a full history of every change ever made.

### Hands-on: Clone the repo
The learner needs to clone the repo to their machine. This is the ONE step that requires their approval — you run the clone command and explain what's happening:
```
cd ~/Desktop
git clone [repo-url]
```
Explain: `cd` moves to a folder, `git clone` downloads a copy of the repo. Once cloned, confirm the folder exists and you can see their personal folder inside it. From this point forward, YOU handle all file creation and git commands — the learner watches, learns, and responds to your questions.

### The three concepts they need to understand
Don't ask them to run these commands. Explain them as YOU demonstrate:

**git pull** — "I'm getting the latest changes from the team repo. I'll do this at the start of every session."

**git add + commit** — "I'm saving a snapshot of the changes I just made, with a description of what changed and why. Think of it like saving a version of a design file."

**git push** — "I'm sending the saved changes to the shared repo so your PM and teammates can see your progress."

### Demonstrate the full cycle
Create a test file called `hello.md` in their folder with one line ("My AI learning journey starts here"). As you do this, explain each step: "I'm creating a file, now I'm committing it with a message, now I'm pushing it to GitHub." Ask them to check GitHub in their browser to confirm it appeared.

### Reflection
"You just saw me push a file to a shared repository. Everyone with access can see it. This is version control — every change is tracked, every version is saved. As we build your AI workspace this week, every file I create gets committed the same way. By Friday, you'll have a full history of everything we built together."

### Clean up
Delete the test file, commit with message "Remove test file — setup complete", and push. Confirm the folder is clean and ready for the course to begin.
