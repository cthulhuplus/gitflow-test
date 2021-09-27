# Git Flow Process/Procedure

Process/Procedure using the git-flow tool in git-flow.md

Process/Procedure using adapted standard git flow in git-process.md

Create your branch however you see fit

When branch is ready to merge into development, create PR

When PR is ready, complete the PR

When ready to do a release create a release branch from development to merge into main

Merge release branch (development) into main using the "ours" strategy
```git merge -s ours main```

Push merged release branch to GH
```git push --set-upstream origin bbrooks/OverwriteDevWithMain```

Create a PR for release branch into main, should be good to go

Create release in GH via the UI from main

