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
* step 3: add this directory to your path (check `.bashrc` or `.bash_profile`) 
  `PATH="$HOME/miniconda/bin:$PATH` or append `:$HOME/miniconda/bin` to the existing path.
* step 4: source the `.bashrc` or `.bash_profile` file
* step 5: create conda environment
  `conda create -n myenv python=3.9`
* step 6: `conda init` then `conda activate <env name>`. If still receiving error, try `echo 'source ~/miniconda/etc/profile.d/conda.sh' >> ~/.bashrc` then `source ~/.bashrc`.

#### replace text globally in a text file 
Example: `sed -i 's/Si/1/g'` where `sed` is the stream editor command, `-i` flag means the edit is done in-place rather than send to an output. `s` initiates the substitution command, here we are replacing all the `Si` with `1` using the global flag `g`. 

#### tar and untar a file  
* `tar -czvf compressed_file.tar.gz your_text_file.txt` to tar a file 
* `tar -xzvf compressed_file.tar.gz` to untar a file 