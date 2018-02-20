Authors: Liangzhe Chen, Sorour E. Amiri, and B. Aditya Prakash

Paper Title: Automatic Segmentation of General Time-Stamped Data Sequences

Date: March, 2018

Usage:
To run DASSA do as follows,
>> make
>> make demo  


First do 'make' (to compile sources). Then 'make demo' will run the DASSA for toy example. You can directly run DASSA with the following command:
 
To run DASSA 
>> python dassa.py <data_path> <num thread 1> <num thread 2>

<data_path> : Directory of the dataset
<num thread 1>: Number of processors to summaries graphs in parallel
<num thread 2>: Number of processors to generate the segmentation graphs in parallel

Example: 
    Static graphs:   python dassa.py ./data/toy/ 1 1



=============================================================

Input:
- 
=============================================================

Output:
- 
