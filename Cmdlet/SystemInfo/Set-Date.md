# Set-Date  

## Synopsis  
Change the system time on the computer to a time that you specify.

## Key Parameters
1. -Date  
2. -Adjust  
   Adjust the system time on the basic of current time.  
   Pass a **TimeSpan** object from **New-TimeSpan** to this paarmeter.  
   Demonstrated in demo_1.  
   
## Heads-up

### New-TimeSpan

### Synopsis:  
Create a TimeSpan object.   

### Syntax:  
New-TimeSpan [-Days <System.Int32>] [-Hours <System.Int32>] [-Milliseconds <System.Int32>] [-Minutes
    <System.Int32>] [-Seconds <System.Int32>] [<CommonParameters>]


## Notice 
1. After you set a datetime on your local computer, which is incorrect, to reset it to the right time, use:
   ```PowerShell
   Get-Service -Name W32Time
   Restart-Service -Name W32Time
   #Run as Administrator
   ```

## Demo  
demo_1
```PowerShell
Get-Date -DisplayHint Date
# Saturday, August 9, 2025

Set-Date -Adjust (New-TimeSpan -Day 1)

Get-Date -DisplayHint Date
# Sunday, August 10, 2025
```