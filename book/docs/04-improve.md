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

