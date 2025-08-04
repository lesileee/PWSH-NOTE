#Get-Member

Synopsis:  
Gets the properties and methods of objects

Basic Concepts
1. "OOP":Object-Oriented Programming
2. "Member" = "Properties" + "Methods"  
3. "peoperties" eqs to "attributes"  
   "methods" eqs to "funtions"  
   kinda like the coding philosophy in C++
4. Basic syntax:  
   Object.Property / Object.Method()
   

Two ways to specifie the "Object"
1. -InputObject  
2. pine an object into "Get-Member"  
There do exist a slight difference between this two ways,  
which will be demonstrated in demo_1  


Output Example  
1. the headline outputs the typename of that object  
2. A table included 3 colums:  
   Name, MemberType, Definition


Key Parameters
1. -InputObject
2. -Name  
   specifies the target member of an object  
3. -MemberType
   specifies the MemberType of outputs, defautly be "ALL"    
   acceptable values: Property, Method, Event...  


demo_1
```powershell
$array = @(1,'hello')

Write-Host "the 'pipe' way:"
$array | Get-Member
#TypeName:System.Int32 for '1', System.String for 'hello'

Write-Host "the '-InputObject' way:"
Get-Member -InputObject $array
#TypeName:System.Object[]

#When you pipe a set of objects into Get-Member,
#it outputs the members of each individual object in the collection;

#When you use "-InputObject" to submit a collection of objects,
#it views the collection as a whole and outputs the members of this collection

```