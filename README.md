#README for FDR-regression repository

This folder contains the code to fully reproduce the simulations and data analysis in the paper
"A regression framework for the proportion of true null hypotheses" by SM Boca and JT Leek.

Before running the code, please make sure you install the packages swfdr and FDRreg, available at:
https://github.com/leekgroup/swfdr \\
https://github.com/jgscott/FDRreg

The directory structure is as follows:
##BMI GIANT GWAS meta-analysis
This directory contains the code to perform the data analysis and generate Figures 3 and 4, which are saved in the "Figures" subdirectory.
The data must first be downloaded from https://www.broadinstitute.org/collaboration/giant/index.php/GIANT_consortium_data_files#GWAS_Anthropometric_2015_BMI
It is not included here, due to file size limitations.

The file 1.read_in_GIANT.Rmd reads in the data in tsv format and creates the BMI_GIANT_GWAS.RData file. Running it also generates the file 1.read_in_GIANT.pdf.
The file 2.make_Figure_3.Rmd loads BMI_GIANT_GWAS.RData and generates Figure 3 from the paper, saved in Figures/Fig3-1.pdf. Running it also generates the file 2.make_Figure_3.pdf.
The file 3.run_analysis.Rmd loads BMI_GIANT_GWAS.RData and runs our approach for estimating the proportion of true null hypotheses in a regression framework, saving the results to BMI_GIANT_GWAS_results.RData. Running it also generates the file 3.run_analysis.pdf.
The file 4.run_analysis_Scott.Rmd loads BMI_GIANT_GWAS.RData and runs the Scott approach for estimating the proportion of true null hypotheses in a regression framework, saving the results to BMI_GIANT_GWAS_results_Scott.RData. Running it also generates the file 3.run_analysis_Scott.pdf.
The file 5.make_Figure_4.Rmd loads BMI_GIANT_GWAS.RData, BMI_GIANT_GWAS_results.RData, and BMI_GIANT_GWAS_results_Scott.RData and generates Figure 4 from the paper, saved in Figures/Fig4-1.pdf. Running it also generates the file 5.make_Figure_4.pdf.






##simulations.Rnw

This file contains the code to generate Figures 1 and 2.

##diff_samp_size_variances.Rnw

This file contains the code to generate the results for Table 2.

##data_analysis_GIANT.Rmd


##simulations.pdf

Output of simulations.Rnw

##diff_samp_size_variances.pdf

Output of diff_samp_size_variances.Rnw

##data_analysis_GIANT.html

Output of data_analysis_GIANT.html

##figures (directory)

Figures generated by the *.Rnw and *.Rmd files and used in the paper.