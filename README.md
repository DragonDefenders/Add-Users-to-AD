# Add-Users-to-AD

1.	Open PowerShell as Administrator
2.	Type Import-Module ActiveDirectory
3.	Follow the path to where the csv file would be located
  a.	Dir- use this command to view what is in the directory 
  b.	Example: C:/Users/Administrator/Documents/Users.csv 
4.	Type Import-Csv .\ <filename.csv> 
5.	Type the following command:

Import-Csv .\HAL-Users.csv | New-ADUser –AccountPassword (ConvertTo-SecureString –AsPlaintext “p@55word123” –Force) -CannotChangePassword $True –Path “OU=HAL,DC=<dc>,DC=local" 

