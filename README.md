# Gromacs-benchmarking
##system
``` bash
MD system AquaporinRibosomePeptides
atoms 81,743
system size  nm10.8×10.2×9.6
time step /fs 2
cutoff radii  nm1.0
PME grid spacing /nm 0.120
neighbor searching frequency 10 
benchmark steps 10,000
```
## Result
Pure MPI jobs
nodes = 1,4,10,...,50,60,70; ntask-per-node = 16, cpu-per-task = 1; first 6 calculation done only  Xeon silver 4116 processor @ 2.1GHz frequency

![1](https://user-images.githubusercontent.com/43625587/99996966-55dc7e00-2d71-11eb-919c-4f11595bf90b.png)

When it reaches to order of 300 atoms/core speed up doesnt increase linearly with no of nodes anymore due to strong scaling effect. Red line denotes the perfect scale up.


![2](https://user-images.githubusercontent.com/43625587/99996974-57a64180-2d71-11eb-9bc6-89bffa2a2069.png)

Similarly, expected performance(ns/day) does not scale up linearly after 15 nodes. Adding 33% more hardware only added 17% more performance. Eventually, it reaces to a saturation limit.

![3](https://user-images.githubusercontent.com/43625587/99996977-58d76e80-2d71-11eb-81eb-b74041ed1fa1.png)


