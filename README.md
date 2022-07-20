# Liu Lab Notes

[workflowr]: https://github.com/workflowr/workflowr
[Liu Lab]: https://liulab.uchicago.edu/

This repository contains a workflowR setup. 

## In order to get started:

```
mkdir -p path/to/store/labwebsite
cd path/to/store/labwebsite
git clone https://github.com/XuanyaoLiuLab/LiuLabNotes.git
cd LiuLabNotes
```

If you have not yet setup workflowr, see the 'WorkflowR Tutorial' for step-by-step instructions on setting up an environment on either your local machine or Midway3/Midway2.

## Link to lab website pages:
### [website](https://xuanyaoliulab.github.io/LiuLabNotes/)

## Best Practices

This section outlines best practices to follow when there are multiple people working on a github repository at once. 

  0. Move into the lab website directry: path/to/LiuLabNotes from above
  1. After you've selected a feature to work on, create a branch in your local repo to build it in.
      * `$ git checkout -b username/short_description_of_feature`
  2. Implement the requested feature, make sure all tests are passing, and commit all changes in the new branch. In our case, this would be to run wflow_publish() on the modified .RMD workflowR pages.
  3. Checkout the master branch locally.
      * `$ git checkout master`
  4. Pull down the master branch from GitHub to get the most up to date changes from others. If you practice git workflow as described here you should never have a merge conflict at this step.
      * `$ git pull origin master`
  5. Make sure all tests are passing on master and then checkout your new branch.
      * `$ git checkout username/short_description_of_feature`
  6. From your new branch, merge in your local master branch.
      * `$ git merge master`
  7. Resolve any merge conflicts, make sure all tests are passing on the new branch, and then commit all changes from the merge.
      * `$ git add .`
      * `$ git commit -m "Merge in master."`
  8. Push the feature branch to the remote repo.
      * `git push --set-upstream origin username/short_description_of_feature`
  9. Submit a pull request on GitHub asking to merge the branch into master.
  10. A teammate reviews the code for quality and functionality.
  11. The teammate merges the pull request and deletes your branch from GitHub.

