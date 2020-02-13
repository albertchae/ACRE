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
