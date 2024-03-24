### Linux system - general
#### create symbolic link in Unix
`ln -s source_folder myfolder`   
where `source_folder` is the existing directory/file, and `myfolder` is the alias for the symbolic link. `cd myfolder` will go to the source folder. 

#### a preferred way to install a package into conda environment. 
`python3 -m pip install --no-deps . -vv`