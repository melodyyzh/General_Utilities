### Linux system - general
#### create symbolic link in Unix
`ln -s source_folder myfolder`   
where `source_folder` is the existing directory/file, and `myfolder` is the alias for the symbolic link. `cd myfolder` will go to the source folder. 

#### a preferred way to install a package into conda environment. 
`python3 -m pip install --no-deps . -vv`

#### install conda environment on HPC clusters [https://rabernat.medium.com/custom-conda-environments-for-data-science-on-hpc-clusters-32d58c63aa95]
* step 1: install miniconda  
  `wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh -O miniconda.sh`
* step 2: "specify the install directory within your home directory, rather in the default system-wide installation (which you won’t have permissions to do)".   
  `bash miniconda.sh -b -p $HOME/miniconda export`
* step 3: add this directory to your path  
  `PATH="$HOME/miniconda/bin:$PATH`
* step 4: create conda environment
  `conda create -n myenv python=3.9`
