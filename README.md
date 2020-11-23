# Gromacs-benchmarking
Strong scalling test using Gromacs2020 on Discovery cluster

## system
``` bash
MD system             Aquaporin
No of atoms           81,743
system size/nm        10.8×10.2×9.6
timestep /fs          2
cutoff radiinm        1.0
PME grid spacing /nm  0.120
benchmark steps       16,000
```
## Result
Pure MPI jobs
nodes = 1,4,10,...,50,60,70; ntask-per-node = 16, cpu-per-task = 1; first 6 calculation done only on Xeon silver 4116 processor @ 2.1GHz frequency

![1](https://user-images.githubusercontent.com/43625587/100000554-968ac600-2d76-11eb-9618-eee054e1ad2c.png)

When the simulation reaches to **less than 300 atoms/core** speed up does **not** increase linearly with no of nodes anymore. Red line denotes the perfect scale up.


![2](https://user-images.githubusercontent.com/43625587/99996974-57a64180-2d71-11eb-9bc6-89bffa2a2069.png)

Similarly, expected performance(ns/day) does not scale up linearly after 15 nodes. As we change the number of nodes from 15 to 20, adding 33% more hardware only adds 17% more performance. Eventually, it reaces to a saturation limit.

![3](https://user-images.githubusercontent.com/43625587/99996977-58d76e80-2d71-11eb-81eb-b74041ed1fa1.png)


