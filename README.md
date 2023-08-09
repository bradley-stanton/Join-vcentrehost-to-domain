# Join-vcentrehost-to-domain
#Join a vcentre host to a domain, or join multiple at a time to save time


Connect-VIServer -Server <vcentrename> -User <username> -Password <password>

$esxihost = Get-VMHost <hostname>

$esxihost | Get-VMHostAuthentication | Set-VMHostAuthentication -JoinDomain -Domain <domain name> -User <username> -Password <password>
