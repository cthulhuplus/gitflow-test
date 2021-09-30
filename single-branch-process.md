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
