#!/bin/bash

#PBS -N Trinity_heterobasidion
#PBS -j oe
#PBS -l nodes=genom2.local:ppn=40
#PBS -d /gpfs_bkp/HOME/aaksenova/trinity/trinity_out_dir
 


PATH=/home/sharov/SOFT/gcc61/bin:$PATH:$HOME/.local/bin:$HOME/bin
LD_LIBRARY_PATH=/home/sharov/SOFT/gcc61/lib64/:$LD_LIBRARY_PATH
export PATH
export LD_LIBRARY_PATH


Trinity --seqType fq --max_memory 100G --left /gpfs_bkp/AfterDemultiplex/Herobasidion/clean_v2/Herobasidion-2/Herobasidion-2_l12_r4_trim_EC_ATR_c_R1.fastq --right /gpfs_bkp/AfterDemultiplex/Herobasidion/clean_v2/Herobasidion-2/Herobasidion-2_l12_r4_trim_EC_ATR_c_R2.fastq --CPU 40 --output Trinity_HB2
# Trinity
for transcriptome
