Active users GET

Get-ADUser -Filter 'enabled -eq $true' | select Name, UserPrincipalName | Export-Csv -Path C:\Users\users\Desktop\ativos.csv -NoTypeInformation -Encoding Unicode


Inactive users GET


Get-ADUser -Filter 'enabled -eq $false' | select Name, UserPrincipalName | Export-Csv -Path C:\Users\users\Desktop\desabilitados.csv -NoTypeInformation -Encoding Unicode
