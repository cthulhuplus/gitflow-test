# Testing Scenarios
## Multi-Branch
Deploy feature to development (default) branch
* Create a new branch
```git checkout -b bbrooks/newFeature development (probably)```
* Make changes to branch, push changes to GitHub
```git push --set-upstream origin bbrooks/newFeature```
```git push -u origin bbrooks/newFeature```
* Create PR in GitHub UI
* Satisfy PR Requirements
* Squash & Merge
* Delete the branch
Deploy development to main (production) and create release
Deploy hotfix to main and development branches

## Single Branch
Deploy feature to "main"
Create release
Hotfix/Revert to previous state (release)