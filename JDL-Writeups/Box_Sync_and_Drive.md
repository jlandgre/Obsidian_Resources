5/4/26 Install Box Drive on new Macbook Pro

## Ensure All Needed Files Sync
Noticed that Box doesn't sync files with Windows "Hidden" status
* learned previously can't toggle this in Mac Get Info; need to do in Windows File Explorer or from command line
* Files can become mysteriously "Windows hidden" status which leaves them out of syncing
 * Powershell command to recursively fix this in a folder while ignoring .DS_Store files:
 
```powershell

attrib -H -S "."

Get-ChildItem -Recurse -Force | Where-Object {
    $_.Name -ne ".DS_Store"
} | ForEach-Object {
    attrib -H -S $_.FullName
}

```

Ran in:
Client_Projects
Projects folders
previously hidden files synced to new computer!!

## Box Storage Location in Mac OSX

Box Drive stores files in a Library folder that is not subject to Time Machine backup:

	`/Users/user_name/Library/CloudStorage/Box-Box`

Typical Windows path to folder for VS Code Workspace inclusion of 

	`\\Mac\Home\Library\CloudStorage\Box-Box\subfolder_path


`Mobile Documents/iCloud~md~obsidian/Documents/JD_Obsidian/03_Projects/ExcelSteps_Graph"`

        }