#Collection of used PowerShell code

#Find user ID by lastname (can also try GivenName for the first name)
Get-ADUser -Filter { Surname -like "Smith" }
