# Rebase vs Merge

> Both git merge and git rebase are used to merge branches. There is one difference between them. The difference lies in the commit history after you integrate one branch into another.

## Merge
* keeps the history
* rule: use to combining tasks from local branch to public branch
* pros: good for integrating code received from others
* cons: it makes hard for someone to understand and follow what’s going on at a particular stage when there are multiple merges

## Rebase
* quite literally change the "base" branch on top of the other
* doesn't preserve the history ("rewrites" history)
* acceptable for code that you have never shared with others
* rule: use to combining tasks from public branch into local branch
* pros: makes the repo look cleaner and is much easier to look at
* cons: might be a lot of conflicts while doing a rebase

## Example

```
git rebase origin/master
```
**What happaned:**

1) got all commits from master as is
2) my commits were moved on top of it, no difference what time they were made
3) in addition, my commits *hash* numbers were changed

## Illustration

![](https://miro.medium.com/max/1710/1*pzT4KMiZDOFsMOKH-cJjfQ.png)

## Links
[https://www.quora.com/What-is-the-difference-between-rebase-and-merge-in-Git](https://www.quora.com/What-is-the-difference-between-rebase-and-merge-in-Git)
[https://medium.com/datadriveninvestor/git-rebase-vs-merge-cc5199edd77c](https://medium.com/datadriveninvestor/git-rebase-vs-merge-cc5199edd77c)
