Connect-AzAccount]
#< Prompt for username and password
$username = Read-Host -Prompt "Enter your Azure username"
$password = Read-Host -Prompt "Enter your Azure password" -AsSecureString
#Get-AzVM
#Start-AzVM -ResourceGroupName <ResourceGroupName> -Name <VMName>
Get-AzVM | Where-Object {$_.PowerState -eq "VM deallocated"} | ForEach-Object {Start-AzVM -ResourceGroupName $_.ResourceGroupName -Name $_.Name}

