# powershell

## to run .ps1 files on command prompt
### powershell path_to_your_file\file_name.ps1 (file in in another directory)
### powershell .\file_name.ps1 (file is in current directory) 

## Create new file example
### New-Item test.xml -ItemType File

## Set contents in file example
### Set-Content 'test.xml' '<title>Welcome!</title>' 

## Append contents in file example
### Add-Content 'test.xml' '<p>Welcome to the world!</p>'

## Get file contents example
### Get-Content test.xml

## Clear file contents example
### Clear-Content test.xml

## create a list
### $list = "one", "two", "three", "four", "five"

## displat the list
### $list

## sort the list
### $list | sort

## count the lines and characters using measure-object
### Get-Content test.xml | measure-object -character -line -word

## Display number of files in current directory
### Get-ChildItem | Measure-Object

## Compare 2 files (showing only differences)
### Compare-Object -ReferenceObject $(Get-Content test.xml) -DifferenceObject $(Get-Content test2.xml)

## Compare 2 files (showing all lines)
### Compare-Object -ReferenceObject $(Get-Content test.xml) -DifferenceObject $(Get-Content test2.xml) -IncludeEqual