# Out-*
Comlets included: Out-Null, Out-Host, Out-File, Out-String

## Out-Null  

### Synopsis:
Hides the output instead of sending it down the pipeline or displaying it.  



## Out-Host  

### Synopsis:  
Sends output to the command line.  

### Key Parameters:  
Out-Host is the default setting, you do not have to specify it unless you want to use its parameters.  
1. -InputObject  
2. -Paging  
   Display one page of output at a time.  


## Out-File  

### Synopsis:  
Sends output to a file.  

### Key Parameters:  
1. -FilePath
2. -Append  
3. -Force
4. -NoClobber
5. -NoNewline  
   By default, the output ends with a newline character;  
   With this parameter,you can specifies that the content written to the file doesn't end with a newline character.  
6. -Width  
   Specifies the maximum number of characters in each line of output.   

## Out-String  

### Synopsis:
Outputs input objects as a string.  

### Key Parameters:
1. -InputObject  
2. -Width  
3. -NoNewline  
4. -Width  
5. -Stream  
   By default, no matter how many lines are exhibited in the command line, Out-String views them as a single string;  
   With "-Stream", Out-String will output each line one by one.
   


## Demo
demo_1
```PowerShell
#This demo exhibits two basic ways to use all Out-* Comlets

#way_1: use the "-InputObject" parameter
Out-Null -InputObject (Get-date)

#way_2: pipe a object to Out-* as an input
get-date | Out-Null 
```