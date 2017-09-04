NOTE: Pretty much anything in powershell can be found using help.
If You want to find a command; read the help. If you want to learn about arrays; read the help. It's that simple.

###1.  Run Update-Help and ensure that it completes without errors, so that you have a copy of the help on your local computer. You need an internet connection, and the shell needs to run under elevated privileges (which means Administrator must appear in the shell window's title bar).

(not question)

###2.  Windows-only: can you find any cmdlets capable of converting other cmdlets output into HTML?

- `ConvertTo-HTML`

###3.  Partially Windows-only: are there any cmdlets that can redirect output into a file, or to a printer?

- `Out-File` and `Out-Printer`

###4.  How many cmdlets are available for working with processes? (Hint: remember that cmdlets all use a singular noun.)

- 8

###5.  What cmdlet might you use to write to an event log? (This one's possible on non-Windows operating systems, but you'll get a different answer.)

- `write-eventlog <logname> <source> <id> -message <message>`

###6.  You've learned that aliases are nicknames for cmdlets; what cmdlets are available to create, modify, export, or import aliases?

- `export-alias`, `import-alias`,  `new-alias`, `set-alias`, `get-alias`

###7.  Is there a way to keep a transcript of everything you type in the shell, and save that transcript to a text file?

- `start-transcript` (with optional -path to set the location)

###8.  Windows-only: it can take a long time to retrieve all of the entries from the Security event log. How can you get only the 100 most recent entries?

- Append `-Newest 100` to the command

###9.  Windows-only: is there a way to retrieve a list of the services that are installed on a remote computer?

- `Get-Service -cn <remote computer name>`

###10.  Is there a way to see what processes are running on a remote computer? (You can find the answer on non-Windows operating systems, but the command itself might not work for you.)

- `Get-Process -ComputerName <remote computer name>`

###11.  Examine the help file for the Out-File cmdlet. The files created by this cmdlet default to a width of how many characters? Is there a parameter that would enable you to change that width?

- The default is 80 chars
- You can modify this with the `-width` flag

###12.  By default, Out-File overwrites any existing file that has the same filename as what you specify. Is there a parameter that would prevent the cmdlet from overwriting an existing file?

- Yes, `-NoClobber`

###13.  How could you see a list of all aliases defined in PowerShell?

- `Get-Alias`

###14.  Using both an alias and abbreviated parameter names, what is the shortest command line you could type to retrieve a list of running processes from a computer named Server1?

- `ps -c Server1`

###15.  How many cmdlets are available that can deal with generic objects? (Hint: remember to use a singular noun like object rather than a plural one like objects.)

- 12 (or 9 if you don't count WMI and ObjectEvents)

###16.  This chapter briefly mentioned arrays. What help topic could tell you more about them?

- `about_Arrays`
