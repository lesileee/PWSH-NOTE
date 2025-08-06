# Measure-Command

## Synopsis
Measures the time it takes to run script blocks and cmdlets.  

## Key-Parameters
1. -Expression  
   Specifies the expression that is being timed;  
   Enclose the expression in braces (`{}`).  
   You can omit the "-Expression" Parameter, but you can not omit the  `{}`     


## Notice
1. To measure the time it takes to run a Comlet, the program has to actually run it in the current scope;  
   So you must wrap the script block in a brace (`{}`)  
2. To aviod changes cause by running the corresponding script blocks, you can use the invocation operator (`&`) to execute the block in a child scope.   


## Demo
demo_1
```PowerShell
Measure-Command {Get-Date}
```
demo_2
```PowerShell
# Pipe objects to Measure-Command for the use of "-Expression"  
10, 20, 50 | Measure-Command -Expression {for ($i=0; $i -lt $_; $i++) {$i}}
```
demo_3
```PowerShell
$test = 1
Measure-Command { $test = 2 }
$test   #test=2
Measure-Command { & { $test = 3 } }
$test   #test=2, still, under the influence of '&'
```