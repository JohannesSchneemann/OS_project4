CS OS 4328.003 - Project 4  
Johannes Schneemann  
j_s1011  
Due date: 11/26/2019  


included files:    pageAlgos.c  
1. use 'gcc pageAlgos.c -o paging' to make executable
2. run './paging' to execute the program for this assignment

Note  
The program will ask for 2 types of input:
1. length of reference string (1-20)
2. number of frames to use (1-5) -> Dr. Chen said max. number of 5 frames is enough.  
Ties are not addressed!

The program will produce similar output for several runs,
but it will eventually provide good results, meaning that
the Optimal Algorithm produces better results than the LRU Algorithm.
(number of page faults: Optimal <= LRU)

Example output:

MBP:pageAlgo hannes$ ./paging   
Please enter the length of the reference string (max 20): 20  
Please enter the number of frames to use (max 5): 4

The generated reference string is:
4 3 5 1 3 2 5 2 4 3 5 3 2 4 5 3 2 1 2 4

<----- OPTIMAL ALGORITHM ---->  
4 0 0 0  
4 3 0 0  
4 3 5 0  
4 3 5 1  
3 found in memory.  
4 3 5 2    
5 found in memory.  
2 found in memory.  
4 found in memory.  
3 found in memory.  
5 found in memory.  
3 found in memory.  
2 found in memory.  
4 found in memory.  
5 found in memory.  
3 found in memory.  
2 found in memory.  
4 1 5 2  
2 found in memory.  
4 found in memory.  
NUMBER OF PAGE FAULTS: 6  

<----LRU ALGORITHM ---->  
4 0 0 0  
4 3 0 0  
4 3 5 0  
4 3 5 1  
3 is in memory.  
2 3 5 1  
5 is in memory.  
2 is in memory.  
2 3 5 4  
3 is in memory.  
5 is in memory.  
3 is in memory.  
2 is in memory.  
4 is in memory.  
5 is in memory.   
3 is in memory.  
2 is in memory.  
2 3 5 1  
2 is in memory.  
2 3 4 1  
NUMBER OF PAGE FAULTS: 8  
  