#Git

#####What is git and why is it used?

In software development, many people will be working on a single project. Many people may want to edit a single file at once. So, we need to control edits to a file from multiple developers. We also want to keep track of our code changes over time to be able to revert to earlier versions of the project if necessary. 

The term for a mechanism such as this is a version control system or VCS. Several VCSs exist such as SVN, CVS, Clearcase, Mercurial... the list goes on. This article will focus on Git. 

Git differs from other version control systems in that Git does NOT store information as a list of file-based changes. Instead, each version is a snapshot where if files have not changed, git will not store the file again, instead it links to the file that already exists. More on this later. 


#####Useful definitions 

Repository - the place where the files for the project are stored. 

#####File lifecycle 

Untracked -> A file which exists outside of the repository. The file is not being version controlled and changes you make to this file will not be tracked.
 
Unmodified -> A file in the repository which has NOT been edited yet. 

Modifed -> A file in the respository which HAS been edited, but the changes have not yet moved to the staging area.

Staged -> A file moved to the staging area which is ready to be commited to the next snapshot. 

Examples: https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository









