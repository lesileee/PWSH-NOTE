# Set-Variable

Synopsis:
Set the value of a variable  
Creates the variable if one with the requested name does not exist  
It can also be used to reset the value of a formerly created valiable    

Key-Parameters
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
   NOtice: An option of a variable can only be set when the variable is created  
   acceptable values:  
   None: Sets no options,default
   ReadOnly: Can be deleted but Cannot be changed
   Constant: Cannot be deleted or changed. 
   Private: The variable is available only in the current scope.
   AllScope: The variable is copied to any new scopes that are created.
5. -Force
   disregard a valiable's option
   
demo_1
```powershell
set-variable name=test value=1 -passthru 
```