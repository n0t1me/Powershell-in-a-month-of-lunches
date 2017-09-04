1.  In the Registry, go to HKEY_CURRENT_USER\software\microsoft\Windows\-currentversion\explorer. Locate the Advanced key, and set its DontPrettyPath property to 1. 

`set-itemproperty -path HKCU:\software\microsoft\Windows\-currentversion\explorer\Advanced\ -PSProperty DontPrettyPath -Value 1`

2.  Create a new directory called C:\Labs.

`new-item -type dir -path C:\Labs`

3.  Create a zero-length file named C:\Labs\Test.txt (use New-Item).

`new-item -type file -path C:\Labs\Test.txt`

4.  Is it possible to use Set-Item to change the contents of C:\Labs\Test.txt to -TESTING? Or do you get an error? If you get an error, why? 

My answer:
I get an error because the set-item is intended for use on items that are in themselves properties, like a variable or registry key, not files.

Author's answer:
The filesystem provider doesn't support this action.)

5.  Using the Environment provider, display the value of the system environment variable %TEMP%. 

`Get-Item Env:\TEMP`

6.  What are the differences between the -Filter, -Include, and -Exclude parameters of Get-ChildItem?

My answer:
filter applies the filter before the objects are collected, exclude removes the objects matching the filter after they are collected, and include removes non-matchin objects after the collection

Author's answer:
Filter uses the PSProvider's filter capability, which not all providers support. You can't use it in the registry, for example)