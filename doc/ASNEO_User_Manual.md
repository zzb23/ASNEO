# _ASNEO: Alternative Splicing NEOantigens_

## Introduction
ASNEO is a computational pipeline to identify personalized tumor neoantigens derived from alternative splicing.

## Requriement
### software
* python
* bedtools
* netMHCpan
* netCTLpan

### python package
* pandas
* sj2psi
* pysam
* biopyton

## Usage

### Parameters

* ##### Requiered

  * -j, --junc

	Junction file, the default format is STAR result SJ.out.tab.  You can also specific your own format by columns names in your junction file and setting --columns. 

  * -g, --genome

	Reference genome file, must be hg19 or GRCh37 .

* ##### Optional

  * -l, --length

	Peptide length [8-11], default "9". if multiple, seperated with ",", such as 8,9,10,11.

  * -a, --allele

	HLA allele, default "HLA-A02:01". Multiple seperated with ",". You can using OptiType or Seq2HLA to detect it with RNA-seq.

  * -p, --process

	Multiple processes, default "10".

  * -o, --outdir

	Output directory, default "result".

  * --reads

	Cutoff of junction reads number, default "10". Only junctions whose unique reads number greater than it will be remained.

  * --psi

	Cutoff of psi value(0-1), default 0.1.  [See PSI means here][https://github.com/olgabot/sj2psi].

  * --bind

	Cutoff of bind rank,  default 2. 0.5 was high binding peptides rank threshold(SB), 2 was low binding peptides rank threshold(WB).

  * --bam

	Bam file, default None. Our software apply a simple caculation of RPKM to filter neoantigens. If you want to use it, specific the indexed bam file. You can also filter the neoantigens by yourself after process done with your own express caculation. 

  * --rpkm

	Cutoff of RPKM value, default 1.0. Only useful when you set --bam.

  * --columns

	If junction file contain columns names. If set, at least contain "chrom, intron_start, intron_stop, unique_junction_reads". Note: the intron coordinates must be 1-based and columns must be sperated by Tab.


### Example

1. git clone https://github.com/zzb23/ASNEO.git

2. cd ASNEO/example

3. bash run_ASNEO.sh hg19.fa
> `hg19.fa` should change to your own reference genome file (must be hg19 or GRCh37)


## Citation
TODO

## Contact
zhangzb@tongji.edu.cn or qiliu@tongji.edu.cn

Tongji University, Shanghai, China
