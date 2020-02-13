--- 
title: "Guidelines for Computational Reproducibility in Economics"
author: "ACRE Team"
date: "2020-02-12"
documentclass: book
bibliography: [book.bib, packages.bib]
biblio-style: apalike
link-citations: yes
github-repo: BITSS/ACRE
site: bookdown::bookdown_site
description: "Materials to support the reproduction of published research in economics."
output:
  bookdown::html_document2: default
  bookdown::pdf_document2:
    keep_tex: true
  bookdown::word_document2:
    toc: true
---
 
 
# Welcome 

<!--chapter:end:index.Rmd-->

---
output:
  word_document: default
  html_document: default
---
# Introduction {#intro}

**[ADD ONE PAGER BETWEEN COVER AND INTRO]**

This guidelines are designed to standarized reproduction excercises perfomed in graduate courses or undergraduate thesis. 
The goal is to provide a unifed terminology and standards to assess and improve the computational reproducibility of published research. 
During this excercise, students are ask to report the result of their reproduction in a structure fashion. The work of student will be 
crowdsourced for two purposes. First, the assessments will be aggregated to compute reproducibility rates in economics. Second, the 
improvements to reproducibiliy created by students will be posted to the public, facilitating incremental improvements and critical 
assessment. 


EMPHASIE THAT ASSESSMENT IS OUTPUT SPECIFIC 

## Stages of the exercise

The reproduction exercise is separated into five different stages: scoping, assessment, improvement, robustness and (possible) extensions. 
First students should define the scope of the exercise by declaring a paper and specific output to reproduce. Second, the reproduction materials 
are reviewed and describe in detail. Third, the student can improve the current reproduction materials. Fourth, robustness checks can be carried out
and recorded in a systematic fashion. Finally, students in a research stage, could extend the current paper to new methodologies or data. 
 

                  (1)       (2)         (3)        (4)        (5)
                  scope --> assess --> improve --> robust --> extend
                   ▲         |  |                   ▲
                   |         |  |                   | 
                   |_________|  |___________________|

      Suggested level of effort:
      - Graduate
        research:   5%       10%        5%         10%         70%
      - Graduate
        course:    10%       25%       20%         40%         5%
      - Undergrad.
        thesis:    10%       30%       40%         20%         0%

Figure 1 depicts the connection between the five stages of a reproduction exercise. 
The three main populations that are likely to work with this framework are: graduate students (and researchers) doing research, 
graduate students in a class, and undergraduate students in a thesis project. These three groups will
differ in the amount of time and focus that will place on each stage. Figure 1
suggest some possible time allocation for each category.  

The process described in Figure 1 need not be cronologically linear. Students can realize that the scope of their reproduction is too ambitious and then switch to a less intensive reproduction. Also later in the excercise, students could begin to test different specification for robustness while assessing the current reproduciblity. 

## Recording the results of the exercise

Students will be ask to record the results of their reproduction as they make progress through different stages. After the [scoping stage](#scoping), they will be ask to complete [a survey](https://berkeley.qualtrics.com/jfe/form/SV_8hLHNI6LGSYchEN) that records paper of choice and specific outputs to reproduce. As part of this step students are ask to write a brief (max two page) summary of the paper of choice. In the [assessment stage](#assessment), reproducers should inspect all the reproduction materials (raw data, analysis data and code), draw diagrams that connect the output-to-reproduce with all its inputs, and score the level of reproducibility. All this information will be recorded in a [standarized spreadsheet](ADD LINK). In the next stage, student can record any specific [improvements](#improvements) report any potential increase in the reported level of reproducibility in a second short survery. Finally, in the [robustness stage](#robust) student will record any analytical choice and possible variations of it. 

## Outputs of this excercise  
 -  One-page introduction describing why you chose this paper
 -  Two-page summary of paper
 -  2 Completed surveys:  
       - i  - General information about the paper and specific
      information about output to reproduce.  
       - ii - Assessment of how (computationally) reproducible is the paper; description of improvements to its reproducibility; record of all the analytical choices identified in the exercise.
 -  ACRE report card with all the improvements that were created by the researcher reproducing the paper. The list of improvements will be made public and original authors will receive a copy of the report card. The option of anonymity will be provided to the researchers reproducing the paper.     

 - New Readme file (autogenerated).
 - Data with all analytical choices identified.
 - ?? Narrated description of improvements to original CR of the paper, assessment of robustness of results. Lessons from the exercise and possible future extensions.

<!--chapter:end:01-intro.Rmd-->

# Scoping

In this first stage, students are assigned or choose a paper to reproduce. This section describes the different steps required to successfully define the scope of a reproduction exercise. 

## Steps

Before you invest any time in reading/summarizing the paper: 

### Check ACRE records  
Check the [ACRE database](ADD LINK) for previous assessments of the same paper. If there is no previous assessment, create the first entry. If there are previous entries, check if the paper-status is "open to reproductions", and create a new entry^[If the paper appears as "closed to reproductions" it means that ACRE has documented interactions between previous reproductors and original authors, showing that it is not possible to access any further required materials. ].   

### Verify that reproduction materials exist  

Verify that the paper has reproduction materials. If yes, continue. If no, verify in our records if authors have been requested these materials before.  If nobody has submitted a similar request before, contact the authors using the language [suggested here](add link), make sure to CC (acre@berkeley.edu). If the authors have been contacted before and the information is still missing, submit a request for closing the paper for further reproductions and choose another paper. 

### Read and summarize the paper 

Read the paper and write a two-page summary: focus on what is the main question the paper answers, its methodology and data sources.    

### Declare scope of the exercise

Declare if assessment will be about all or main output, and if it aims to start from raw data, or analytic data.   

#### Reproduction margins  

Intensity of the reproduction: analytic or raw.  

##### Extensive margin: outputs to reproduced  
  - **Main results:** a successful reproduction of main results would have obtained the same estimates as in the original paper, for the estimates that the authors highlight the most in either the abstract, introduction or conclusion of the paper. If no estimate is highlighted, then the researcher conducting the reproduction should choose the main result and declare it at the begging of the reproduction.
  - **Complete:**  a successful reproduction is complete when it is possible to obtain the same estimates as the original study for all the outputs presented in the paper. This includes: tables, figures, and inline estimates both in the main body of the paper and all the appendices.   

###### Types of output:   
  - **Tables:** Describe how to cite record location. 
  - **Figures:**  
  - **In-line:**    


##### Intensive margin: depth of reproduction in terms of original data
 - **Raw data:** A data set is considered to be raw, if it corresponds to the a unmodified file that was obtained by the authors from the sources cited in the paper. The only possible modification that can be made to raw data, without changing its category to processed data, is that of deleting personally identifiable information.

 - **Processed data:** a raw data set that has gone through any transformation should be defined as processed data. Processed data can be separated into intermediate data and analytic data.
      - *Intermediate data:* a processed dataset is defined as intermediate if it is not directly used as final input for an analysis in the final paper (including appendix). Intermediate data should not contain direct identifiers.
      - *Analytic data:* data will be defined as analytic if it will be used as the last input in the workflow, to produce a statistic displayed in the final paper (including the appendix).

###### How to classify a data set?
To classify a data set as **raw** you can use some of the following strategies:    

 - Check if the data is stored in a folder denominated as "raw"  
 - Check if the file name has the word "raw" in some part of it  
 - Verify that the data set is not the output of any code script in the reproduction materials  
 - Verify that the same file can be independently obtained from the data source cited in the paper  

To classify a data set as **analytic** you can use some of the following strategies:   

 - Check if the data is stored in a folder denominated as "analytic" or "analysis"  
 - Check if the file name has the word "analytic" or "analysis" in some part of it  
 - Verify that the data set is the last input required to produce some of the output (formatted or unformatted) of the paper  


## Recording the results of scoping  

Complete [survey one](https://berkeley.qualtrics.com/jfe/form/SV_8hLHNI6LGSYchEN).  

## Sample strategies for scoping  

### Strategy 1: 

- First main estimates from paper.

- Then main 2 main tables and/or two main figures.

- Once done with improvements stage of these outcomes, then go back to rest of the paper.    

### Strategy 2:  

 - get everything to run up to analytic data, then go to improvements. Once completed go back for raw data (or in parallel?)  
 
 

<!--chapter:end:02-scope.Rmd-->

# Assessment

The goal of this stage is to provide a standardized assessment of computational reproducibility. All the details required in this section are designed to leave a record of most of the learning process behind a reproduction. Such a record facilitates incremental improvements, allowing new reproductors pick up where others left. 

First, students will be asked to provide a detailed description of all the reproduction materials. Second, they are requested to connect the outputs chosen to reproduce with all of their corresponding inputs. With all this elements in place, students can then score the level of reproducibility of a specific output, and report on paper-level dimensions of reproducibility. 


A recommendation to students performing reproduction it to first focus on one specific output (e.g. "Table 1"). After completing the assessment to this first output, students will have a much easier time translating those improvements to other outputs.   


## Describe inputs  
This section explains how to list all the input materials found or referred in the reproduction package. First students should identify all data sources and connect them with raw data files (when available). Second they are ask to locate and provide a description a brief description of the analytic files. In the last step students locate, inspect and describe all the computer code use in the paper. 
 
The following concepts will be used in this section:     

 - **Cleaning code:** a script should be classified as primarily data cleaning if most of its content is dedicated to actions such as: deleting variables or observations, merging data sets, removing outliers, and reshaping the structure of the data (from long to wide or vice versa).     
 - **Analysis code:** a script should be classified as primarily analysis code if most of its content is dedicated to actions such as: running regressions, running hypothesis tests, computing standard errors, and imputing missing values.  
 - **Raw data:** A data set is considered to be raw, if it corresponds to the a unmodified file that was obtained by the authors from the sources cited in the paper. The only possible modification that can be made to raw data, without changing its category to processed data, is that of deleting personally identifiable information.  LINK THIS DEF TO THE CONCEPT OF DATA SOURCE BELOW. 
 - **Processed data:** a raw data set that has gone through any transformation should be defined as processed data. Processed data can be separated into intermediate data and analytic data.
      - **Intermediate data:** a processed dataset is defined as intermediate if it is not directly used as final input for an analysis in the final paper (including appendix). Intermediate data should not contain direct identifiers.
      - **Analytic data:** data will be defined as analytic if it will be used as the last input in the workflow, to produce a statistic displayed in the final paper (including the appendix).
      - ADD DEFINITION FOR REPRODUCTION PACKAGE. 


### Data sources and raw data   

In the paper to reproduce, find references to all the data sources used in the analysis. A data source is usually described in narrative form, for example the body of the paper can have text like "...for earnings in 2018 we use the Current Population Survey...", in this example, the data source is "Current Population Survey 2018". It is mentioned for the first time in the page 1  of the appendix, so its location should be recorded as "A1". Do this for all the data sources mentioned in the paper.   

Next, look a the reproduction package and map the *data sources* mentioned in the paper to the *data files* in the available materials. In addition to looking at all the existing data files, it is recommended to review the first lines of all code files (specially cleaning code) looking for lines that call the data sets. By inspecting this scripts students might be able to understand how each different data sources is used, and possibly identify any missing files from the reproduction package.

Record all the information of this section into a [assessment tool](https://docs.google.com/spreadsheets/d/1LUIdVFH0OfR70C7z07TYeE-uWzKI_JIeWUMaYhqEKK0/edit#gid=0&range=A1) with the following structure:    

          Raw data information:
          |----------------------|------|-----------------------------------------------|---------------------|
          | data_source          | page | data_files                                    | known_missing       |
          |----------------------|------|-----------------------------------------------|---------------------|
          | "Current Population  | A1    | cepr_march_2018.dta                          |                     |
          | Survey 2018"         |      |                                               |                     |
          |----------------------|------|-----------------------------------------------|---------------------|
          | "DHS 2010 - 2013"    | 4    | nicaraguaDHS_2010.csv;                        | boliviaDHS_2011.csv |
          |                      |      | boliviaDHS_2010.csv; nicaraguaDHS_2011.csv;   |                     |
          |                      |      | nicaraguaDHS_2012.csv; boliviaDHS_2012.csv;   |                     |
          |                      |      | nicaraguaDHS_2013.csv; boliviaDHS_2013.csv    |                     |
          |----------------------|------|-----------------------------------------------|---------------------|
          | "2017 SAT scores"    | 4    | Not available                                 |                     |
          |----------------------|------|-----------------------------------------------|---------------------|
          | ...                  | ...  | ...                                           | ...                 |
          |----------------------|------|-----------------------------------------------|---------------------|

### Describe analytic data sets  

List all the analytic files that you find in the reproduction materials and identify its location relative to the master reproduction folder ^[relative location takes the form `/folder_in_rep_materials/sub_folder/file.txt`, in contrast to absolute location that has the form `username/documents/projects/repros/folder_in_rep_materials/sub_folder/file.txt`]. Record all this information in a [assessment tool](https://docs.google.com/spreadsheets/d/1LUIdVFH0OfR70C7z07TYeE-uWzKI_JIeWUMaYhqEKK0/edit#gid=1299317837&range=A1).

On an initial review, it will probably be hard to provide a one-line description of each analytic data set. But as progress is made in the reproduction exercise, students are ask to return to the spreadsheet and add a one-line description of the main content in each file (for example: `all_waves.csv ` has the simple description `data for region-level analysis`).

The resulting report will have the following structure:  


          Analysis data information:
          |----------------|-----------------------|--------------------------------|
          | analysis_data  | location              | description                    |
          |----------------|-----------------------|--------------------------------|
          | final_data.csv | /analysis/fig1/       | data for figure1               |
          |----------------|-----------------------|--------------------------------|
          | all_waves.csv  | /final_data/v1_april/ | data for region-level analysis |
          |----------------|-----------------------|--------------------------------|
          | ...            | ...                   | ...                            |
          |----------------|-----------------------|--------------------------------|


### Describe code scripts  
List all the code files that you find in the reproduction materials and identify its location relative to the master reproduction folder. Review the begining and end of each code file and identify the inputs required to succesfully run such file. Example of inputs are data sets or other code scripts that are in call commands typically at the begining of a script (e.g.:  `load, read, source, run, do` ), example of outps are other data sets, or plain text files that are typically at the end of a script (e.g.:  `save, write, export`). Record all this information in a [assessment tool](https://docs.google.com/spreadsheets/d/1LUIdVFH0OfR70C7z07TYeE-uWzKI_JIeWUMaYhqEKK0/edit#gid=1617799822&range=A1).

As the student gains understanding of each code script they will likely find more inputs and outputs and are encouraged to update the [assessment tool](https://docs.google.com/spreadsheets/d/1LUIdVFH0OfR70C7z07TYeE-uWzKI_JIeWUMaYhqEKK0/edit#gid=1617799822&range=A1). Once finished with the reproduction excercise, students are ask to classify each code file as analysis or cleaning type. This subjective assessment should be made base on the students' interpretation of the main role of each script.   

Record all this information in a [assessment tool](https://docs.google.com/spreadsheets/d/1LUIdVFH0OfR70C7z07TYeE-uWzKI_JIeWUMaYhqEKK0/edit#gid=1617799822&range=A1)  


          |-------------------|------------------|---------------------|---------------------|----------------------|--------------|
          | file_name         | location         | inputs              | outputs             | description          | primary_type |
          |-------------------|------------------|---------------------|---------------------|----------------------|--------------|
          | output_table1.do  | /code/analysis/  | analysis_data01.csv | output1_part1.txt   | produces first part  | analysis     |
          |                   |                  |                     |                     | of table 1           |              |
          |                   |                  |                     |                     | (unformatted)        |              |
          |-------------------|------------------|---------------------|---------------------|----------------------|--------------|
          | data_cleaning02.R | /code/cleaninig/ | admin_01raw.csv     | analysis_data02.csv | removes outliers     | cleaning     |
          |                   |                  |                     |                     | and missing vals     |              |
          |                   |                  |                     |                     | from raw admin data  |              |
          |-------------------|------------------|---------------------|---------------------|----------------------|--------------|
          | ...               | ...              | ...                 | ...                 | ...                  | ...          |
          |-------------------|------------------|---------------------|---------------------|----------------------|--------------|
 

## Connect each output to all its inputs 

Draw diagrams from output to raw data sources. For more examples of diagrams connecting final output to initial raw data, [see here](#additional-diagrams).    

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

This diagram can be represented in data format by specifying how each component depends to its inputs. For example:  

          Data representation of diagram behind Table 1.
          |--------|-------|-------------------|---------------------|------------|
          | ouput  | order | component         | depends_on          | inpt_type  |
          |--------|-------|-------------------|---------------------|------------|
          | table1 | 1     | table1            | formatting_table1.R | code       |
          |--------|-------|-------------------|---------------------|------------|
          | table1 | 2     |formatting_table1.R| output1_part2.txt   | output     |
          |--------|-------|-------------------|---------------------|------------|
          | table1 | 3     |formatting_table1.R| output1_part1.txt   | output     |
          |--------|-------|-------------------|---------------------|------------|
          | table1 | 4     | output_table1.do  | analysis_data01.csv | data       |
          |--------|-------|-------------------|---------------------|------------|
          | ...    | ...   | ...               | ...                 | ...        |
          |--------|-------|-------------------|---------------------|------------|

Record all this information in a [assessment tool](https://docs.google.com/spreadsheets/d/1LUIdVFH0OfR70C7z07TYeE-uWzKI_JIeWUMaYhqEKK0/edit#gid=1384504774&range=A1). 
In case of any difficulty translating the diagram into a spreadsheet, students can 
draw it with pen and paper, take a picture and upload the picture in the assessment survey.


## Assign a reproducibility score  

Once all the possible inputs have been identified, and there is a clear understanding of the connection between the output-to-reproduce and all of its necessary inputs, it is possible to assess the output-specific level of reproducibility. 

The following concepts will be used in this section:     

 - **Computationally Reproducible from Analytic data (CRA):** an output is CRA if it can be reproduced with minimal effort starting from the analytic data sets.

 - **Computationally Reproducible from Raw data (CRR):** an output is CRR if it can be reproduced with minimal effort from the raw data sets.

 - **Minimal effort:** the definition of minimal effort we will use here is that of spending
five minutes or less in getting the code running. This five minutes do not include the computing time.

### Levels of Computational Reproducibility for a Specific Output  
We can now outline different levels of computational reproducibility. Each level is defined on the basis of data and code availability, possible improvements, and weather or not it achieves some type of reproducibility. In the next chapter we describe each possible improbevement with more detail.  

The assessment is made at the output level. Hence a paper can be highly reproducible for its main results, but suffer of low reproducibility for other outputs. The assessment is on a 10-level scale, where 0 represents imposible to reproduce and 10 represents completely reproducible output. 

 **Level 1 (L1):** There are no data or code available of any type. Possible improvements include: adding raw data (+AD) and adding analysis data (+RD).  

 **Level 2 (L2):** There are analytic data available, but no raw data or any type of code. Possible improvements include: adding raw data (+RD) and adding analysis code (+AC).  

 **Level 3 (L3):** Both analytic data sets and analysis code are available. However the code does not run or produces different results that those of the paper (not CRA). Possible improvements include obtaining raw data (+RD) or debugging the analysis code (DAC).    

 **Level 4 (L4):** Both analytic data sets and analysis code are available, and they produce the same output as in the paper (yes CRA). The reproducibility package can still be improved by obtaining the original raw data sets, or by documenting the steps required to obtain those files.   

 **Level 5 (L5):** All data, analytic and raw, are available. However some or all the codes for cleaning and analysis are missing. Steps for improvement include adding analysis code (+AC) and/or cleaning code (+CC).      

 **Level 6 (L6):**  All data and analysis code are available. However the code does not run or produces different results that those of the paper (not CRA). Possible improvements include adding the missing cleaning code (+CD) or debugging the analysis code (DAC).   

 **Level 7 (L7):**  All data and analysis code are available, and they produce the same output as in the paper (yes CRA). The reproducibility package can still be improved by adding adding the missing cleaning code (+CD).   

 **Level 8 (L8):**  All materials (raw and analysis data, and cleaning and analysis code) are available. However the code does not run or produces different results that those of the paper (not CRR and not CRA). Possible improvements include debugging the cleaning code (DCC) or debugging the analysis code (DAC).  

 **Level 9 (L9):**  All materials (raw and analysis data, and cleaning and analysis code) are available, and the analysis code produces the same output as in the paper (yes CRA). However the cleaning code does not run or produces different results that those of the paper (not CRR). Possible improvements include debugging the cleaning code (DCC).  

 **Level 10 (L10):** All materials are available and produce the same results as in the paper with minimal effort, starting from the analytic data sets (yes CRA) and from the raw data (yes CRR).    

The following figure summarizes the different levels of computational reproducibility (for any given output). For each level, there will be possible improvements that have been done already (`-`), that can be done to move up one level of reproducibility (`✔`) or that are out of reach given the current level of reproducibility (`x`). 


    Figure 1: Levels of Computational Reproducibility and Possible Improvements   

                                               |       |               Possible improvements              |
                                               -----------------------------------------------------------
                                               | Level |+Analysis|  +Raw  |+Analysis|+Cleaning|Debug|Debug|
                                               |       |   Data  |  Data  | Code(AC)| Code(CC)|  AC |  CC |
                                               --------|---------|--------|---------|---------|-----|-----|
    What data are available?                   |       |         |        |         |         |     |     |
    ├── None ..................................|   L1  |    ✔    |    ✔   |    x    |    x    |  x  |  x  |
    ├── Analytic data only. Code?              |       |         |        |         |         |     |     |
    |   ├── No code or cleaning code only......|   L2  |    -    |    ✔   |    ✔    |    x    |  x  |  x  |
    |   └── Analysis code only. Is it CRA?     |       |         |        |         |         |     |     |
    |      ├── No..............................|   L3  |    -    |    ✔   |    -    |    x    |  ✔  |  x  |
    |      └── Yes.............................|   L4  |    -    |    ✔   |    -    |    x    |  -  |  x  |
    └── Raw & Analytic data. Code?             |       |         |        |         |         |     |     |
       ├── None ...............................|   L5  |    -    |    -   |    ✔    |    ✔    |  x  |  x  |
       ├── Analysis code only. CRA?            |       |         |        |         |         |     |     |
       |  ├── No...............................|   L6  |    -    |    -   |    -    |    ✔    |  ✔  |  x  |
       |  └── Yes..............................|   L7  |    -    |    -   |    -    |    ✔    |  -  |  x  |
       └── A. and cleaning code. Is it CRR?    |       |         |        |         |         |     |     |
           ├── No. CRA?                        |       |         |        |         |         |     |     |
           |  ├── No...........................|   L8  |    -    |    -   |    -    |    -    |  ✔  |  ✔  |
           |  └── Yes..........................|   L9  |    -    |    -   |    -    |    -    |  -  |  ✔  |
           └── Yes.............................|   L10 |    -    |    -   |    -    |    -    |  -  |  -  |

Choose the appropiate level of computational reproducibility and record it using the following format.   

          |-------------|-------|------------------------|------------|
          | output_name | level | additional_explanation | other_info |
          |-------------|-------|------------------------|------------|
          | table 1     | 4     |                        | ...        |
          |-------------|-------|------------------------|------------|
          | table 2     | 7     |                        | ...        |
          |-------------|-------|------------------------|------------|
          | figure 1    | 5     |                        | ...        |
          |-------------|-------|------------------------|------------|
          | ...         | ...   | ...                    | ...        |
          |-------------|-------|------------------------|------------|
Record all this information in a [assessment tool](https://docs.google.com/spreadsheets/d/1LUIdVFH0OfR70C7z07TYeE-uWzKI_JIeWUMaYhqEKK0/edit#gid=1384504774&range=A1). You will be asked to provide this information in the [assessment and improvement survey](ADD LINK).   

### Reproducibility dimensions at the paper level  
In addition to an output-specific assessment of computational reproducibility, there are
several practices that facilitate the overall computational reproducibility of the paper. This 
practices are described in detail in the improvement chapter. In this section of assessment it is only 
requiere for students to verify that the original reproduction package made use of any of the following:  

- version control         
- dynamic document        
- translate to open source  
- file organization       
- computing capsule       

Congragtulations! you have now completed the assessment stage. You just provided a concrete building block of knowledge to better understand the state or reproducibility in Economics. 

Please continue to the [next section](#improvements) where you can now help to improve it!


<!--chapter:end:03-assess.Rmd-->

# Improvements   

After completing the assessment of the current reproducibility packages, it is possible to propose a contribution to increase the reproducibility of a paper.  Creating improvements provides an opportunity to gain a more in depth knowledge of the paper. The student will gaing a better understanting of the methods used, while also diving in to a more detailed understanding of the topic under study. In addition to this individual benefits, each contribuion will be assessed by the ACRE community and can potentialy be used by students and researchers around the world as an improved version of the reproducibility package that comes with the paper. 

As in the assessment section, a recommendation to students performing reproduction it to first focus on one specific output (e.g. "Table 1"). After completing the improvements to this first output, students will have a much easier time translating those improvements to other outputs.   

## Types of output-level improvements

### Add missing raw data files or meta-data (+RD) 

It is common that reproductions packages do not include all the original [raw datasets](#describe-inputs). To obtain any missing raw data, or information about them, follow these steps:

   - 1 - Identify a specific missing file. During the assessment all data sources are idenfied from the paper and appendices (column `data_source` in [this standarized spreadsheet](https://docs.google.com/spreadsheets/d/1LUIdVFH0OfR70C7z07TYeE-uWzKI_JIeWUMaYhqEKK0/edit#gid=0&range=A1)). However, some data sources (as delievered to the original investigators) might be missing one or more data files. The specific name of this files can sometimes be obtained by looking at the begining of the cleanning code scripts. If no specific name is found, the reproducer can reference to "Some (or all) of the files use in the paper corresponding to the data source X". If a name is found, it should be recorded in the `data_file` field of the [same spreadsheet](https://docs.google.com/spreadsheets/d/1LUIdVFH0OfR70C7z07TYeE-uWzKI_JIeWUMaYhqEKK0/edit#gid=0&range=A1) as above.    
   - 2 - Verify whether this file(s) can be easily obtained from the web.   
      - 2.1 - If yes: obtain the missing files and add them to the reproducibility package. Make sure to obtain permission to repost this data. See [tips for communication](#tips-for-communication) for a template email.   
      - 2.2 - If no: proceed to step 3.   
   - 3 - [Verify the ACRE database](ADD LINK) for previous attemps to contact the authors on this topic. 
   - 4 - Contact the original authors and kindly request the original materials. Be mindful of the authors time, and remember that the paper you are trying to reproduce was most likely published in a time where standards for computational reproducibility where low or non-existent. See [tips for communication](#tips-for-communication) for sample language on how to approach the authors.  
   - 5 - If the data sets are not available due to confidentiality or proprietary issues, the researcher conducting the reproduction can still improve the reproduction package by including a detailed set of instructions, including contact information and possible costs, for future researchers to follow.
   
In additions to the efforts to obtain raw data, reproductors can also contribute by obtainning missing analysis data. 
 
### Add missing analysis data files (+AD)

[Analysis data](#describe-inputs) can be missing for two reasons: (i) raw data exists but the procedures to transform the different raw data sets into a analysis data are not fully reproducible, or (ii) some or all raw data is missing and some of all the analysis data is not included in the original reproduction package.  To obtain any missing analysis data, follow these steps:

  - 1 - Identify specific name of the missing data set. Typically this information can be found in some of the analysis code that calls such data in order to perform an analysis (eg `analysis_data_03.csv`).   
  - 2 - Verify that such data cannot be obtained by running the data cleaning code over the raw data.   
  - 3 - [Verify the ACRE database](ADD LINK) for previous attemps to contact the authors on this topic.  
  - 4 - [Contact the authors](#tips-for-communication) and request the specific data set.       

### Add missing analysis code (+AC) 

[Analysis code](#describe-inputs) can be added when there are analytic data files, but some or all the methodological steps are missing from the code. In this case researchers conducting the reproduction to follow the these steps:  

  - 1 - Identify specific line/paragraph in the paper that describes the missing analytic step in the code (eg "we impute missing values to...," or "we estimate this regressions using a bandwidth of ...").  
  - 2 - Identify the code file and approximate line in code where the analysis could be carried out.  
  - 3 - [Verify the ACRE database](ADD LINK) for previous attempts to contact the authors on this issue.   
  - 4 - [Contact the authors](#tips-for-communication) and request the specific code files, following the ACRE sample language to request the specific analysis.  
  - 5 - If no response from the authors, researchers reproducing the paper are encourage to attempt to recreate the analysis based on their interpretation of the paper, and filling in any missing piece by making explicit assumptions.   
    
### Add  missing data cleaning code (+CC)   

[Data cleaning (processing)](#describe-inputs) code can be added when there are certain steps missing in the creation/recoding of variables, merging, subsetting of the data sets, and other cleaning related processes. Researchers conducting the reproduction should follow the same steps (1-5) as when adding missing analysis code.

### Debug analysis code (DAC) 
Whenever any code is available in the reproduction package, the researcher performing the reproduction will be able to debug those scripts. Here four types of debugging are suggested to label the different modifications performed in the reproduction:  

  - *Code cleaning:* whenever set of instructions is simplified (e.g. by wrapping repetitive steps in a function or a loop) or when redundant code is removed (eg. old code that was commented out) but the original output remains intact.  
  - *Performance improvement:* whenever a set of instructions is replace by other that performs the same tasks but take less time (eg. choosing one numerical optimization algorithm over another, but obtaining the same results).  
  - *Environment set up:* whenever the code has to be modified to include correct paths to files, specific versions of software, and instructions to install missing packages or libraries.  
  - *Correcting errors:* a coding error will occur when a section in the code, of the reproduction package, executes a procedure that is in direct contradiction with the intended procedure expressed in the documentation (paper or comments of the code). For example an error happens if the paper specify that the analysis is perform on the population of males, but the code restricts the analysis to females only. Please follow the [ACRE procedure to report coding errors](ADD LINK).  


### Debug cleaning code (DCC)

Same as for analysis code, only separate for reporting purposes.  


### Reporting results  
Reproductors are ask to track of all the different types of improvements implemented and record in [this standarized spreadsheet](https://docs.google.com/spreadsheets/d/1LUIdVFH0OfR70C7z07TYeE-uWzKI_JIeWUMaYhqEKK0/edit#gid=0&range=A3) of the assessment tool with the following structure: 

           Level-specific quality improvements: add data/code, debug code.

           | output_name | imprv | description_of_added_files        | lvl |
           |-------------|-------|-----------------------------------|-----|
           | table 1     | +AD   |        ADD EXAMPLES               |  5  |
           | table 1     | +RD   |        ADD EXAMPLES               |  5  |
           | table 1     | DCC   |        ADD EXAMPLES               |  5  |
           | figure 1    | +CC   |                                   |  6  |
           | figure 1    | DAC   |                                   |  6  |
           | inline 1    | DAC   |                                   |  8  |
           | ...         | ...   | ...                               | ... |  




##  Types of paper-level improvements

In addition to the different levels of computational reproducibility described in the previous sections, this section highlights six additional improvements that researchers conducting the reproduction can do to improve the overall reproducibility of a paper. This additional improvements can be apply across levels (including level 10).  

  - 1 - Set up the replication package using version control software (Git).
  - 2 - Improve documentation: add extensive comments to the code.
  - 3 - Integrate documentation with code: adapt the paper into a literate programming environment (eg: Jupyter notebook, RMarkdown, Stata Dynamic Doc).
  - 4 - Re-write the code from a proprietary statistical software (eg Stata, Matlab) into a open source statistical software (eg R, Python, Julia).
  - 5 - File organization and master script: re-organize the reproduction materials into a set of folders and sub-folders that follow [standardized best practices](https://www.projecttier.org/tier-protocol/specifications/#overview-of-the-documentation), and add a master script that executes all the code in order and with no further modifications. [See AEA's reproduction template](https://github.com/AEADataEditor/replication-template).  
  - 6 - Set up a computing capsule that executes all the reproduction in the browser without the need to install any software. See for examples [Binder](https://mybinder.org/) and [Code Ocean](https://codeocean.com/).


### Reporting improvements  
Repoductors will be asked to provide this information in the [assessment and improvement survey](ADD LINK).   



<!--chapter:end:04-improve.Rmd-->

# Checking for Robustness {#robust}


[UNDER CONSTRUCION]

- Identify all possible analytical choices: original and repeated ones.   
- Identify type of choice.  
- Identify choice value. 
- Suggest choice alternative and justify (one line)  




## Identifying Analytical Choices
As part of the requirements to [demonstrate comprehension of the paper and the code](requirements_comprehension.md) researchers conducting the reproduction will be asked to record all the analytical choices identified during the code review process. This is done in two steps: first adding comment lines into the code files where an analytic choice are found, and second, compiling those analytic choices into a standardized data set.  

In your copy of the replication code, add the comment `“# ANALYTICAL CHOICE OF TYPE ____. RECORDED FOR THE FIRST TIME [HERE or IN "FILE_NAME-LINE_NUMBER"]”` above each analytical choice detected in the code. Possible types of analytical choices include (but are not limited to):  

- Analytical choices in data cleaning code:
  - Variable definition  
  - Data sub-setting  
  - Data reshaping (merge, append, long/gather, wide/spread)  
  - Others (specify as "processing - other")
- Analytical choices in analysis code:   
   - Regression function (link function)  
   - Key parameters (tuning, tolerance parameters, etc.)  
   - Controls  
   - Adjustment of standard errors  
   - Choice of weights  
   - Treatment of missing values  
   - Imputations
   - Other (specify as "methods - other")    

Once finished, transcribe all the information on analytical choices into a data set. For the `source` field type "original" whenever the analytical choice is identified for the first time, and `file_name-line number` every time that the same analytical choice is applied subsequently (for example if a analytic choice is identified for the first time in line 103 and for a second in line 122 their respective values for the `source` field should be `original` and `code_01.do-L103` respectively).

The resulting data base should have the [following structure](https://docs.google.com/spreadsheets/d/1nZuJSHswbZgaaIfBcyIUGPwG-WIP8zE1Oambud-WoDc/edit?usp=sharing):

| file_name  | line_number | choice_type         | choice_value                   | Source              |
|------------|-------------|---------------------|--------------------------------|---------------------|
| code_01.do | 73          | data subsetting     | males                          | original            |
| code_01.do | 122         | variable definition | income = wages + capital gains | "code_01.do-L103" |
| code_05.R  | 143         | controls            | age, income, education         | original            |
| ...        | ...         | ...                 | ...                            | ...                 |


## Choose and justify alternative values for analytical choices  



## Test the robustness of results  

Test the robustness of results to alternative (sensible) specifications

  - Identify sensible alternatives to analytical choices.
  - Sample from sensible analytical choices and re-run: report how much do results change as fraction of standard deviations.  
  - Jackknife the preferred estimate.
  - Use ML to select among covariates...  

 



<!--chapter:end:05-robust.Rmd-->

---
output:
  word_document: default
  html_document: default
---
# Concluding the reproduction  

[UNDER CONSTRUCTION]


Walk the students on checking that they have completed all the steps and where can they see their output.  


### Final products
 -  One-page introduction describing why you chose this paper
 -  Two-page summary of paper
 -  2 Completed surveys:  
       - i  - General information about the paper and specific
      information about output to reproduce.  
       - ii - Assessment of how (computationally) reproducible is the paper;
       description of improvements to its reproducibility; record of all the
       analytical choices identified in the exercise.
 -  ACRE report card with all the improvements that were created by the researcher reproducing the paper. The list of improvements will be made public and original authors will receive a copy of the report card. The option of anonymity will be provided to the researchers reproducing the paper.     

 - New Readme file (autogenerated).
 - Data with all analytical choices identified.
 - ?? Narrated description of improvements to original CR of the paper, assessment of robustness of results. Lessons from the exercise and possible future extensions.

<!--chapter:end:06-concluding-the-reproduction.Rmd-->

# Tips for Communication

[UNDER CONSTRUCTION]

## For students or researchers conducting a reproduction  

### Contacting the Authors of the Original Study

#### Verify in the ACRE database, if authors have been contacted before

#### Email them     

##### Template language   
[draft here](https://docs.google.com/document/d/1xJ7pZTQ1VQXVCrs6IUlp7HlBB4oxYha0oOniCG2SWLM/edit?ts=5d251563)

Remember to link template language to documentation for later, to check with team  

###### Requesting raw/analytic data and code  
###### Following up on a non-response requesting additional contact information
  - point out the level of reproducibility of project and how to improve 
  
###### Reporting improvements done to current reproducibility package

###### Requestion permission to re-post public data in new reproduction packages  
Would like to repost your data  
You already gave permission to authors XYZ  
Just trying to improve this authors reproducibility  
Your permission would allow students and researchers do more work in this area.  


###### If response  

Follow up with request of steps necessary for any researcher in the future to access this data.  



 - **Coding errors:**  a coding error will occur when a section in the code, of the reproduction package, executes a procedure that is in direct contradiction with the intended procedure expressed in the documentation (paper or comments of the code). For example an error happens if the paper specify that the analysis is perform on the population of males, but the code restricts the analysis to females only. Please follow the [ACRE procedure to report coding errors](ADD LINK).  


## For original authors contacted by reproductors

## Responding to inquiries





<!--chapter:end:07-tips-for-a-productive.Rmd-->

---
output:
  word_document: default
  html_document: default
---
# Others

[UNDER CONSTRUCTION]

## Code of conduct

## Ask for feedback on guidelines 

## Contributors  

## Additional Diagrams 

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




<!--chapter:end:08-others.Rmd-->



<!--chapter:end:09-references.Rmd-->
