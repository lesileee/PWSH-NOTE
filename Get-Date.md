# Get-Date

Output Example: Monday, August 4, 2025 7:06:46 AM  
format: DayOfWeek, Month Day, Year  Hour:Minute:Second AM/PM  
(DayOfWeek, Month Day, Year  Hour:Minute:Second AM/PM) = DateTime  
(DayOfWeek, Month Day, Year) = Date  
(Hour:Minute:Second AM/PM)   = Time  

Usage  
1. Get info about current Date&Time  
2. Transfer a Date/Time that is previous known into useful info  

Special Parameters for the record  

1. -DisplayHint  
   Allowed Values: Date, Time, DateTime  

2. -Format  
   Allowed Values: FileDate(yyyyMMdd),  
                   FileDateUniversal(yyyyMMddZ),  
                   FileDateTime(yyyyMMddTHHmmssffff),  
                   FileDateTimeUniversal(yyyyMMddTHHmmssffffZ)  
                   ('Z' as an indicator to UTC)  

3. -UnixTimeSeconds  
   Convert a unix timestamp to "DateTime" format  

Usage_1
```powershell
Get-Date
Write-Host DateTime:(Get-Date).DateTime
Write-Host Year:(get-date).Year
Write-Host DayOfWeek:(Get-Date).DayOfWeek
Write-Host DayOfYear:(Get-Date).DayOfYear
Write-Host -DisplayHint Date:
(Get-Date -DisplayHint Date)
```


Usage_2
```powershell
Write-Host "Get-Date "2020-01-01T00:00:00"":
Get-Date "2020-01-01T00:00:00"
```

demo:Create a timestamp
```powershell
$TimeStamp=(Get-Date -Format FileDate)
New-Item -Path . -Name "TEST$TimeStamp.txt" -ItemType "File" -Value "This is a TEST."
```