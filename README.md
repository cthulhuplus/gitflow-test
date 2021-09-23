# gitflow-test
In this repository you will find information on Git-Flow
https://nvie.com/posts/a-successful-git-branching-model/
https://github.com/nvie/gitflow
https://jeffkreeftmeijer.com/git-flow/

This was typed on the development branch, branch protections should prevent commits directly to the development branch

First pass at proections did not work, so I had to add additional branch protections to prevent direct commits to main and development. They are now working and this comment is from feature branch add-comment-about-proections which was created with this command:

git flow feature start add-comment-about-protections

Since Git-Flow takes a local first approach the branch is created locally first. When you want to push code up to GitHub remote you will need to run a command like this to create the branch on the remote/origin and push the code up

git push --set-upstream origin feature/add-comment-about-protections

To finish the feature we are going to make one last commit to this branch, then create a Pull Request to merge changes from add-comment-about-protections to the development branch. Once the PR requirements/protections have been satisfied we will run the below command:

git flow feature finish add-comment-about-protections

This will close this branch, merge the changes onto the development branch and checkout the development branch. We will then need to run a git push to move the new code to the development branch which will close the PR.
