# Get-DelegatesAndForwardingRules.ps1

This script gathers delegate and SMTP forwarding information for all Exchange user mailboxes.

## Description

This script connects either to Exchange Online or to a dedicated on-premises Exchange Server to export configures mailbox delegates and SMTP forwarding configurations. The SMTP forwarding configurations are gathered from inbox rules and from mailbox forwarding settings.

The gathered information is exported into three different CSV files for further analysis.

## Requirements

- Exchange Server 2016 or newer
- Crednetials to logon to Exchange Online and Office 365 when querying EXO mailboxes
- Utilizes GlobalFunctions PowerShell Module --> [http://bit.ly/GlobalFunctions](http://bit.ly/GlobalFunctions)

## Parameters

### ExchangeOnline

Connect to Exchange Online instead of an on-premises Exchange organization

### UseStoredCredentials

Use encrypted credentials stored in a file. (Not implemented yet)

### ExchangeHost

Host name of the on-premises Exchange Server to connect to

### CsvDelimiter

Preferred delimiter character for the exported CSV file

## Examples

``` PowerShell
.\Get-DelegatesAndForwardingRules.ps1 -ExchangeHost mx01.varunagroup.de
```

Connect to the on-premises Exchange Server mx01.varunagroup.de and export delegation and SMTP forwarding information

``` PowerShell 
.\Get-DelegatesAndForwardingRules.ps1 -ExchangeHost mx01.varunagroup.de -Verbose
```

Connect to the on-premises Exchange Server mx01.varunagroup.de, export delegation and SMTP forwarding information and get verbose information on the objects worked on

``` PowerShell 
.\Get-DelegatesAndForwardingRules.ps1 -ExchangeOnline
```

Connect to Exchange Online and export delegation and SMTP forwarding information

## Note

THIS CODE IS MADE AVAILABLE AS IS, WITHOUT WARRANTY OF ANY KIND. THE ENTIRE
RISK OF THE USE OR THE RESULTS FROM THE USE OF THIS CODE REMAINS WITH THE USER.

The script is based on the original PowerShell script by by Brandon Koeller which is available here [https://github.com/OfficeDev/O365-InvestigationTooling/blob/master/DumpDelegatesandForwardingRules.ps1](https://github.com/OfficeDev/O365-InvestigationTooling/blob/master/DumpDelegatesandForwardingRules.ps1)

## Credits

Written by: Thomas Stensitzki

## Stay connected

- My Blog: [http://justcantgetenough.granikos.eu](http://justcantgetenough.granikos.eu)
- Twitter: [https://twitter.com/stensitzki](https://twitter.com/stensitzki)
- LinkedIn: [http://de.linkedin.com/in/thomasstensitzki](http://de.linkedin.com/in/thomasstensitzki)
- Github: [https://github.com/Apoc70](https://github.com/Apoc70)
- MVP Blog: [https://blogs.msmvps.com/thomastechtalk/](https://blogs.msmvps.com/thomastechtalk/)
- Tech Talk YouTube Channel (DE): [http://techtalk.granikos.eu](http://techtalk.granikos.eu)

For more Office 365, Cloud Security, and Exchange Server stuff checkout services provided by Granikos

- Blog: [http://blog.granikos.eu](http://blog.granikos.eu)
- Website: [https://www.granikos.eu/en/](https://www.granikos.eu/en/)
- Twitter: [https://twitter.com/granikos_de](https://twitter.com/granikos_de)