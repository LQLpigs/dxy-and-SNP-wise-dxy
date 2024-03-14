# dxy-and-SNP-wise-dxy
Dxy and SNP-wise Dxy.
The dxy calculates all different pairwise comparisons from different populations on each sliding window divided by all sites, to delete SNP density influence, the SNP-wise dxy was generated according to dxy algorithm using the number of comparisons on pairs for each SNP to replace all sites to be divided. Significantly, the SNP-wise dxy is theoretically not influenced by the genotype information missing in sites. The usage for this C++ manual script in linux has two steps:
g++ dxy_SNP_wise_dxy.cpp –o dxy_SNP_wise_dxy.
cat you.vcf | dxy_SNP_wise_dxy window_size population1.txt population2.txt > results.txt.
You need to prepare the SNP calling file (VCF) and files of samples id for two populations, and set the sliding window size.
