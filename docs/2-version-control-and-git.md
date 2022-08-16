[![index.md](assets/back_main_page_icon_124174_32.png)](index.md) [Go to Contents](index.md)

- Git Cofiguration
  - System:
    - /etc/gitconfig
    - Program Files\Git\etc\gitconfig
    - git config --system
  - User:
    - ~/.gitconfig
    - $HOME\.gitconfig
    - git config --global
  - Project:
    - my_project/.git/config
    - git config
- All files are stored in .git folder
- Commit hash index(label)
  - File's in commit Checksum
  - Algorithm: SHA-1("Sha value" - Ша вэлюэ)
- HEAD principles
  1. When changing branches, Git remembers the HEAD of the previous branch and will resume at that commit when the user returns to that branch.
  2. The .git/HEAD file indicates the branch HEAD currently points to, and the contents of the file will contain the SHA of that branch's HEAD.
  If you checkout another branch, the contents of .git/refs/heads/new will not change, but the .git/HEAD contents will.
- Git doesn't want you to change the previos commits
- Reset types
  - Soft reset
  - Mixed reset
  - Hard reset
- Good practice
  - Name branches with Jira ticket name, bugfix, feature, etc. prefixes
  - Name commits in present tens
    - Don't put extra information
    - Be clear and descriptive
  - Every time before any changes try to check project with git status
  - Strategies to reduce merge conflicts 
    - Merge often current branch to master
    - Use feature flag if it is not possible to commit fully completed and tested code
    - Use tracking technick: Periodic merging from master to current branch
    - Small and focused commits
    - Keep lines shot
- Rebase
  1. The first thing to understand about git rebase is that it solves the same problem as git merge.
  2. This moves the entire feature branch to begin on the tip of the main branch, effectively incorporating all of the new commits in main.
  But, instead of using a merge commit, rebasing re-writes the project history by creating brand new commits for each commit in the original branch.
  3. The primary reason for rebasing is to maintain a linear project history.
  4. Advantages:
    - Local Cleanup
    - Incorporating Upstream Changes Into a Feature

----
### Questions:

1) What is GIT?

GIT is a distributed version control system and source code management (SCM) system with an emphasis to handle small and large projects with speed and efficiency.

2) What is a repository in GIT?

A repository contains a directory named .git, where git keeps all of its metadata for the repository. The content of the .git directory are private to git.

3) What is the command you can use to write a commit message?

Git

The command that is used to write a commit message is “git commit –a”.  The –a on the command line instructs git to commit the new content of all tracked files that have been modified. You can use “git add<file>” before git commit –a if new files need to be committed for the first time.

4) What is the difference between GIT and SVN?

The difference between GIT and SVN is

a) Git is less preferred for handling extremely large files or frequently changing binary files while SVN can handle multiple projects stored in the same repository.

b) GIT does not support ‘commits’ across multiple branches or tags.  Subversion allows the creation of folders at any location in the repository layout.

c) Gits are unchangeable, while Subversion allows committers to treat a tag as a branch and to create multiple revisions under a tag root.

5) What are the advantages of using GIT?

a) Data redundancy and replication

b) High availability

c) Only one.git directory per repository

d) Superior disk utilization and network performance

e) Collaboration friendly

f) Any sort of projects can use GIT

6) What language is used in GIT?

GIT is fast, and ‘C’ language makes this possible by reducing the overhead of runtimes associated with higher languages.

7) What is the function of ‘GIT PUSH’ in GIT?

‘GIT PUSH’ updates remote refs along with associated objects.

8) Why GIT better than Subversion?

GIT is an open source version control system; it will allow you to run ‘versions’ of a project, which show the changes that were made to the code overtime also it allows you keep the backtrack if necessary and undo those changes.  Multiple developers can checkout, and upload changes and each change can then be attributed to a specific developer.

9) What is “Staging Area” or “Index” in GIT?

Before completing the commits, it can be formatted and reviewed in an intermediate area known as ‘Staging Area’ or ‘Index’.

10) What is GIT stash?

GIT stash takes the current state of the working directory and index and puts in on the stack for later and gives you back a clean working directory.  So in case if you are in the middle of something and need to jump over to the other job, and at the same time you don’t want to lose your current edits then you can use GIT stash.

11) What is GIT stash drop?

When you are done with the stashed item or want to remove it from the list, run the git ‘stash drop’ command.  It will remove the last added stash item by default, and it can also remove a specific item if you include as an argument.

12) How will you know in GIT if a branch has been already merged into master?

Git branch—merged lists the branches that have been merged into the current branch

Git branch—-no merged lists the branches that have not been merged

13) What is the function of git clone?

The git clone command creates a copy of an existing Git repository.  To get the copy of a central repository, ‘cloning’  is the most common way used by programmers.

14) What is the function of ‘git config’?

The ‘git config’ command is a convenient way to set configuration options for your Git installation.  Behaviour of a repository, user info, preferences etc. can be defined through this command.

15) What does commit object contain?

a)      A set of files, representing the state of a project at a given point of time

b)      Reference to parent commit objects

c)       An SHAI name, a 40 character string that uniquely identifies the commit object.

16) How can you create a repository in Git?

In Git, to create a repository, create a directory for the project if it does not exist, and then run command “git init”. By running this command .git directory will be created in the project directory, the directory does not need to be empty.

17) What is ‘head’ in git and how many heads can be created in a repository?

A ‘head’ is simply a reference to a commit object. In every repository, there is a default head referred as “Master”.  A repository can contain any number of heads.

18)   What is the purpose of branching in GIT?

The purpose of branching in GIT is that you can create your own branch and jump between those branches. It will allow you to go to your previous work keeping your recent work intact.

19) What is the common branching pattern in GIT?

The common way of creating branch in GIT is to maintain one as “Main“

branch and create another branch to implement new features. This pattern is particularly useful when there are multiple developers working on a single project.

20) How can you bring a new feature in the main branch?

To bring a new feature in the main branch, you can use a command “git merge” or “git pull command”.

21) What is a ‘conflict’ in git?

A ‘conflict’ arises when the commit that has to be merged has some change in one place, and the current commit also has a change at the same place. Git will not be able to predict which change should take precedence.

22) How can conflict in git resolved?

To resolve the conflict in git, edit the files to fix the conflicting changes and then add the resolved files by running “git add” after that to commit the repaired merge,  run “git commit”.  Git remembers that you are in the middle of a merger, so it sets the parents of the commit correctly.

23) To delete a branch what is the command that is used?

Once your development branch is merged into the main branch, you don’t need

development branch.  To delete a branch use, the command “git branch –d [head]”.

24) What is another option for merging in git?

“Rebasing” is an alternative to merging in git.

25) What is the syntax for “Rebasing” in Git?

The syntax used for rebase is “git rebase [new-commit] “

26) What is the difference between ‘git remote’ and ‘git clone’?

‘git remote add’  just creates an entry in your git config that specifies a name for a particular URL.  While, ‘git clone’ creates a new git repository by copying and existing one located at the URI.

27) What is GIT version control?

With the help of GIT version control, you can track the history of a collection of files and includes the functionality to revert the collection of files to another version.  Each version captures a snapshot of the file system at a certain point of time. A collection of files and their complete history are stored in a repository.

28) Mention some of the best graphical GIT client for LINUX?

Some of the best GIT client for LINUX is

a) Git Cola

b) Git-g

c) Smart git

d) Giggle

e) Git GUI

f) qGit

29) What is Subgit? Why to use Subgit?

‘Subgit’ is a tool for a smooth, stress-free SVN to Git migration.  Subgit is a solution for a company -wide migration from SVN to Git that is:

a) It is much better than git-svn

b) No requirement to change the infrastructure that is already placed

c) Allows to use all git and all sub-version features

d) Provides genuine stress –free migration experience.

30) What is the function of ‘git diff ’ in git?

‘git diff ’ shows the changes between commits, commit and working tree etc.

31) What is ‘git status’ is used for?

As ‘Git Status’ shows you the difference between the working directory and the index, it is helpful in understanding a git more comprehensively.

32) What is the difference between the ‘git diff ’and ‘git status’?

‘git diff’ is similar to ‘git status’, but it shows the differences between various commits and also between the working directory and index.

33) What is the function of ‘git checkout’ in git?

A ‘git checkout’ command is used to update directories or specific files in your working tree with those from another branch without merging it in the whole branch.

34) What is the function of ‘git rm’?

To remove the file from the staging area and also off your disk ‘git rm’ is used.

35) What is the function of ‘git stash apply’?

When you want to continue working where you have left your work, ‘git stash apply’ command is used to bring back the saved changes onto the working directory.

36) What is the use of ‘git log’?

To find specific commits in your project history- by author, date, content or history ‘git log’ is used.

37) What is ‘git add’ is used for?

‘git add’ adds file changes in your existing directory to your index.

38) What is the function of ‘git reset’?

The function of ‘Git Reset’ is to reset your index as well as the working directory to the state of your last commit.

39) What is git Is-tree?

‘git Is-tree’ represents a tree object including the mode and the name of each item and the SHA-1 value of the blob or the tree.

40) How git instaweb is used?

‘Git Instaweb’ automatically directs a web browser and runs webserver with an interface into your local repository.

41) What does ‘hooks’ consist of in git?

This directory consists of Shell scripts which are activated after running the corresponding Git commands.  For example, git will try to execute the post-commit script after you run a commit.

42) Explain what is commit message?

Commit message is a feature of git which appears when you commit a change. Git provides you a text editor where you can enter the modifications made in commits.

43) How can you fix a broken commit?

To fix any broken commit, you will use the command “git commit—amend”. By running this command, you can fix the broken commit message in the editor.

44) Why is it advisable to create an additional commit rather than amending an existing commit?

There are couple of reason

a)  The amend operation will destroy the state that was previously saved in a commit.  If it’s just the commit message being changed then that’s not an issue.  But if the contents are being amended then chances of eliminating something important remains more.

b) Abusing “git commit- amend” can cause a small commit to grow and acquire unrelated changes.

45) What is ‘bare repository’ in GIT?

To co-ordinate with the distributed development and developers team, especially when you are working on a project from multiple computers ‘Bare Repository’ is used. A bare repository comprises of a version history of your code.

46) Name a few Git repository hosting services

Pikacode
Visual Studio Online
GitHub
GitEnterprise
SourceForge.net