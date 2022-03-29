# cloudpool_testing
Messing around with cloudpool


##

Copy 3.7gb from scratch to another place on isilon

```$ /usr/bin/time cp ~/scratch/JI2822_Hifiasm_assembly1.p_ctg.FINAL.fasta .
0.02  user 
5.90  system
0:53.34 elapsed 

```

Copy from isilon to cloudpool

```
/usr/bin/time cp JI2822_Hifiasm_assembly1.p_ctg.FINAL.fasta In_CloudPools/
0.01  user 
3.39  system 
0:35.43 elapsed
```

FAIDX on the isilon

```
time samtools faidx JI2822_Hifiasm_assembly1.p_ctg.FINAL.fasta

real    0m26.682s
user    0m25.509s
sys     0m0.967s
```

FAIDX on cloudpool

```
$ time samtools faidx JI2822_Hifiasm_assembly1.p_ctg.FINAL.fasta

real    0m26.455s
user    0m25.466s
sys     0m0.965s
[mvickers@NBI-HPC interactive In_CloudPools]$
```
