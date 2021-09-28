Found commit of tagged release using
```git rev-list -n 1 v0.0.1```
Create branch from commit ID
```git branch hotfixFromProd commit-id```
Creating a "hotfix" based on main/prod at the point of the release. This file is that hotfix.

Using a single branch deployment method we would deploy based off of the version tag. Create Relase in GitHub UI, based off of the hotfix branch, tag it, and then release.

Useful tidbit:
Checkedout code that was deployed to prod based on commit id retruned from above
```git checkout commit-id```
