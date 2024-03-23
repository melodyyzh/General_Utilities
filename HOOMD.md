### General notes during HOOMD-dev 
Some are related to different tools such as pytest, but included here anyways. 

#### Pytest: make the test stop on the first error occurred 
`python -m pytest <file> -x -ra`. `-x` means exit first, which terminates the test once it exit, and `-ra` gives more detailed information on the error. 

#### CMAKE: switch between debug mode and release mode in CMake
`cmake -DCMAKE_BUILD_TYPE=Release .` switch to release mode. The default is `Release` mode. 
`cmake -DCMAKE_BUILD_TYPE=Debug .` switch to debug mode.

