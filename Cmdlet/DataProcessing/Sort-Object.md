# Sort-Object

## Synopsis
Sorts objects by property values.  

## Key Parameters
1. -Property  
   •You can use the value of a single property or values of multiple properties as the criteria of your sort.  
   •If you use more than one properties in the parameter, separate them with a comma.  
   •You can also write a HashTable as the value of this parameter. Demonstrated in demo_2.  
2. -Ascending, -Descending  
   •"-Ascending" is the default setting.  
3. -Bottom, -Top  
   •Input a number as this parameter's value.    
   •For example, "-Bottom 3" will output 5 records counting from the bottom.  
4. -Stable  
   •Sorted objects will be delivered in the order they were received when their criteria of sorting are equal.
5. -CaseSensitive  
   •By default, sorts aren't case-sensitive.  
6. -Unique  
   •Remove all the repeated members.  

## Demo
demo_1
```powershell
   # basic use
   (2,7,8,1,3,5,9,0,4,6) | Sort-Object -Descending $true   
```



demo_2
```powershell
    Get-Service |
        Sort-Object -Property @{Expression = "Status"; Descending = $true},
                              @{Expression = "DisplayName"; Descending = $false}
							  # @{<name>=<value>}
```

