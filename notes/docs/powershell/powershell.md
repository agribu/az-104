# Description
- A command-line shell and a scripting language all in one
- A console to interact with cloud resources and other resources.

# Features
- Built-in help system:  The help system in PowerShell provides information about commands and also integrates with online help articles.
- Pipeline: Traditional shells use a pipeline to run many commands sequentially. PowerShell implements this concept like traditional shells, but it differs because it operates on objects over text. 
- Aliases: Aliases are alternate names that can be used to run commands. 

# How it differs from traditional CLIs
- It operates on objects over text. In a command-line shell, you have to run scripts whose output and input might differ, so you end up spending time formatting the output and extracting the data you need. By contrast, in PowerShell you use objects as input and output. That means you spend less time formatting and extracting.
- It has cmdlets. Commands in PowerShell are called cmdlets (pronounced commandlets). In PowerShell, cmdlets are built on a common runtime rather than separate executables as they are in many other shell environments. Cmdlets typically take object input and return objects. The core cmdlets in PowerShell are built in .NET Core, and are open source. You can extend PowerShell by using more cmdlets, scripts, and functions from the community and other sources, or you can build your own cmdlets in .NET Core or PowerShell.
- It has many types of commands. Commands in PowerShell can be native executables, cmdlets, functions, scripts, or aliases. Every command you run belongs to one of these types. The words command and cmdlet are often used interchangeably, because a cmdlet is a type of command.

# Commands
- Cmdlets are named according to a verb-noun naming standard. It also helps cmdlet developers create consistent names. You can see the list of approved verbs by using the `Get-Verb` cmdlet.

## Locate Commands
```
Get-Command <command>
Get-Command -Noun alias*
Get-Command -Verb Get -Noun alias*
```