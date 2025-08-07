# *-Variable
Comlets included: Get-Variable, Set-Variable, Clear-Variable, Remove-Variable  




## Get-Variable

### Synopsis:
retrieve variables in the current session  

ps: "varible" contains "name" and "value"  


### Key Parameters:
1. -Name  
   specifics the target variable  
2. -ValueOnly  
   only retrieve the value of a variable
3. -Include, -Exclude   

  



## Set-Variable

### Synopsis:
Set the value of a variable  
Creates the variable if one with the requested name does not exist  
It can also be used to reset the value of a formerly created valiable    

### Key-Parameters:
1. -Name, -value  
   The two basic components of a variable  
   For the record, the value of a variable can be neglected when the variable is set  
2. -Description  
   Specifies the description of the variable
3. -PassThru  
   returns an object representing the new variable  
   You can take it as a demand for feeback, under the circumstances that this Comlet does not generate any output defautly 
4. -Option  
   Specifies the value of the Options property of the variable  
   Notice: An option of a variable can only be set when the variable is created  
   acceptable values:None, ReadOnly, Constant, Private, AllScope
5. -Force  
   disregard a valiable's option
   


## Clear-Variable

### Synopsis:  
Deletes the value of a variable  



## Remove-Variable

### Synopsis:  
Deletes a variable, including its value  



## NOTICE
1. For Set-Variable, Remove-Variable and Clear-Variable, given consider that a variable maight be set as "ReadOnly",
it's recommanded to always use the "-Force" parameter to ensure a successful operation.
2. The output of Get-Variable is usually piped into other Comlets.

## Demo
demo_1  
```powershell
$tmp=1
Get-Variable -Name test -ValueOnly
#output:1
```
demo_2  
```powershell
set-variable name=test value=1 -passthru 
```