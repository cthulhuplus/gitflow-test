# Testing Scenarios
## Multi-Branch
### Deploy feature to development (default) branch
* Create a new branch

```git checkout -b bbrooks/newFeature development (probably)```
* Make changes to branch, push changes to GitHub

```git push --set-upstream origin bbrooks/newFeature```

```git push -u origin bbrooks/newFeature```
* Create PR in GitHub UI
* Satisfy PR Requirements
* Squash & Merge
* Delete the branch

### Deploy development to main (production) and create release
* Create branch from main branch

```git checkout -b bbrooks/RC1.0.0 main```
* Overwrite development branch on top of it

```git merge -X theirs development```
* This will take the development branch, not do a file comparison, and overwrite the main branch
* Create PR in UI for release branch into main branch (should be 0 conflicts)
* Satisfy PR Requirements
* Squash & Merge
* Delete Branch
* Create release in GitHub UI
 * Create tag, target main branch
 * Publish when ready

### Deploy hotfix to main and development branches
* Create branch from main branch

```git checkout -b bbrooks/HF1.0.1 main```
* Make bug fixes
* Push fixes up

```git push --set-upstream origin bbrooks/HF1.0.1```
* Create PR for HF1.0.1 to be merged into main
* Satisfy PR Requirements
* Squash & Merge
* Create release in GitHub UI
 * Create tag, target main branch
 * Publish when ready

* Create PR for HF1.0.1 to be merged into development (might be easier to create a new branch with the HF based on development depending on merge conflicts)
* Satisfy PR Requirements
* Squash & Merge
* Delete the branch


## Single Branch
### Deploy feature to default branch (development)
* Create a new branch

```git checkout -b bbrooks/newFeature development (probably)```
* Make changes to branch, push changes to GitHub

```git push --set-upstream origin bbrooks/newFeature```

```git push -u origin bbrooks/newFeature```
* Create PR in GitHub UI
* Satisfy PR Requirements
* Squash & Merge
* Delete the branch

### Create release
* When default branch (development) is ready for release
* Create release in GitHub UI
 * Create tag, target main branch
 * Publish when ready

### Hotfix/Revert to previous state (release)
* Find commit of tagged release

```git rev-list -n 1 v1.0.0```
* Create branch from commit ID

```git branch bbrooks/release1.0.1 $commit-id```
* Create a hotfix branch (hotfix1.0.1) from the new branch (release1.0.1)
* Create the fix on hotfix branch
* Create PR of hotfix branch into branch created from release (release1.0.1)
* Satisfy PR Requirements
* Squash & Merge
* Create release in GitHub UI
 * Create tag (v1.0.1), target release branch (release1.0.1)
 * Publish when ready
* Delete hotfix branch
* Delete release branch?

Useful tidbit:
Checkedout code that was deployed to prod based on commit id retruned from above

```git checkout commit-id```