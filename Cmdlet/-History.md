# *-History
Comlets include: Get-History, Invoke-History


## Get-History

### Synopsis:  
Gets a list of the commands entered during the current session  

### Heads up:
1. "History" here refers to the Comlet entry history.  
2. During a session, the system will automatically gives every commmand you enter a special ID;  
   Starting from '1' in a ascending order;  
   Thus to distinguish several indentical commands entered at different time point.  

### Key Parameters:  
1. -Count  
   Specifies the number of the most recent history entries that this cmdlet gets
2. -ID  
   Specifics the ID of the target command  


## Invoke-History

### Synopsis:
Runs commands from the session history  

### Key Parameters:
1. -ID  
   Specifies the ID of a command in the history;  
   Also, you can type the first few characters of the command as the value of "-ID".  
   (This makes totally no sense, right?..)

## NOTICE
ID is also a property of each record in entry history  



## Demo
demo_1  
```PowerShell
12..18 | Foreach-Object {Invoke-History -ID $_}
```