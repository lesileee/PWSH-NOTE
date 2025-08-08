# Get-FileHash 

## Heads-up  
The HashValue of a file is the only reliable symbol of its content;  
Under the same algorithm, different content lead to different HashValue;  
Thus, HashValue can be use to examine whether the file is editted.  

## Synopsis  
Compute the hash value for a file by using a specified hash algorithm.


## Key Parameters  
1. -Path  
2. -Algorithm  
   Accpetable values:  
   SHA1, SHA256, SHA384, SHA512, MD5;    
   Recommand to use SHA256.(The Deault Setting)  
   
   
## Notice
You can naively assume that you can add a timestamp and a hashvalue at the end of a file;  
That will be meaningless because while you append the hashvalue to the file, the file's content is changing, so as its hashvalue;  
Given consider of this, you have to create a new file for restoring hashvalue use only.  