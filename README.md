Paper Title: Automatic Segmentation of General Time-Stamped Data Sequences
==========================================================================

Authors: Liangzhe Chen, Sorour E. Amiri, and B. Aditya Prakash

Date: March, 2018


Usage:
-----
To run DASSA do as follows,
>> make demo  


'make demo' will run the DASSA for toy example. 

You can directly run DASSA with the following command:

>> python dassa.py <data_path> <matlab_path> <min_window> <num_of_clusters> <calc_mode>


<data_path> : Directory of the dataset
 
<matlab_path>: Directory of MATLAB in your machine

<min_window>: Minimum desired length for segmentation (i.e., s_min)

<num_of_clusters>: Number of co-occurring clusters (It will be used if <calc mode> is 0)

<calc_mode>: 0/1 value. if <calc mode> is 0 DASSA directly use <num of clusters> as the number  of co-occurring clusters. Otherwise it automatically detects the best number of clusters.

Example: 
    python dassa.py './data/test/' '/Applications/MATLAB_R2016a.app/bin/matlab' 172800 5 0




Input: 
------
- input.txt is a tab separated file. Each row represents a multidimensional observation. Each column is the value of each dimension, and the last column in each row represents the timestamp of the corresponding observation.

The input.txt file for dassa.py looks like as follows:

f11 f12 f13 f14 ... f1n t1

f21 f22 f23 f24 ... f2n t2

f31 f32 f33 f34 ... f3n t3

.

.

.



Output:
-------

- Segmentation.txt: It shows the final segmentation result. For example,

'628490000.0-630390000.0', '630390000.0-630560000.0', '630560000.0-633760000.0'

It means DASSA detects a cut point at time 630390000.0 and 630560000.0 in the time interval [628490000.0-633760000.0]

- Intermediate results:
The following are the intermediate files of the above example:
    Xtilde.txt
    
    BeginEndTime.txt
    
    P_Xtilde_Y.txt
    
    X.txt
    
    Y.txt
    
    Ytilde.txt
    
    ALP_runnimgtime.txt

