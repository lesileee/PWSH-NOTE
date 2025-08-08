# *-Item

Comlets included: New-Item, Get-Item, Rename-Item, Move-Item, Remove-Item, Copy-Item

## New-Item

### Synopsis:
Creates a new item.


### Key Parameters:
1. -Name  
2. -Path  
3. -ItemType  
   acceptable values:  
   •File  
   •Directory  
   •SymbolLink  
   •Junction  
   •HardLink  
4. -Value  

## Get-Item

### Synopsis:
Gets the item at the specified location.  
You can get the content by this comlet, it only returns a list of items in the specific directory.  

### Key Parameters:
1. -Path 

## Rename-Item

### Synopsis:
Rename an item in a PowerShell provider namespace.  
For rename use only, you can use it to move an item to other locations.   

### Key Parameters:
1. -NewName  
   Enter only a name, path+name is not permitted.   
2. -Path  
   Enter a Path to the target item  
3. -Force  
4. -PassThru  
   By default, this Comlet returns nothing to the host.  

## Move-Item

### Synopsis:
Moves an item from one location(`-Path`) to another(`-Destination`).  

### Key Parameters:
1. -Path  
2. -Destination  
3. -Recurse  
4. -PassThru  



## Remove-Item

### Synopsis:
Delete the specified items.  

### Key Parameters:
1. -Path  
2. -Include, -Exclude  
3. -Force  
4. -Recurse  


## Copy-Item

### Synopsis:

### Key Parameters:
1. -Path  
2. -Destination  
3. -Recurse  
4. -PassThru 
5. -FromSession, -ToSession  
   For romote copying use  
6. -Include, -Exclude  

