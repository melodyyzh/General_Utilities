### Pull a remote branch to the local machine 
   a. Use the `-a` option to see all the local and remote branches  
```
git branch -a
example output: 
* main
  remotes/origin/HEAD -> origin/main
  remotes/origin/add_transform_styles
  remotes/origin/main
```  
  b. the `add_transform_style` branch is available remotely but not locally. We then want to checkout this branch
```
git checkout add_transform_style
example output:
branch 'add_transform_styles' set up to track 'origin/add_transform_styles'.
Switched to a new branch 'add_transform_styles'
```
  c. (optional) check if everything is up to date 
```
git pull
```

### Update submodule  
examples: `sphinx-doc/tutorial`
```
git submodule update
```
