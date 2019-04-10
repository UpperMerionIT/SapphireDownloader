# SapphireDownloader
A Powershell Module to import reports from Sapphire SIS

## Installation:
Download zip file or use git: `git clone https://github.com/andrewzirkel/SapphireDownloader.git`

## Usage:
Use `Set-SDParameters` to set options

See examples in SapphireDownloaderExample.ps1

## Available Modules:
### Set-SDParameters

Set options for download.

`Set-SDParameters -Username $SDusername -Password $SDpassword -URL $sapphireURL -DistrictID $SDdistrict_id -SchoolID $SDschoold_id -SchoolYear $SDschool_year`

Note: Only School ID can be changed on the fly with `Set-SDParameters -SchoolID $SDschoold_id`

### Get-SDClass_Roster

Get Class Roster Report

### Get-SDDEMO_CUST_LIST

Get Custom Demographics report

### Get-SDReport (not working)

Get report writier report

### Get-SDConnectEd

Get ConnectEd (School Messenger) Report

### Get-SDMarkingPeriods

Get Marking Periods for current building

###  Get-SDDictionary

usage:  `Get-SDDictionary $DictionaryName`

currently supported dictionaries are: Durations,DURATION_MP,DURATION_GROUPS

### Get-SDClassDurations

returns array of objects with Duration Code, start and end dates

### Get-SDUsers

returns array of objects with sapphire users

must have access to Admin > Security, Users and Staff > Users

### Set-SDStudentEmailAddress

usage: `Set-SDStudentEmailAddress -StudentID $id -EMail $email`

sets email address for student record
