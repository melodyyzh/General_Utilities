#### 1. Pull a remote branch to the local machine 
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

#### 2. Update submodule  
examples: sphinx-doc/tutorial is a submodule, and git add will not stage the submodule. Use:

`git submodule update`

#### 3. list git configuration 
`git config --list`

#### 4. set up remote origin (double check when is it needed)
`git remote set-url origin git@github.com:glotzerlab-hoomd-blue.git`

#### 5. `git reset` and `git revert`
* `git reset` unstages a file or discard commits in a private branch
* `git revert` undo a commit to a public branch

#### 6. Add SSH passphrase to an SSH agent
When we create a SSH key, we create a public-private key pair. The SSH key has been encrypted with a passphrase, and when you perform operations that requires authentication, SSH prompt the passphrase to unlock the private key.   
* a. start the SSH agent with `eval $(ssh-agent)`  
* b. add the private key to it with `ssh-add`
* c. it will ask you for your passphrase once and add the identity.

#### 7. View local commits that has not been pushed yet
`git log --branches --not --remotes`
