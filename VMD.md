#### 1. Change render background
> graphics -> color -> display under "category" -> background -> choose a color

#### 2. Select certain atom 
> graphics -> representation -> select atoms: `index 0 to 20`, or `index 0 20` for discrete points. 

#### 3. Display the distance between 2 atoms
> click 2 on canvas, a cross cursor shows up, select the 2 atoms by clicking on the center. 
> note: the cursor is not very sensitive. Try to reduce the atom display radius to click on the center more accurately. 

#### 4. Make a movie: 
> extension -> visualization -> movie maker -> renderer (choose snapshot) -> movie setting (trajectory, delete image files) -> format (use `MPEG-1 (ffmpeg)`, change compression setting, use 30 as animation frame rate) -> make movie

#### 5. Use TK console in VMD  
This example moves all the atoms by a certain distance
* a. load the molecule 
* b. extension -> TK console -> type `set sel [atomselect top all]` 
* c. type `sel moveby {200, 0, 0}`
* d. type `pbc box`
* in VMD control window, click the first line, then click file -> save coordinates -> write `all` in `selected atoms`, then save the lammpstrj file. 
  