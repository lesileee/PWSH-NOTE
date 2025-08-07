# Write-*
Comlets included: Write-Warning, Write-Host, Write-Output

## Write-Host


### Synopsis:
Writes output to a host.  


### Key-Parameters:
1. -Object  
2. -BackgroundColor, -ForegroundColor  
3. -NoNewline  
4. -Separator  
   Demonstrated in demo_1.

## Write-Output

### Synopsis:
Write the specified objects to the pipeline.  


### Key Parameters:
1. -InputObject  
2. -NoEnumerate  
   By default, Write-Output enumerates its output.  
   Demonstrated in demo_2.



## Write-Warning

### Synopsis:
Write a warning message.  
The response to the warning depends on the value of the user's '$WarningPreference' variable and the use of the **WarningAction** common parameter.


## Notice
1. The biggest difference between Write-Host and Write-Output is that the output of Write-Output can be sent to pipeline while the output of Write-Host can not. 
The only destination of Write-Host is the host, as it is named.

## Demo

demo_1
```PowerShell
Write-Host (2,4,6,8,10) -Separator '+2='
```

demo_2
```PowerShell
Write-Output (2,4,6,8,10) | Measure-Object
#Output:5
Write-Output (2,4,6,8,10) -NoEnumerate | Measure-Object
#Output:1
```
