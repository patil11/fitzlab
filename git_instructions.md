Git Instructions
=================


# Introduction to Basic Usage

Git is a bit odd and takes some getting used to, but is very simple. Key to remember, is that if you have multiple branches ensure that you are working on the correct branch. Ensure that you are up-to-date as well before making local changes. Right now I have two repositories: 

1. fitzlab This is in ucla/labdata/docs/fitzlab
2. fitzmed This is in ucla/clinical/ABXDosing/fitzmed
	

To clone the master and all associated branches:

	git clone git://github.com/agregson/fitzlab.git
	
To get something up-to-date I think the following will work while you are in the directory. fetch does not merge or modify the local contents, it just pulls down from the repository anything that is not already local. 

	git fetch 
	
Then we edit a file and or add new files then we have to add an edited file or a new file (edited files need to be added even though they are already added).

	git add <filename>
	
	git status

The status command will tell us what we are about to commit. Then we do a commit to stage them to be added with the next push:

	git commit -m "what we did in the commit"
	
	git push fitzlabh master
	
That last "master" could be the name of a branch that we are working on instead of the master. To see what remotes you have to push to:

	git remote -v
	
and also to check and see which branch you are working on:	

	git branch -v

To start working on a different branch, or to switch back to the master repository:

	git checkout master

where master can be replaced with a branch name. To create a new branch:

	git branch NewBranchname

## Check out just one branch

	git clone <url> --branch <branch> --single-branch <folder>
	
Or for us, say we want to checkout just the LSR II branch:

	git clone git://github.com/agregson/fitzlab.git --branch lsrii --single-branch nameoflocalfolder
	

# General Pandoc Instructions

An example to convert to pdf.

``pandoc abstract_jove.md --biblio ~/Documents/jabref/JabRefdb/gnr-new.bib --csl journal-of-visualized-experiments.csl --latex-engine=xelatex -o abstract_jove.pdf``