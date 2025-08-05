# Get-Alias

Synopsis:
Get-Alias takes an alias and returns the command name  

Alias <-> Command:  
Defautly, Get-Alias outputs in "Alias->Command" way;  
With the parameter "-Definition", Get-Alias can work in the reversed way  
(An explaination to "-Definition":it tells the program to fine the command name in the definition of the corresponding alias)  

Key Parameters:
1. -Definition
2. -Name  
   specifics the target alias  
3. -Exclude  
   excludes some results that matchs some certain conditions
   
   
demo_1: Alias<->Command
```powershell
Write-Host "Alias->Command"
Get-Alias -Name pwd
Write-Host "Command->Alias"
Get-Alias -Definition Get-Location
```
demo_2: -Exclude
```powershell
#WildCards is allowed
Get-Alias -Definition "*-PSSession" -Exclude e*
```
 