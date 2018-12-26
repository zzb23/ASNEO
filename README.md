# _**ASNEO**: **A**lternative **S**plicing **NEO**antigens_

## Introduction
ASNEO is a computational pipeline to identify personalized tumor neoantigens derived from alternative splicing.

## Requriement
### software
* python
* bedtools
* netMHCpan

### python package
* pandas
* sj2psi
* pysam
* biopyton

## Usage
### input
1. Reference genome file: `hg19.fa` or `GRCh37.fa`
2. `STAR` mapped file: `SJ.out.tab` and `indexed bam`(optional)

### example
1. git clone https://github.com/zzb23/ASNEO.git
2. cd ASNEO/example
3. bash run_ASNEO.sh hg19.fa 
> `hg19.fa` should change to your own reference genome file

For detailed usage information, please refer to the [ASNEO User Manual](/doc/AS_User_Manual.md)

## Citation
Zhanbing Zhang, Qi Liu et al. *ASNEO: a computational pipeline to identify Alternative Splicing NEOantigens. 2018*  (**Submitting**)

## Contact
zhangzb@tongji.edu.cn or qiliu@tongji.edu.cn

Tongji University, Shanghai, China
