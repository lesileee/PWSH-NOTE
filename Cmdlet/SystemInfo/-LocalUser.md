# *-LocalUser  

Comlets included: Get-LocalUser, New-LocalUser, Set-LocalUser, Remove-LocalUser,  
                  Enable-LocalUser, Disable-LocalUser  
				  Add-LocalGroupMember, Remove-LocalGroupMember   
				  
## Heads-up  

1. UAC: User Account Control  
2. SID: Security ID  
        Equal to a computer user's identity card.  

## Get-LocalUser  

### Synopsis:  
Get local user accounts.  

### Key Parameters:
1. -Name  


## New-LocalUser  

### Synopsis:  
Create a local user account.  

### Key Parameters:
1. -Name  
2. -Password, -NoPassword  
3. -Description  
4. -AccountExpire, -AccountNeverExpire  
5. -Disabled


## Set-LocalUser  

### Synopsis:  
Modifie a local user account.  

### Key Parameters:
1. -Name  
2. -Password  
3. -AccountExpire, -AccountNeverExpire  
4. -UserMayChangePassword  
   Indicate that the user can change the password on the user account.
5. -Description  
6. -SID  
   Specifie the security ID (SID) of the user account that this cmdlet changes.  
   By default, the system will automatically generate a SID for the new account.  

## Romove-LocalUser  

### Synopsis:  
Delete local user accounts.  

### Key Parameters:
1. -Name  
2. -SID  



## Enable-LocalUser  

### Synopsis:  
Enable a localuser account.  

### Key Parameters:
1. -Name  
2. -SID  


## Disable-LocalUser  

### Synopsis:  
Disable a localuser account.  

### Key Parameters:
1. -Name  
2. -SID  



## Add-LocalGroupMember  

### Synopsis:  
Add members to a local group.  

### Key Parameters:
1. -Group  
   The most commonly used group: Administrators.  
2. -Member    


## Add-LocalGroupMember  

### Synopsis:  
Remove members from a local group.  

### Key Parameters:
1. -Group  
   The most commonly used group: Administrators.  
2. -Member 