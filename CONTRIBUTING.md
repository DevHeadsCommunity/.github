# DevHeads Contribution Guide

DevHeads Community welcomes all contributors.

This document provides a set of guidelines for all open source contributions - logging bug reports, feature requests, 
code submissions / pull requests, etc - so that patches can be quickly accepted into the various projects of the organization.
For the most part, these guidelines apply equally to any project in the organization regardless of programming language or topic. 
Where applicable, we outline where individual projects/languages may have additional requirements.

## Becoming a contributor
### Prerequisites
As a contributor, you will need to be familiar with the specific project(s) from the organization that you want to contribute to. 
How to configure, install and use the project as described in its repository.
You are required to be well-versed in usage of common developer tools that may be used in the project of your choosing.

If you have any questions or want to start a discussion, please feel free to ask in our (Discord)[https://discord.gg/devheads].

### How to Contribute
Now before contributing, we need to ensure things are properly coordinated in order to help you understand all you need to do before 
starting the work. It is recommended that you show your intention to contribute either in the project’s issue tracker or by starting 
a conversation in the project’s discord channel. Whether you already know what contribution to make, or are still searching, the issue 
tracker in the project’s GitHub repository is always the first place to go. Issues will be triaged to categorize them and manage 
workflows for each project, keeping in mind that each repository will manage its issues separately.

### Submitting a Pull Request
All contributions, except trivial changes like typo fixes, must be tied to an existing issue. A contributor should feel free to open 
an issue to discuss their intentions. This gives our maintainers and other contributors insight to what is going on ensuring no 
duplication of efforts and alignment with the goals of the project.

### Good commit messages
Since changes are submitted as Git commits. Each commit has a commit message that describes the change. Commit messages in DevHead’s 
projects follow a specific set of conventions, which we discuss in this section.
```
[area]: [summary of change]

[Commit message body]

[Issue reference]

Signed-off-by: [Your Full Name] <[your.email@address]>	
```

Here is a good example of a good commit message.
```
backend: auth: validate user permission

Ensures the user logged in has enough permissions
for the operation they are about to undertake.

Fixes #67890

Signed-off-by: Jane Smith <jane.smith@devheads.org>	
```

1. First line of the change is a short one-line summary of the change, prefixed by the part of code being changed. It must be:
    a. One line
    b. Must not start with a capital letter, since it is not a complete sentence
    c. Less than 72 characters
    d. Followed by a blank line

2. The commit message body is a description elaborating and providing context for the change and explaining what it does. Should be written in complete sentences with correct punctuation. It must not be empty.  It should show the following if relevant:
    a. What the change does
    b. Why you chose that approach
    c. What assumption were made
    d. How you know it works - tests, for example.
    *Each line in your commit message body must not exceed 75 characters in length.*

3. Referencing issues with the associated change.
4. The commit is completed with a signing off that must use your legal name.

### Review process of Pull Request
When you open a new Pull Request, it will get looked at by a maintainer. The maintainer will examine the submission and provide feedback 
for the contributor. For new contributors typically feedback may focus on the fundamental requirements and frequent oversights. These 
standard checks include:
1. The commit message must follow the prescribed formatting rules. Consistency is insisted upon across each project’s history.
2. Nearly all changes require an associated GitHub issue that documents either the bug being fixed or the feature being implemented. 
Community agreement should already have been reached on the issue tracker before code submission. *Exception to this is purely 
cosmetic adjustments like typo fixes may be accepted with an issue reference.*
3. The existing code style of the project must be strictly followed.
4. In some cases, the documentation must be updated as needed.

## Licensing and Copyright
When contributing with code, you agree to put your changes and new code under the same license as the DevHead’s project of your choice 
unless stated and agreed otherwise.

When changing existing code, you cannot alter the copyright of the original files(s). The copyright will still be owned by the original 
author(s).

By submitting a pull request to any of the DevHead’s projects, you are assumed to have the right to the code or allowed by your employer 
or any other entity to handover the code to DevHeads. We credit you for your changes as far as possible, in order to give credit but also 
to keep track of the people who have made changes. DevHeads requires you to provide your full real name when contributing.

### Contribution Workflow
Contributing to a project involves a series of steps to ensure the changes are consistent with the existing codebase and the project’s 
overall goals.
As discussed above (in the commit section), when contributing to a project, it is important you provide as much information as you 
can about the change you have made, update appropriate documentation (if applicable), and test your changes thoroughly before submitting.

The general GitHub workflow used by DevHeads community uses a combination of Git commands and browser interaction with GitHub. As it 
is with Git, there are multiple ways of getting something done. Here is a description of a typical workflow:
1. Create a fork of your project of choice to your account on GitHub.
2. In your development environment, change into the directory that was created when you cloned the project.

```sh
    cd <project_dir>
```
3. Rename the default remote pointing to the upstream repository from origin to upstream

```sh 
    git remote rename origin upstream
```

4. Now point to your fork with origin.

```sh
    git remote add origin git@github.com/<your_user>/<your_fork>.git
```

5. At this point you are ready to commit and push your changes.
6. Open a [Pull Request (PR)](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request).

