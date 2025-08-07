# *-Transcript
Comlets include: Start-Transcript, Stop-Transcript

## Heads up
You can regard transcript as a record of the whole session or at least a part of it.  

## Start-Transcript

### Synopsis:
Creates a record of all or part of a PowerShell session to a text file.  
Defautly, the record starts at the Start-Transcript command and ends with the session.  


### Key Parameters:
1. -Path  
   Specifies a path to restore a transcript. The path must point to a `.txt` file instead of a folder.  
2. -Append  
   Add the new transcript to the end of an existing file.
3. -Force  
   Allow the program to add the new transcript to the end of an existing file when that file is a "Read-Only"
4. -OutputDirectory  
   Specifies a specific path to a folder in which to save a transcript
5. --NoClobber  
   Kinda like "-Append"  


## Stop-Transcript

### Synopsis:
Stops a transcript, cooperating with the Start-Transcript Comlet.  
With this parameter, the record starts at the Start-Transcript command and ends at the Stop-Transcript command.  


## Notice
Default Name: PowerShell_transcript.<computername>.<random>.<timestamp>.txt 
Default Path: $Home\Document  


