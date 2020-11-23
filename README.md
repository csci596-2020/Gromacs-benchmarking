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
ntask-per-node = 16, cpu-per-task = 1 , no of nodes vary from 1 to 70 , no of cores vary from 1 to 1200
Xeon silver 4116 processor @ 2.1GHz frequency


![1](https://user-images.githubusercontent.com/43625587/99941423-db850d00-2d22-11eb-8dea-ad02f0af071e.png)

performance doesnt increase with nodes due to strong scaling


![2](https://user-images.githubusercontent.com/43625587/99941598-26068980-2d23-11eb-8d01-f6b953a476c0.png)

