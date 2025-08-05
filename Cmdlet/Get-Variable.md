# Get-Variable

Synopsis:
retrieve variables in the current session  

ps: "varible" contains "name" and "value"  


Key Parameters
1. -Name
   specifics the target variable  
2. -ValueOnly
   only retrieve the value of a variable
3. -Include, -Exclude  


Notice:  
The output of Get-Variable is usually piped into other Comlets  

demo_1
```powershell
$tmp=1
Get-Variable -Name test -ValueOnly
#output:1
```
