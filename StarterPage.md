The table below lists the usage of some basic commands to help you get started on PowerShell faster.
Note that all bash commands should continue working on PowerShell session.

| Bash                            | PowerShell                              | Description
|:--------------------------------|:----------------------------------------|:---------------------
| ls                              | dir, Get-ChildItem                      | List files and folders
| tree                            | dir -Recurse, Get-ChildItem -Recurse    | List all files and folders
| cd                              | cd, Set-Location                        | Change directory
| pwd                             | pwd, $pwd, Get-Location                 | Show working directory
| clear, Ctrl+L, reset            | cls, clear                              | Clear screen
| mkdir                           | New-Item -ItemType Directory            | Create a new folder
| touch test.txt                  | New-Item -Path test.txt                 | Create a new empty file
| cat test1.txt test2.txt         | Get-Content test1.txt, test2.txt        | Display files contents
| cp ./source.txt ./dest/dest.txt | Copy-Item source.txt dest/dest.txt      | Copy a file
| cp -r ./source ./dest           | Copy-Item ./source ./dest -Recurse      | Recursively copy from one folder to another
| mv ./source.txt ./dest/dest.txt | Move-Item ./source.txt ./dest/dest.txt  | Move a file to other folder
| rm test.txt                     | Remove-Item test.txt                    | Delete a file
| rm -r &lt;folderName>           | Remove-Item &lt;folderName> -Recurse    | Delete a folder
| find -name build*               | Get-ChildItem build* -Recurse           | Find a file or folder starting with 'build'
| grep -Rin "sometext" --include="*.cs" |Get-ChildItem -Recurse -Filter *.cs <br> \| Select-String -Pattern "sometext" | Recursively case-insensitive search for text in files
| curl https://github.com         | Invoke-RestMethod https://github.com    | Transfer data to or from the web

### Recommended Training and Reading
- [Windows PowerShell 7.1 Learning][in-action]
- [Windows PowerShell Cookbook][cookbook] by Lee Holmes

[in-action]: https://docs.microsoft.com/en-us/powershell/scripting/learn/more-powershell-learning?view=powershell-7.1
[cookbook]: http://shop.oreilly.com/product/9780596801519.do

### My collection of used PowerShell code
`Find user ID by lastname (can also try GivenName for the first name)`

  ````powershell
  Get-ADUser -Filter { Surname -like "Smith" }
