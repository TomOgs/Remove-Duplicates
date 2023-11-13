# Overview
A PowerShell Script to identify duplicate files from a given directory and if desired move them to a new directory for later deletion.

The script won't delete duplicate files, but instead moves them to a new directory which can then be removed. This is done to prevent any ‘unfortunate’ or ‘unforeseen’ errors :^)  

Duplicate identification is done through the MD5 hash of each file.  

# Usage
`Remove-Duplicates.ps1 .`

- Identifies duplicates in the current workign directory, does not move them.

`Remove-Duplicates.ps1 . remove`

- Identifies duplicates in the current working directory and moves them to a new directory for deletion (which will be called 'Delete Me').
- This is the most common use-case for the script

`Remove-Duplicates.ps1 \test\ remove \test\"yeet them"`

- Identifies duplicates in the \test\ file and moves them to a new directory called 'Yeeted Files'.

# Parameters
## UserPath

Path to the directory you want to identify duplicates for. 

## RemoveFiles

Type 'remove' (case sensitive) to move duplicates to a new directory, otherwise they'll just be listed. 

## RemovalDirectoryName

Choose a name for the new directory duplicate files will be moved to. 

Default is 'Remove Me' 

# To-Do
- General cleanup
- Handle errors
- Validate parameters
- New Param: 
- New Param: Support files over 50MB by adding variable size limit
