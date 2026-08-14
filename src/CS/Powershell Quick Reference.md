Powershell has plenty of command combinations for performing various actions in Windows 11. Below are the most common keywords, commands, and actions in Powershell that most developers are expected to use: 

# Rename Files and Folders

### Standard Renaming
Files can be renamed in multiple ways. The main method of doing so is
```powershell
Rename-item -Path "C:\path\to\file.ext" -NewName "new_name.ext" # primary syntax
# use this if the item is read-only or hidden
Rename-Item -Path "report.txt" -NewName "archive.txt" -Force
```
>[!warning]+ Warning: `-NewName` Parameter Syntax
>The `-NewName` parameter must only contain the new name, not the full file path. 

This can also be applied to folders/directories: 
```powershell
Rename-Item -Path "C:\Projects\OldFolder" -NewName "NewFolder"
```

### Bulk Renaming
Multiple Items can be renamed at once using `Get-ChildItem`: 
```powershell
Get-ChildItem *.txt | Rename-Item -NewName { $_.Name -replace "Draft", "Final" }
```
This example replaces the word "Draft" with "Final" in all text files. 

File extensions can also be swapped in bulk: 
```powershell
Get-ChildItem *.log | Rename-Item -NewName { $_.Name -replace '\.log$', '.txt' }
```
This example changes all `.log` items in a folder to `.txt` files. 

---
# Move Items
The **`Move-Item`** cmdlet is the primary tool used to move files, folders, and registry keys from one location to another in PowerShell. It transfers the items completely, deleting them from the source once the relocation is finished.

### Standard Moving
The primary way of moving a file from one directory to another is
```powershell
Move-Item -Path "C:\source\file.txt" -Destination "C:\destination\"
```
This moves the target file from the root directory to a sub-directory `destination`.  This can also be used on a folder and its contents: 
```powershell
Move-Item -Path "C:\SourceFolder" -Destination "D:\TargetFolder"
```
All files of a specific type can be moved using wildcards `*`: 
```Julia
Move-Item -Path "C:\SourceFolder\*.pdf" -Destination "C:\TargetFolder\"
```
Lastly, a file can be moved and renamed simultaneously: 
```powershell
Move-Item -Path "C:\Source\oldname.txt" -Destination "C:\Destination\newname.txt"
```

---

# Removals

### Removing Directories
To delete a folder, along with all its subfolders and files:
```powershell
Remove-Item -Path "C:\path\to\your\folder" -Recurse -Force
```
Additionally, the folder's contents can be wiped without deleting the folder itself: 
```powershell
Remove-Item -Path "C:\path\to\your\folder\*" -Recurse -Force
```

>[!warning]+ Warning: "Folder Not Empty" Bug
>A known issue in PowerShell can sometimes cause `Remove-Item -Recurse` to fail or skip files when deleting deeply nested directories. The most reliable workaround is to pipe the contents directly into the delete command:
>```powershell
>Get-ChildItem -Path "C:\path\to\your\folder" -Recurse | Remove-Item -Force
>```
