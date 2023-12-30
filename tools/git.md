# Git

Git is a version control system (VCS).

## Official Documentation

The following links will cover installation and usage of Git in a local environment.

Overview of version control: \
https://git-scm.com/about

Installation: \
https://git-scm.com/downloads

Reference: \
https://git-scm.com/docs

## Common commands

Display current branch and file status:
```bash
git status
```

Create a new branch:
```bash
git checkout -b [NEW_BRANCH_NAME]
```

Switch to an existing branch:
```bash
git checkout [BRANCH_NAME]
```

Display current changes:
```bash
git diff
```

Add all current changes to be staged for a commit:
```bash
git add .
```

Commit all currently staged changes with a relevant description as the message:
```bash
git commit -m 'do a thing'
```

Show a detailed history of Git commits:
```bash
git log
```

Show a concise history of Git commits:
```bash
git log --pretty=oneline
```

Pull changes from remote repository:
```bash
git pull
```

Pull changes from remote repository, without updating your local branches:
```bash
git fetch
```

Push changes to a remote repository:
```bash
git push origin [BRANCH_NAME]
```

## Remote Repository Platforms

In order to easily access a project from multiple computers, a Git project must be pushed up from a local environment to a remote repository. GitHub and GitLab are the most popular remote repository platforms. GitHub is more popular for open-source and personal projects, whereas GitLab is more popular for enterprise development. The following walkthrough will focus on GitHub.

### Pushing code to remote repository

Create a free account on GitHub:
https://github.com/

In your local environment, generate SSH keys using the following procedure: \
https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

In your GitHub account settings, add your new **public** SSH key to your profile using the following procedure: \
https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account

> [!CAUTION]
> Be careful that your **PUBLIC** key is added.
> 
> Your private key should never leave your local environment. For more on the signficance of public and private keys, see the following:
> 
> https://www.ssh.com/academy/ssh/public-key-authentication

On your GitHub profile, create a new repository with the same name as your local project. Make sure that you do **NOT** select to create the repository with a README, .gitignore, or license.

Once you create a new repository on your profile, you should see instructions on how to push from your local. However, you must make sure that all of your local changes are committed. Use the following command to commit **all** current changes, including any new files:

```bash
git add . && git commit -m 'made some changes to files'
```

In your local environment, set the new repository as your remote:
```bash
git remote add origin git@github.com:[YOUR_ACCOUNT]/[YOUR_PROJECT_NAME].git
```

Push your local project up to the remote repository:
```bash
git push -u origin main
```

> [!NOTE]
> If you get a Git error asking for your name and email, use the command output to set the global Git config for the username and email that you used for your GitHub profile.

