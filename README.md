# slo-pier-weekly data processing


Data structure
* ```raw_dir``` - all raw fastq reads
* ```tagseq-qiime2-snakemake``` - cloned repo for snakemake pipeline



## Steps

### 1. Make qiime2 manifest file
```
# Activate R
conda activate r_3.5.1

# Copy R code to generate manifest file
cp tagseq-qiime2-snakemake/scripts/write-manifest-current.R raw_dir/

# Write manifest file
cd raw_dir
Rscript write-manifest-current.R
```
Check output file: ```manifest-orig.txt```

### 2. Modify config file

Location: ```tagseq-qiime2-snakemake/config.yaml```



