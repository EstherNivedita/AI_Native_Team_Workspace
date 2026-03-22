# Lesson 0: Setting up your workspace

## What this session covers
Git basics: what a repository is, how to clone it, how changes sync between their computer and GitHub, and the full cycle of pull → change → commit → push. By the end, the learner has the repo on their machine, understands how version control works, and has made their first personal contribution to their workspace — all done by you (the AI tutor) while explaining each step.

## Teaching flow

### What is a repository?
A repository (repo) is a shared folder that lives online — in this case on GitHub. Everyone on the team has their own copy on their machine. When changes are made, they get "pushed" so others can see. When others make changes, you "pull" to get the latest version. Think of it like a shared Google Drive folder, but with a full history of every change ever made — you can always go back to any previous version.

### Clone the repo
The learner needs to clone the repo to their machine. This is the first step — you run the clone command and explain what's happening:
```
cd ~/Desktop
git clone [repo-url]
```
Explain: `cd` moves to a folder, `git clone` downloads the entire repo from GitHub to their computer. Once cloned, confirm the folder exists.

### Explore the folder structure
Navigate into the repo and show them their personal folder. Explain the structure:
```
team-ai-workspace/
└── [their-name]/
    ├── course/          ← Session files are already here (your learning material)
    └── (everything else gets built during the week)
```
Explain: "The course/ folder has all your session files pre-loaded — that's what I'll read each day to teach you. Everything else — your context files, skill files, agent files — we'll build together over the week. All of it lives under YOUR folder, and all of it gets pushed to GitHub so your PM can see your progress."

### The git cycle — the five things that happen
Explain the full cycle simply. Don't ask them to run these — YOU demonstrate each one:

**git pull** — "I'm downloading the latest changes from the shared repo. I'll do this at the start of every session to make sure we have the latest version."

**Making changes** — "This is just creating, editing, or deleting files. Normal work."

**git add .** — "I'm telling git 'these are the changes I want to save.' Think of it as selecting which files to include in the snapshot."

**git commit -m "message"** — "I'm saving a snapshot with a description of what changed and why. This is like saving a version of a design file — you can always go back to it."

**git push** — "I'm sending the saved snapshot to the shared repo on GitHub. Now everyone can see the changes."

Every session, every file we create follows this exact cycle. I'll handle all of this for you — but I want you to understand what's happening each time.

### Demo: the full cycle with a test file
Create a test file called `hello.md` in their folder with one line ("My AI learning journey starts here"). Walk through each step out loud as you do it: "I'm creating the file... now I'm staging it with git add... now I'm committing with a message... now I'm pushing to GitHub." Ask them to open GitHub in their browser and confirm they can see the file. This is the moment it clicks — something on their computer is now visible online.

### Demo: editing a file
Edit hello.md to add a second line ("This file was edited to show how changes work"). Run the same add → commit → push cycle. Explain: "Same process whether I'm creating a new file or changing an existing one. Every change gets saved as a new snapshot with its own message."

### Quick vocabulary
Explain these briefly — one sentence each, they don't need to use them yet but should know the terms:

**Branch** — "You're working on 'main', which is the shared version everyone sees. Think of it as the primary copy."

**Pull request** — "A way to propose changes for someone to review before they go into main. You won't use this yet, but you'll hear the term."

**Merge** — "Combining changes together. When multiple people work on the same repo, their changes get merged. Git handles this automatically most of the time."

### Their first personal contribution
Now ask: "We're about to start building your AI workspace this week. What's one folder you'd want to create in your workspace, and one file you'd want to put in it? It can be anything — something related to your work, a notes file, a list of ideas."

Based on their answer, YOU create the folder and file under their personal workspace (NOT under course/). Commit with a descriptive message that references their choice — e.g., "Add inspiration/ folder with design-ideas.md — [Name]'s first workspace contribution." Push to GitHub. Ask them to verify it on GitHub.

This stays in their workspace — it's real, it's theirs, and it's the beginning of what they'll build all week.

### Clean up the test file
Delete hello.md, commit with message "Remove test file — setup complete", push. Their personal folder and file remain. The workspace is clean and ready.

### Reflection
"You just saw the full cycle — clone, create, edit, commit, push — and you've got your first real file in your workspace on GitHub. Every day this week, I'll create files as we learn together, and every one of them will be committed and pushed so there's a full history of everything we build. Your PM can see your progress, your teammates can see your workspace, and you can always go back to any version. That's version control — and it's the foundation we'll build everything else on top of."
