# Downstream-Effects-of-Upstream-Causes

# Author Contributions Checklist Form

## Data

### Abstract 

This Matlab code is to reproduce some key results presented in the paper "Nonparametric Bayes Models of Fiber Curves Connecting Brain Regions".

The data used in the paper are from two datasets: (a) a test-retest dataset collected at the University of Sherbrooke; (b) the Human Connectome Project Dataset. Since we mainly focus our analysis on brain structural connectivity, only dMRI data in these datasets are used. The whole processed dMRI (after fiber reconstruction) take a lot of disk space. Therefore, we are not able to upload all the original data. After preprocessing using the method described in the paper, i.e., variance decomposition, we dramatically reduced the data size. We release some of the processed data (after variance decomposition) in .mat format, which can be loaded to MATLAB directly. All data are in the "data" folder.

The Matlab code has been tested in Matlab 2017b. No special package is needed to run the code.

### Availability 

The original Human Connectome Project (HCP) Dataset is current available and can be downloaded from https://[www.humanconnectome.org/](www.humanconnectome.org/).

The test-retest data is not publicly available for ethical reasons. Subjects were not asked ahead of time if they accepted their data to become public. We are in the process of getting this approval. Then, the data will be anonymized and skull stripped to remove all possible identification of subjects.

### Description

Permissions: the authors have registered accounts at ConnectomeDB ([https://db.humanconnectome.org/](https://db.humanconnectome.org/)) and agreed to the Open Access Data Use Terms.

All data in HCP can be downloaded from [https://db.humanconnectome.org](https://db.humanconnectome.org). In this submission, all data have processed. Most of the data required to reproduce the main results are included in our submission (in the folder “data”).

## Code

### Abstract

The provided MATLAB code contains five main procedures: (1) a simulation example to perform the variation decomposition (under the name of “main_simulation.m”); (2) an example of modeling fiber curves connecting a pair of regions in an individual’s brain (under the name of “main_fibers_in_one_subject.m”); (3) an example of modeling fiber curves across 9 scans (from 3 subjects) for one connection (under the name of “main_fibers_across_3subjects.m”); (4) an example of modeling fiber curves across 15 scans (from 5 subjects) for 45 connections (under the name of “main_fibers_across_5subjects.m”) from the test-retest data set; and (5) an example of modeling fiber curves from a subset of HCP subjects for 45 connections (under the name of “main_fibers_across_20hcp_subjects.m”).

_main_simulation.m_ will generate subplots in Figure 3 in the paper. In a regular laptop, this code takes a few mins to run.

_main_fibers_in_one_subject.m_ can be used to reproduce results presented in Figure 7 in the main paper (with some modification, it can also help to produce Figure 2, 3 and 4 in the Supplement), and Table 1. On a regular laptop, this code takes 1 to 2 mins to run.

_main_fibers_across_3subject.m_ uses 3 subjects' data from the Sherbrooke test-retest dataset. Results of Figure 8 and 9, and Table 1 in Supplement can be reproduced with this file. On a regular laptop, this code takes 15 to 20 mins to run.

_main_fibers_across_5subjects.m_ uses 5 subjects' data from the Sherbrooke test-retest dataset. Results of Table 2 in the main paper can be reproduced here. On a regular laptop, this code takes 20 to 30 mins to run.

_main_fibers_across_20hcp_subjects.m_ can be used to model 20 subjects' data from the HCP dataset. Among the 20 subjects, 10 have very low reading scores with a mean of 67.4 (sd = 3.3) and 10 have very high scores with a mean of 134.9 (sd = 2.6) (Refer to Supplementary Section 10 for more details on how these subjects were selected). In a regular laptop, this code takes 10 to 20 mins to run.

### Description 

We released the data and our MATLAB code through github.com: [https://github.com/zhengwu/BNP_Model_Brain_Fibers](https://github.com/zhengwu/BNP_Model_Brain_Fibers). Please refer the README file for more details of the code.

### Additional Information

MATLAB is necessary for running the code (It has been extensively tested in Matlab 2017b).

## Instructions for Use

### Reproducibility 

All tables and figures from the paper can be reproduced. To reproduce the quantitative results,
please use the provided MATLAB code.

* “main_fibers_across_3subjects.m” can be used to generate Figure 3 in the main paper;
* “main_fibers_in_one_subject.m” can be used to generate Figure 7 in the main paper (with some modification, it can also help to produce Figure 2, 3 and 4 in the Supplement), and Table 1;
* “main_fibers_across_3subjects.m” can be used to generate Figure 8 and 9, and Table 1 in the Supplement;
* “main_fibers_across_5subjects.m” can be used to generate results in Table 2.
* “main_fibers_across_20hcp_subjects.m” can be used to generate Figure 9 in the main paper.

### Additional Notes

The downloaded raw dMRI data from HCP dataset are processed using dipy, which can be downloaded from [http://nipy.org/dipy/](http://nipy.org/dipy/).
