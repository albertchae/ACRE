---
output:
  word_document: default
  html_document: default
---
# Reproduction Diagrams  

## Different Scenarios

JOEL: PLease fill-in. 

### Complete
          table 1
            └───[code] formatting_table1.R
                ├───output1_part1.txt  
                |   └───[code] output_table1.do           
                |       └───[data] analysis_data01.csv
                |          └───[code] data_cleaning01.R
                |             └───[data] survey_01raw.csv
                └───output1_part2.txt  
                    └───[code] output_table2.do           
                        └───[data] analysis_data02.csv
                           └───[code] data_cleaning02.R
                              └───[data] admin_01raw.csv  



### Raw data and analytic data, but cleaning code is missing.
          table 1
            └───[code] formatting_table1.R
                ├───output1_part1.txt  
                |   └───[code] output_table1.do           
                |       └───[data] analysis_data01.csv
                |          └───[code] MISSING FILE(S)
                |             └───[data] survey_01raw.csv
                └───output1_part2.txt  
                    └───[code] output_table2.do           
                        └───[data] analysis_data02.csv
                           └───[code] MISSIN FILE(S)
                              └───[data] admin_01raw.csv  





## Additional resources

Create a section with short summaries of great resources for comp. repro and invite reader to contribute. 

### Some summaries

### Summary on reproducbile workflow (Chapter 11) from @christensen2019transparent:  
- TODO   



### Links

- [Project TIER](https://www.projecttier.org/tier-protocol/)   
- [IDB's cheatsheet for transparency, reproducibility and ethics](http://idbdocs.iadb.org/wsdocs/getdocument.aspx?docnum=EZSHARE-1350314980-383)   
- [Lars Vilhuber LDI's Wiki for Reproducibility](https://github.com/labordynamicsinstitute/replicability-training/wiki). Particularly [this section](https://github.com/labordynamicsinstitute/replicability-training/wiki/Prepare_and_run_replication).   
- World Bank [DIME's Wiki for transparent and reproducible research](https://dimewiki.worldbank.org/wiki/Main_Page).
- Dynamic documents in [R](https://rmarkdown.rstudio.com/gallery.html), [Python](https://github.com/jupyter/jupyter/wiki/A-gallery-of-interesting-Jupyter-Notebooks#economics-and-finance) and [Stata](https://github.com/BITSS/CEGA2019/blob/master/03-extra_dynamic_docs/02b-Stata-markdown/Stata%20Markdown.pdf)  
- Git resources:   
  - [Jenny Bryan's book](https://happygitwithr.com) and [video](https://www.rstudio.com/resources/videos/happy-git-and-gihub-for-the-user-tutorial/)  
  - [Github learning lab](https://lab.github.com/)
  - [Udacity's intro](https://www.udacity.com/course/how-to-use-git-and-github--ud775)  
  - [Git for poets](https://www.youtube.com/playlist?list=PLRqwX-V7Uu6ZF9C0YMKuns9sLDzK6zoiV)  
  - [Combining GitHub and Dropbox](https://github.com/kbjarkefur/GitHubDropBox)    
  - [Atlassian intro to Git](https://www.atlassian.com/git/tutorials)
  - [Software Carpentry tutorial from the command line](https://swcarpentry.github.io/git-novice/)
- [Open Science Framework (OSF)](https://osf.io)
- [R for Stata users](https://github.com/hblackburn/R4Econ/blob/master/Resources.md)  


