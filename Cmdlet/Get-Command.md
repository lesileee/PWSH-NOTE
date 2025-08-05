# Get-Command

Output: A table included 4 colums  
		CommandType, Name, Version, Source
		
A Comlet is composed of 2 basic parts: "Verb" - "Noun", "Name"="Verb"+"Noun"  
e.g. Get-Date  
	 Verb:Get, Noun:Date, Name:Get-Date
	
Key Parameters
1. -Syntax  
   To purely gain the syntax of a Comlet
2. -TotalCount  
   Set the total number of outputed Comlets
3. -Module  
   To gain the module that this Comlet is contained
4. -UseFuzzyMatching  
   Commonly being used when you forget the exactly name of a Comlet while you still want its info
5. -All  
   Get all Comlets
6. -ListImported  
   Defaultly,Get-Command will list all those Comlets that have been installed to this computer;  
   To get commands specifically imported to current session from the computer, use "-ListImported"
   

   
demo_1:alias<->name
```powershell
Write-Host alias->name:
Get-Command -Name dir
Write-Host name->alias:
Get-Alias -Definition Get-Location
```

demo_2:Reader-Friendly Output of Get-Command
```powershell
Get-Command -Type Cmdlet | Sort-Object -Property Noun | Format-Table -GroupBy Noun
```

demo_3:-Syntax
```powershell
Get-Command Get-Date -Syntax
#The question is, if I aim to get the syntax of a specific Comlet,
#Why don't I just use get-help?...
```

demo_4:an example of "UseFuzzyMatching"
```powershell
#"Get-Date" without 'e'
Get-Command Get-Dat -UssFuzzyMatching
```