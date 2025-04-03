### 1. Pull a remote branch to the local machine 
  a. Use the `-a` option to see all the local and remote branches  
`git branch -a` 
example output: 
```
main
remotes/origin/HEAD -> origin/main
remotes/origin/add_transform_styles
remotes/origin/main
```  

  > alternative ways to show branch details  
  > `git branch -v` and `git branch -vv` 
  > these commands will show:
  > 1. local branches
  > 2. commit hash it points to
  > 3. upstream branch  

  b. the `add_transform_style` branch is available remotely but not locally. We then want to checkout this branch
```
git checkout add_transform_style
example output:
branch 'add_transform_styles' set up to track 'origin/add_transform_styles'.
Switched to a new branch 'add_transform_styles'
```
  c. (optional) check if everything is up to date   
`git pull`

In case of the repositories forked from the original repository like the al_driver repo in the Lindsey Lab, the operation is different. Here, we have the `LL/al_driver-LLfork` on github, the forked repo `al_driver-myfork` on github, and the local clone `al_driver-myfork`. We create a new branch called `develop` in the `LL/al_driver-LLfork`, and next we need to make sure that we have access to the `develop` branch in myfork and local clone. 
  a. `git remote add al_driver-LLfork git@github.com:LindseyLab-umich/al_driver-LLfork.git` 
  b. `git remote -v` will show the following message: 
  ```
  al_driver-LLfork	git@github.com:LindseyLab-umich/al_driver-LLfork.git (fetch)
  al_driver-LLfork	git@github.com:LindseyLab-umich/al_driver-LLfork.git (push)
  origin	git@github.com:melodyyzh/al_driver-myfork.git (fetch)
  origin	git@github.com:melodyyzh/al_driver-myfork.git (push)
  ```
  c. `git fetch al_driver-LLfork`  
  d. `git branch -a` shows both remote and local branches   
  e. `git checkout develop` switch the branch to `develop`  
  f. `git push origin develop` adds this branch to `al_driver-myfork`  

### 2. Create a local branch and push to remote 
  > first create a local branch and check it out: `git checkout -b <branch-name>`
  > then push the branch to remote: `git push --set-upstream origin <branch-name>` 

### 3. Update submodule  
examples: sphinx-doc/tutorial is a submodule, and git add will not stage the submodule. Use:

`git submodule update`

### 4. list git configuration 
`git config --list`

### 5. set up remote origin (double check when is it needed)
`git remote set-url origin git@github.com:glotzerlab-hoomd-blue.git`

### 6. `git reset` and `git revert`
* `git reset` unstages a file or discard commits in a private branch. 
  * To delete the most recent commit but keep the work you've done, execute: 
  `git reset --soft HEAD~1`
  * the following command will destroy the work you've done: 
  `git reset --hard HEAD~1`
* `git revert` undo a commit to a public branch
* `git reset HEAD~ ` undo a local commit

### 7. Add SSH passphrase to an SSH agent
When we create a SSH key, we create a public-private key pair. The SSH key has been encrypted with a passphrase, and when you perform operations that requires authentication, SSH prompt the passphrase to unlock the private key.   
* a. start the SSH agent with `eval $(ssh-agent)`  
* b. add the private key to it with `ssh-add`
* c. it will ask you for your passphrase once and add the identity.

### 8. View local commits that has not been pushed yet
`git log --branches --not --remotes`

### 9. add all the unstaged deleted files at once
`git add -u`