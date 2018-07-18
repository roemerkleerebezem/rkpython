# rkpython

## Description
This is a general use Python module.
For now, it only contains some functions to make reading and **writing to text files** easier, as well as a function that returns the current **largest objects in memory**.
  
## Installation
Use  
```
pip install rkpython
```
  
Then import it in Python with 
```python
import rkpython as rk
```
## Functions
  
### to_txt()
	
	rk.to_txt(l=None, path='text_file.txt', overwrite=False, verbose = False)	
	
	--------------  

	Saves a list to a .txt file.  
	  
	l : list, default is None  
		List object to be saved.  
	  
	path : str, default is 'text_file.txt'  
		File path (with file name) you want to save to.    
	  
	overwrite : bool, default is False    
		Overwrites the file if it exists.  
		  
	verbose : boolean, default is False  
		Prints out a message if the operation was succesful  
		  
	--------------  

	Examples :  
	  
	rk.to_txt(var_list, './documents/vars.txt', verbose = True)  
	>> File successfully written to ./documents/vars.txt 
	
### read_txt()  

	rk.read_txt(path='text_file.txt', verbose = False)    

	--------------  

	Reads from a text file, saving the result as a list, where each line is one item.  
	  

	path : str, default = 'text_file.txt'  
		File path (with file name) you want to read from. Can be any type of file (.txt, .csv...)    
	  
	verbose : boolean, default is False  
		Prints out a message if the operation was succesful  
		  
	--------------  
  
	Examples :  
	  
	var_list = rk.read_txt('./documents/vars.txt', verbose = True)  
	>> File successfully read from ./documents/vars.txt  
	
### to_size()

def to_size(size_in_bytes):

    Converts a number of bytes into a more readable unit, up until Terabytes, and rounds the number down to 1 decimal. Returns a string.
    
    --------------
        
    size_in_bytes : int
        Size in bytes that needs to be converted
        
    --------------

    Examples :
    
    get_size(124480000)
    >> '124.5 Mb'

### rk.get_mem()

def get_mem(nb_objects = 10):

    Prints out a list of the largest objects stored in memory, as well as the total memory usage of global variables. Returns a string.
    
    --------------
        
    nb_objects : int, default =  10
        Maximum number of items to be printed out.
        
    --------------

    Examples :
    
    get_mem(5)
    >> Total usage : 25.3 Gb
    >>
    >>  5 largest objects :
    >>  _477  :  1.7 Gb
    >>  _529  :  1.7 Gb
    >>  _437  :  1.4 Gb
    >>  _412  :  1.3 Gb
    >>  _415  :  1.3 Gb