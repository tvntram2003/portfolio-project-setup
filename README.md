# Portfolio Project - Initial Setup

## 1. Tools Installed
- **Cursor IDE:** Installed the AI-powered code editor as the primary development environment.
- **Claude Code and Codex Assist (v0.4.62):** Installed to manage chat history, code diffs, and usage tracking.
- **Codex – OpenAI’s coding agent (v26.417.40842):** Added and authenticated to enhance code generation capabilities.

## 2. Steps Completed
- Set up the local development environment by downloading and installing Cursor IDE on macOS.
- Searched for, installed, and successfully authorized both required extensions (Claude Code & Codex).
- Initialized a new public Git repository on GitHub named `portfolio-project-setup`.
- Created this `README.md` file locally to document the workflow and tool stack.
- Executed standard Git commands (`init`, `add`, `commit`, `branch -M main`) via Cursor's integrated terminal to track changes.
- Connected the local repository to the remote GitHub server and pushed the initial commit.

## 3. Issues Ran Into and Solutions

While setting up the Git workflow, I encountered two specific technical issues and resolved them as follows:

* **Issue 1: Authentication Block on macOS**
    * **Problem:** During the initial `git push`, the default browser-based GitHub authentication failed to sync properly with the macOS credential manager, blocking the push.
    * **Solution:** I bypassed the browser authentication by navigating to my GitHub Developer Settings and generating a classic Personal Access Token (PAT) with `repo` scopes. I then used this token for secure command-line authentication.
* **Issue 2: Remote URL Configuration Error**
    * **Problem:** After generating the PAT, I attempted to set the remote URL manually but encountered a "URL rejected: Port number was not a decimal number" error.
    * **Solution:** I reviewed the command syntax and identified a formatting typo (using a `/` instead of an `@` separator before `github.com`). I quickly corrected the remote origin using the `git remote set-url origin` command with the proper format (`https://<username>:<token>@github.com/...`) and successfully pushed the code to the `main` branch.