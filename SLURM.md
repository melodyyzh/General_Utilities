### SLURM commands
#### 1. check what jobs are currently running on a certain node.  
`squeue -l -w <node_name>`  
The node name can be found using:   
`squeue -u <username> `

#### 2. show details of the pending job
`scontrol show job <job-id>`

#### 3. relation between node, processor(cpu/gpu), and core
* a node is a cluster
* 1 node has certain number of processors
* 1 processor contains certain number of cores

#### 4. threads vs tasks 
* each calculation step has one or more parallel tasks
* task is connected to mpi, put 1 test in a core
* thread is when a process have multiple tasks that perform independently. 

#### 5. log into certain node and see cpu usage 
* for greatlake: `ssh <username>@<node_name>.arc-ts.umich.edu`
* see how many cpu is actually being used: `top/htop`

