#### VS code 
1. markdown preview  
`(cmd + k) + v`

2. control palette  
`cmd + shift + p`

#### Vim NerdTree
1. show/hide tree   
`fcn + F1 (customized)`
2. toggle between tree and vim window  
`ctrl + W + h/l` or `ctrl + W + </>`

#### Vim remove plugin 
1. add `"` in front of `plugin` in `.vimrc`, save and close
2. open vim, type `:PluginClean`, will prompt `y/n`
3. should source `.vimrc` but I think it does not work.  

#### tmux  
1. scroll mode in tmux
`ctrl + b + [` and `q` to quit scrolling mode 

#### create symbolic link in Unix
`ln -s source_folder myfolder`   
where `source_folder` is the existing directory/file, and `myfolder` is the alias for the symbolic link. `cd myfolder` will go to the source folder. 

#### a preferred way to install a package into conda environment. 
`python3 -m pip install --no-deps . -vv`

#### change multiple at the same time 
1. select the word 
2. cmd+D, continue until all the ones are selected
3. start typing your new word
