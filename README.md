# InterpretedUserType

Decided to create this repository to keep track, in an open source and collaborative way, of the different InterpretedUserType values and meanings.

Original blog post was developed and is maintained by [@dariomws](https://github.com/dariomws) and me here https://get-itips.capazero.net/posts/sfbonprem-interpretedusertype and dates back to 5th of May, 2019.

We feel that, as the list of Interpreted User Types is growing, based on blog post feedback, the blog post by itself can't keep with it and it is a great opportunity for other SfB/Teams architects to contribute here.

## How to contribute

Repository has two branches, main and dev, and every pull request against the documentation found here must be done against the dev branch.

Many thanks for your contributions.

## Lazy contributor guide by [shivtorov](https://github.com/shivtorov)

Shivtorov created a wonderful PowerShell script to gather values from your Tenant, on his own words:

*Suggesting adding some sample PowerShell code that will allow anyone to quickly check if their tenants have any InterpretedUserType values not documented here yet.*

### Example 1
*Works great for small tenants up to few thousands of users*

```PowerShell
Connect-MicrosoftTeams
Import-PSSession (New-CsOnlineSession)

$webRequest = Invoke-WebRequest -Uri "https://raw.githubusercontent.com/get-itips/InterpretedUserType/main/docs/InterpretedUserTypes.md"
$knownTypes = $webRequest.Content -split '\r?\n' -replace '^\|\s*(\w+).*','$1' | where { $_ -match '^\w+$' } | ConvertFrom-Csv | Sort-Object InterpretedUserType

$myTypes = Get-CsOnlineUser -ResultSize Unlimited | Select-Object InterpretedUserType | Group-Object InterpretedUserType -NoElement | sort Name
$myTypes.Name | where { $_ -notin $knownTypes.InterpretedUserType }
```

### Example 2
*Previous example takes minutes to run on tenants with dozens of thousands of users due to it downloads all userdata and then process all calculations locally. The following example moves filtering task from the client PC to the cloud, thus it runs significantly faster on larger tenants*

```PowerShell
# grub data from GitHub
$webRequest = Invoke-WebRequest -Uri "https://raw.githubusercontent.com/get-itips/InterpretedUserType/main/docs/InterpretedUserTypes.md"
$knownTypes = $webRequest.Content -split '\r?\n' -replace '^\|\s*(\w+).*','$1' | where { $_ -match '^\w+$' } | ConvertFrom-Csv | Sort-Object InterpretedUserType

# grub data from SFBO
Connect-MicrosoftTeams
$sfbo = New-CsOnlineSession
$myTypes = Invoke-Command -Session $sfbo -ScriptBlock { Get-CsOnlineUser -ResultSize Unlimited | Select-Object InterpretedUserType -Unique } | Select-Object InterpretedUserType

# report new types
$myTypes.InterpretedUserType | where { $_ -notin $knownTypes.InterpretedUserType }
