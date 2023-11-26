# Assessing the impact of government financial support from Hilfe Program on small and medium-sized (SMEs) in Germany: a survey-based analysis of COVID-19’s influence on company economic performance

The project aims to explore the impact of financial support on the performance of SMEs and identify the factors influencing the effectiveness of fundings. We use a confidential survey wave 4 data provided by German Business Panel (GBP), encompassing feedback from German companies on company information, funding reception details, and performance expectations.

## Authors
 Minal Singhania
 Lan Luo
 Academic Supervisor : Prof. Stefan Bender
 
## Data

To study this topic we have used confidential wave 4 data of the survey "Accounting Transparency and Reporting, Tax Misperceptions, Key Financial Performance Indicators, and Changing Business Conditions During and Beyond the COVID-19 Crisis" provided by GBP and accessed strictly from Mannheim University.

Detailed information about the data can be found under this link https://gbpanel.org/page/datensatze using GBP Codebook: Survey Round 4.



## Repository Structure

For the purpose of reproducibility and version control Git is used to create an existing repository. The current repo Master_Thesis is further divided into Scripts and Data .

Data folder contains merely the test data used .

Script contains the Rmarkdown code using which analysis has been performed.There are 2 scripts to explicitly work with weighted and un-weighted data. 
GBP_Corona_Analysis_Final_survey_wts.Rmd works with weighted sampled data
GBP_Corona_Analysis_noweights_final.Rmd is for un-weighted analysis

## Data Model

For our analysis we have used GBP_data.csv file, the test version of the same is also published in git.To generate the results and necessary plots which are used to carry out the analysis update the path "data" to the location of csv file.

The file contains demographic information about the companies participating in the survey.For our study we were particularly interested in Company's location,  employee count, reported revenue in previous year, industry type, sampling weights, types for goverment funds opted and key kpis.
Detailed information on the dataset and survey question can be found on the website.

The study is restricted to access the impact of 3 government aids which are Soforthilfe, Kurzarbeit and KfW programs therefore any other types of aid are not considered during further coarse of action. Using these funds we draw a parallel between company's performance which is measured using variable Expected change in revenue and profit between funded and non funded companies.

We have used exploratory data analysis to study the data and its correlation between variables, regression and propensity score matching to study the impact of confounding variables on the KPIs.





## Session Info
For the purpose of reproducibility below packages and software version we used to produce this report.

R version 4.1.2 (2021-11-01)
Platform: x86_64-apple-darwin17.0 (64-bit)
Running under: macOS Catalina 10.15.7

Matrix products: default
BLAS:   /System/Library/Frameworks/Accelerate.framework/Versions/A/Frameworks/vecLib.framework/Versions/A/libBLAS.dylib
LAPACK: /Library/Frameworks/R.framework/Versions/4.1/Resources/lib/libRlapack.dylib

locale:
[1] en_US.UTF-8/en_US.UTF-8/en_US.UTF-8/C/en_US.UTF-8/en_US.UTF-8

attached base packages:
[1] grid      stats     graphics  grDevices utils     datasets  methods  
[8] base     

other attached packages:
 [1] epade_0.5.1     plotrix_3.8-2   car_3.1-0       carData_3.0-5  
 [5] lubridate_1.9.2 forcats_1.0.0   purrr_1.0.1     readr_2.1.4    
 [9] tibble_3.2.0    tidyverse_2.0.0 Rcpp_1.0.10     sandwich_3.0-1 
[13] lmtest_0.9-39   zoo_1.8-9       MatchIt_4.5.3   srvyr_1.2.0    
[17] ggplot2_3.4.1   tableone_0.13.2 stringr_1.5.0   tidyr_1.3.0    
[21] dplyr_1.1.0     survey_4.1-1    survival_3.2-13 Matrix_1.5-1   

loaded via a namespace (and not attached):
 [1] bitops_1.0-7        RColorBrewer_1.1-2  tools_4.1.2        
 [4] backports_1.4.1     utf8_1.2.2          R6_2.5.1           
 [7] rpart_4.1.16        Hmisc_4.6-0         DBI_1.1.2          
[10] colorspace_2.0-2    nnet_7.3-16         withr_2.5.0        
[13] tidyselect_1.2.0    gridExtra_2.3       compiler_4.1.2     
[16] cli_3.6.0           htmlTable_2.4.0     labeling_0.4.2     
[19] caTools_1.18.2      scales_1.2.1        checkmate_2.0.0    
[22] askpass_1.1         digest_0.6.29       foreign_0.8-81     
[25] rmarkdown_2.11      wdman_0.2.5         base64enc_0.1-3    
[28] jpeg_0.1-9          pkgconfig_2.0.3     htmltools_0.5.2    
[31] fastmap_1.1.0       htmlwidgets_1.5.4   rlang_1.1.0        
[34] rstudioapi_0.14     farver_2.1.0        generics_0.1.2     
[37] magrittr_2.0.3      Formula_1.2-4       munsell_0.5.0      
[40] fansi_1.0.3         abind_1.4-5         lifecycle_1.0.3    
[43] stringi_1.7.6       chk_0.9.0           yaml_2.3.5         
[46] MASS_7.3-54         crayon_1.5.1        semver_0.2.0       
[49] lattice_0.20-45     splines_4.1.2       hms_1.1.2          
[52] knitr_1.37          pillar_1.8.1        XML_3.99-0.8       
[55] glue_1.6.2          evaluate_0.14       mitools_2.4        
[58] latticeExtra_0.6-29 data.table_1.14.2   vctrs_0.5.2        
[61] png_0.1-7           tzdb_0.2.0          gtable_0.3.0       
[64] openssl_2.0.0       assertthat_0.2.1    xfun_0.29          
[67] binman_0.1.2        RSelenium_1.7.7     cluster_2.1.2      
[70] timechange_0.2.0    ellipsis_0.3.2  