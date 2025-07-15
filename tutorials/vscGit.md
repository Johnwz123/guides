{% set title="VS Code - Working with Git" %}
<frontmatter>
  title: "{{ title }}"
  pageNav: 2
</frontmatter>

<include src="vscode.md#wip-warning" />

# {{ title }}

<box type="info" seamless>

This tutorial is adapted from the [official VS Code Intro to Git tutorial](https://code.visualstudio.com/docs/sourcecontrol/intro-to-git).
</box>

This tutorial covers the basics of using Git in VS Code to manage your source code.

**If you are new to working with Git in VS Code**, we recommend watching the video below for an introduction to Git features wihtin VS Code.

<panel header=":fab-youtube: Using Git with VS Code" peek >

@[youtube](i_23KUAEtUM)

</panel>

**To recall how to use a specific feature**, you can refer to the sections below.

## Prerequisites

<include src="vscCreatingNewJavaProject.md#vsc-java-prereq" />

<box type="warning" seamless>

This tutorial assumes you already understand the basics of Git. It focuses on how to use Git features within VS Code. If you prefer, you can continue using Git commands in your terminal as usual.

</box>

Before you begin, check that Git is installed on your computer. If it isn't, [download and install](https://git-scm.com/downloads) it, then restart VS Code to enable Git features.

<box type="tip" seamless>

You can also sign into VS Code with your GitHub account in the **Accounts** menu.

![Accounts menu](https://code.visualstudio.com/assets/docs/sourcecontrol/intro/vscode-accounts-menu.png)

</box>

## Open a Git Repository

### Clone a repository

To clone a repository to your computer, you can either:

* Open the Command Palette ({{ icon_windows }}/{{ icon_linux}} `Ctrl+Shift+P` | {{ icon_apple }} `Cmd+Shift+P`), then type and select the `Git: Clone` command, or
* In the **Source Control** view ({{ icon_windows }}/{{ icon_linux}} `Ctrl+Shift+G` | {{ icon_apple }} `Cmd+Shift+G`), click the **Clone Repository** button

You can choose to:
* **Clone from GitHub**, or 
  ![GitHub Clone](https://code.visualstudio.com/assets/docs/sourcecontrol/intro/github-clone.png)
* Enter the repository URL and click **Clone from URL**
  ![Git Clone Repository URL](https://code.visualstudio.com/assets/docs/sourcecontrol/intro/git-clone-repository-url.png)

Lastly, select the folder on your computer to clone into. Once cloning is complete, VS Code automatically opens the project folder for you.

### Initialize a repository

To initialize a new Git repository:

1. Open a folder in VS Code
1. In the **Source Control** view ({{ icon_windows }}/{{ icon_linux}} `Ctrl+Shift+G` | {{ icon_apple }} `Cmd+Shift+G`), click the **Initialize Repository** button. This creates a new Git repository in the current folder.

![Initialize Repository](https://code.visualstudio.com/assets/docs/sourcecontrol/intro/scm-init-publish.png)

### Publish local repository to GitHub

You can also publish a local repository to GitHub. This creates a new remote repository under your GitHub account and pushes your local project files to it. Storing your files remotely helps with backup and collaboration.

To publish a local repository to GitHub:

1. In the **Source Control** view ({{ icon_windows }}/{{ icon_linux}} `Ctrl+Shift+G` | {{ icon_apple }} `Cmd+Shift+G`), click the **Publish to GitHub** button.
2. Enter a name and description for the new remote repository and select whether it should be public or private.

![Publish to GitHub](https://code.visualstudio.com/assets/docs/sourcecontrol/intro/publish-to-github.png)

## Staging and Committing Code Changes

After your Git repository is set up, the **Source Control** view will list all the files that have been changed in your workspace.

<box type="tip" seamless>

You can switch between a tree or list view using the icon in the **Source Control** view header.

</box>

![Source Control View](https://code.visualstudio.com/assets/docs/sourcecontrol/intro/source-control-view.png)

Clicking a file shows a diff view that highlights the changes in the file since the last commit.

![Diff view](https://code.visualstudio.com/assets/docs/sourcecontrol/intro/scm-staging.png)

To stage changes, click the `+` icon next to a file. Staged files move to the **Staged Changes** section and will be included in your next commit.

<box type="tip" seamless>

To stage all changes at once, click the `+` icon next to **Changes**.

</box>

![Stage Changes](https://code.visualstudio.com/assets/docs/sourcecontrol/intro/scm-stage-changes.png)

To undo staging, click the `−` icon next to the file, or next to **Staged Changes** to unstage all.

![Unstage changes](https://code.visualstudio.com/assets/docs/sourcecontrol/intro/scm-unstage-changes.png)

To commit your staged changes, enter a commit message in the text box at the top and click the **Commit** button. This creates a commit in the local Git repository.

<box type="tip" seamless>

You can browse and review all past changes and commits for a file in the **Timeline** view at the bottom of the **Explorer** view ({{ icon_windows }}/{{ icon_linux}} `Ctrl+Shift+E` | {{ icon_apple }} `Cmd+Shift+E`).

![Timeline view](https://code.visualstudio.com/assets/docs/sourcecontrol/intro/timeline.png)

</box>

## Pushing and Pulling Remote Changes

After you have made commits to your local Git repository, you will want to push them to your remote repository. The **Sync Changes** button shows the number of commits that will be pushed or pulled. Clicking it will pull any new commits from the remote repository and push your new local commits to the remote repository.

![Sync Changes button](https://code.visualstudio.com/assets/docs/sourcecontrol/intro/sync.png)

<box type="tip" seamless>

You can also push or pull separately using the commands found in the Source Control menu.

![Source Control menu](https://code.visualstudio.com/assets/docs/sourcecontrol/intro/scm-menu.png)

</box>

## Using Branches

The branch indicator in the Status Bar shows the current branch you are on and lets you switch between existing branches or create a new one.

![Branch Indicator](https://code.visualstudio.com/assets/docs/sourcecontrol/intro/branch-indicator.png)

To switch to an existing branch, click the branch indicator and click to choose the branch you wish to switch to.

To create a new branch, click the branch indicator and choose to create a new branch from the current branch or another local branch. Enter a name for the new branch and confirm. VS Code will switch you to the new branch.

![Create branch](https://code.visualstudio.com/assets/docs/sourcecontrol/intro/scm-create-branch.png)

You can push the new branch to the remote repository by clicking **Publish Branch** in the **Source Control** view ({{ icon_windows }}/{{ icon_linux}} `Ctrl+Shift+G` | {{ icon_apple }} `Cmd+Shift+G`). This creates a new branch on the remote repository.
