# rkpython

## Description
This is a general use Python module.
For now, it only contains some functions to make reading and **writing to text files** easier.
  
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
	  
	rk.to_txt(var_list, './Documents/vars.txt', verbose = True)  
	>> File successfully written to ./Documents/doc.txt  
	
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
	  
	var_list = rk.read_txt('./Documents/vars.txt', verbose = True)  
	>> File successfully read from ./Documents/vars.txt  