# dxy-and-SNP-wise-dxy
Dxy and SNP-wise Dxy.
The dxy metric calculates all different pairwise comparisons from different populations for each sliding window and divides by all sites. To delete the influence of SNP density, the SNP-wise dxy was derived using the dxy algorithm but modifies the divisor to be the number of comparisons on pairs among SNPs instead of all sites. Notably, SNP-wise dxy is theoretically unaffected by missing genotype information at certain sites. 
The script can be compiled and run on Linux with the flowing steps:
1.Compile the script using g++ v7.2.0:
g++ dxy_SNP_wise_dxy.cpp –o dxy_SNP_wise_dxy
2. Execute the script and direct the output to a results file:
cat your.vcf | dxy_SNP_wise_dxy window_size population1.txt population2.txt > results.txt
