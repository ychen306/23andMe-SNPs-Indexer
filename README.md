Utility program to index 23andMe's SNPs data
### Dependency
This script requires pyasm. Simply `pip install pysam` will do the job.  
### Usage
* You will need to download 23andMe's [file](https://api.23andme.com/res/txt/snps.data) which contains the translation between SNP id and corresponding chromosome and chromosomal position.
* Here's how you MIGHT do it
```
# download file from 23andMe
$ wget https://api.23andme.com/res/txt/snps.data -O snps.txt
# index it
$ ./index_snps snps.txt snps.sorted.txt
```
* After using commands above, you will have three new files in the directory you issued the commands -- `snps.sorted.txt`, `snps.sorted.gz`, `snps.sorted.gz.tbi`. `snps.sorted.txt` is the sorted csv file containing the snps (without headers). `snps.sorted.gz` and `snps.sorted.gz.tbi` are tabix-compressed files of `snps.sorted.txt`.
