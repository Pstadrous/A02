# A02 – How to Use Git, WebStorm, and GitHub

Author: _Your Name_ (UCID: _yourUCID_)  
Course: _Course Name / Section_

This tutorial walks a beginner through installing the tools, creating a **repository** on **GitHub**, editing it in WebStorm, and saving work back to **GitHub** with **Git**. Glossary words are bolded each time they are used; their definitions are in Part 2.

---

## Part 1: Directions on Using WebStorm with Git and GitHub

### Step 1 – Create a GitHub account

1. Go to https://github.com/signup.
2. Enter your email address, create a password, and choose a username. For this class, use your UCID as your username so your **repository** link looks like `https://github.com/yourUCID/A02`.
3. Verify your email address using the code **GitHub** sends you.
4. (Recommended) Students can apply for free extras through the **GitHub** Student Developer Pack at https://education.github.com/pack (GitHub, n.d.-d).

### Step 2 – Download and install Git

**Git** is the program that tracks your changes on your own computer. WebStorm uses it behind the scenes.

1. Download **Git** from https://git-scm.com/downloads and choose your operating system (Windows, macOS, or Linux).
2. Run the installer. The default options are fine for beginners.
3. Open a terminal (Command Prompt, PowerShell, or Terminal) and check the install:

   ```bash
   git --version
   ```

4. Tell **Git** who you are. Use the same email you used for **GitHub**:

   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "you@example.com"
   ```

   (Chacon & Straub, 2014)

### Step 3 – Download and install WebStorm

1. Download WebStorm from https://www.jetbrains.com/webstorm/download/ (JetBrains, n.d.-d).
2. WebStorm is free for non-commercial use, including learning. Students can also get a free educational license for all JetBrains tools at https://www.jetbrains.com/community/education/#students (JetBrains, n.d.-a).
3. Install and open WebStorm. On first launch, choose your theme and accept the defaults.

### Step 4 – Create the A02 repository on GitHub

1. Sign in at https://github.com.
2. Click the *+* icon in the top-right corner and choose *New repository*.
3. In *Repository name*, type `A02`. Use a capital *A*. **Repository** names are case-sensitive in the link your instructor checks.
4. Set the **repository** to *Public* so your instructor can see it.
5. Check *Add a README file*. This creates the `README.md` file you will edit.
6. Click *Create repository*.

Your new **repository** is now at `https://github.com/yourUCID/A02` (GitHub, n.d.-b).

### Step 5 – Connect WebStorm to your GitHub account

1. In WebStorm, open *Settings* (Windows/Linux: *File → Settings*; macOS: *WebStorm → Settings*).
2. Go to *Version Control → GitHub*.
3. Click *+* (Add Account) and choose *Log In via GitHub*.
4. A browser window opens. Click *Authorize* to give WebStorm access, then return to WebStorm.
5. Also check *Version Control → Git*. Click *Test* to confirm that WebStorm found your **Git** installation (JetBrains, n.d.-b).

### Step 6 – Clone the repository to your computer

To **clone** a **repository** means to download a full copy of it, including its history.

1. On the WebStorm Welcome screen, click *Clone Repository* (in older versions, *Get from VCS*). If a project is already open, use *Git → Clone…* from the main menu.
2. Choose the **GitHub** tab on the left. Your **repository** list will appear.
3. Select *A02*, choose a folder on your computer for it, and click **Clone**.
4. Click *Trust Project* when asked. The project opens with `README.md` in the Project panel.

Behind the scenes, WebStorm ran this command:

```bash
git clone https://github.com/yourUCID/A02.git
```

The **GitHub** copy is now set up as a **remote** called `origin` (Chacon & Straub, 2014).

### Step 7 – Edit the README.md file

1. Double-click `README.md` in the Project panel.
2. WebStorm shows the Markdown text and a live preview side by side.
3. Type your tutorial, then save with *Ctrl+S* (macOS: *Cmd+S*). Changed files turn blue in the Project panel.

### Step 8 – Commit your changes

A **commit** saves a snapshot of your changes in your local **repository**.

1. Open the **Commit** tool window: *Git → Commit…* or *Ctrl+K* (macOS: *Cmd+K*).
2. Check the box next to each file you want to include, such as `README.md`.
3. Write a clear **commit** message in the message box. Use the class format:

   ```text
   Task: Create Repository
   Feature: added workflow for using github
   Fix: changed readme.md for definition of terms
   ```

4. Click **Commit**. If you are ready to upload right away, click *Commit and Push…* instead.

Command-line equivalent:

```bash
git add README.md
git commit -m "Feature: added workflow for using github"
```

### Step 9 – Push your commits to GitHub

To **push** is to upload your local **commit** history to the **remote** **repository** on **GitHub**.

1. Choose *Git → Push…* or *Ctrl+Shift+K* (macOS: *Cmd+Shift+K*).
2. Review the list of commits and click **Push**.
3. Refresh `https://github.com/yourUCID/A02` in your browser. Your updated README now appears.

Command-line equivalent: `git push origin main` (GitHub, n.d.-c).

### Step 10 – Fetch and pull changes from GitHub

If you edit a file on the **GitHub** website or on another computer, bring those changes into WebStorm:

1. **Fetch**: *Git → Fetch* downloads information about new changes from the **remote** but does not change your files yet. It lets you see what is new first.
2. **Pull**: *Git → Pull…* (or *Ctrl+T* / *Cmd+T* to Update Project) downloads the changes and combines them into your files.

Always **pull** before you start working so that your copy is up to date (Atlassian, n.d.).

### Step 11 – Work on a branch and merge it (optional but recommended)

A **branch** lets you try changes without affecting the main version.

1. Click the **branch** name in the top-left of the WebStorm window (it usually says `main`).
2. Choose *New Branch…*, name it (for example, `add-glossary`), and click *Create*.
3. Edit your files, then **commit** and **push** as in Steps 8–9.
4. When you are done, switch back to `main` from the same **branch** menu.
5. Click the `add-glossary` **branch** and choose *Merge 'add-glossary' into 'main'*.
6. **Push** `main` to **GitHub**.

### Step 12 – Resolve a merge conflict

A **merge conflict** happens when two changes edit the same lines and **Git** cannot decide which one to keep.

1. WebStorm opens a *Conflicts* dialog that lists the affected files.
2. Click *Merge…* to open the three-pane view. Your version is on the left, the incoming version is on the right, and the result is in the middle.
3. Use the arrows to accept the left change, the right change, or both. You can also type directly in the middle pane.
4. Click *Apply*, then **commit** and **push** the result (JetBrains, n.d.-c).

### Step 13 – Submit your repository link to Canvas

1. Copy the link from your browser's address bar. It should look like `https://github.com/yourUCID/A02`.
2. Paste it into the Canvas assignment submission box and submit.

### Quick reference: WebStorm vs. command line

| Action | WebStorm | Command line |
|---|---|---|
| **Clone** | Git → Clone… | `git clone <url>` |
| **Commit** | Git → Commit… (Ctrl+K) | `git add .` then `git commit -m "message"` |
| **Push** | Git → Push… (Ctrl+Shift+K) | `git push` |
| **Fetch** | Git → Fetch | `git fetch` |
| **Pull** | Git → Pull… | `git pull` |
| **Branch** | Branch menu → New Branch… | `git switch -c <name>` |
| **Merge** | Branch menu → Merge into… | `git merge <name>` |

---

## Part 2: Glossary

- **Branch** – A separate line of development in a repository. A branch lets you make and test changes without affecting the main version of the project until you choose to merge them (Chacon & Straub, 2014).
- **Clone** – To make a complete local copy of a remote repository, including all of its files, branches, and commit history (GitHub, n.d.-a).
- **Commit** – A saved snapshot of changes in a repository. Each commit records who made the change, when it was made, and a message describing it (Chacon & Straub, 2014).
- **Fetch** – To download new commits and branch information from a remote repository without changing your working files (Atlassian, n.d.).
- **GIT** – A free, open-source, distributed version control system that tracks changes to files over time. It lets many people work on the same project (Chacon & Straub, 2014).
- **Github** – A web-based platform that hosts Git repositories online. It adds tools for sharing, collaboration, issue tracking, and code review (GitHub, n.d.-a).
- **Merge** – To combine the changes from one branch into another branch (Chacon & Straub, 2014).
- **Merge Conflict** – A situation where Git cannot automatically merge changes because two branches changed the same lines of a file differently. A person must choose which changes to keep (GitHub, n.d.-a).
- **Push** – To upload local commits to a remote repository, such as one on GitHub (GitHub, n.d.-c).
- **Pull** – To fetch changes from a remote repository and immediately merge them into your current local branch (Atlassian, n.d.).
- **Remote** – A version of the repository that is hosted on the internet or a network, such as on GitHub. By default it is named `origin` (Chacon & Straub, 2014).
- **Repository** – A storage location for a project that contains all of its files and the complete history of changes to them. It is often shortened to "repo" (GitHub, n.d.-a).

---

## References

Atlassian. (n.d.). *Git pull*. Atlassian Git Tutorials. https://www.atlassian.com/git/tutorials/syncing/git-pull

Chacon, S., & Straub, B. (2014). *Pro Git* (2nd ed.). Apress. https://git-scm.com/book/en/v2

GitHub. (n.d.-a). *GitHub glossary*. GitHub Docs. https://docs.github.com/en/get-started/learning-about-github/github-glossary

GitHub. (n.d.-b). *Creating a new repository*. GitHub Docs. https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository

GitHub. (n.d.-c). *Pushing commits to a remote repository*. GitHub Docs. https://docs.github.com/en/get-started/using-git/pushing-commits-to-a-remote-repository

GitHub. (n.d.-d). *GitHub Student Developer Pack*. GitHub Education. https://education.github.com/pack

Instructor. (2026). *Git and GitHub* [PowerPoint slides]. Canvas. _(Replace with your instructor's name, the presentation title, and the course.)_

JetBrains. (n.d.-a). *Free educational licenses*. https://www.jetbrains.com/community/education/#students

JetBrains. (n.d.-b). *Manage projects hosted on GitHub*. WebStorm Help. https://www.jetbrains.com/help/webstorm/github.html

JetBrains. (n.d.-c). *Resolve conflicts*. WebStorm Help. https://www.jetbrains.com/help/webstorm/resolving-conflicts.html

JetBrains. (n.d.-d). *Download WebStorm*. https://www.jetbrains.com/webstorm/download/
