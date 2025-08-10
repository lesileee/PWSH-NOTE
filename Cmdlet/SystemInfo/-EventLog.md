# *-EventLog 

Comlets included: Get-EventLog, Clear-EventLog  

## Get-EventLog

### Synopsis:
Get events and event logs from local or remote computers.

### Key Parameters:  
1. -LogName  
   Commonly used log:  
   • System  
   • Security  
   • Application     
   • HardwareEvents  
2. -Before, -After  
3. -EntryType  
   • Error  
   • Information  
   • FailureAudit  
   • SuccessAudit  
   • Warning  
4. -Newest  
5. -List  
   Display the list of available event logs on the computer.  


## Clear-EventLog

### Synopsis:
Clear all entries in specified event logs on the local or remote computers.

### Key Parameters:
1. -LogName  