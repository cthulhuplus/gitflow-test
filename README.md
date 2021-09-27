<<<<<<< HEAD
# Git Flow Process/Procedure
=======
# gitflow-test
In this repository you will find information on Git-Flow

https://nvie.com/posts/a-successful-git-branching-model/
https://github.com/nvie/gitflow
https://jeffkreeftmeijer.com/git-flow/
>>>>>>> 2da5150f743d643a7302066c7db57f39c000f5ce

Process/Procedure using the git-flow tool in git-flow.md

Process/Procedure using adapted standard git flow in git-process.md

<<<<<<< HEAD
=======
git flow feature start add-comment-about-protections

Since Git-Flow takes a local first approach the branch is created locally first. When you want to push code up to GitHub remote you will need to run a command like this to create the branch on the remote/origin and push the code up

git push --set-upstream origin feature/add-comment-about-protections

To finish the feature we are going to make one last commit to this branch, then create a Pull Request to merge changes from add-comment-about-protections to the development branch. Once the PR requirements/protections have been satisfied we will click Squash & Merge in the GitHub UI.

The checkout the development branch locally, pull the most recent changes and then run:

git flow feature finish add-comment-about-protections

This will close the feature branch and get us ready to start a new feature branch.


This was typed on the main branch, branch protections should prevent commits directly to the main branch

When ready for a release use:

git flow release start NameOfRelease/Branch

Push it to GitHub
git flow release publish NameOfRelease/Branch

Publish Release
git flow release finish NameOfRelease/Branch

Resolve any merge conflicts

Create PR for Main <- Release Branch

Create PR for Development <- Release Branch

Close Release in GitHub UI from main (production = main)
>>>>>>> 2da5150f743d643a7302066c7db57f39c000f5ce
