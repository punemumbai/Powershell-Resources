# Table of content
1. [How to check powershell version](#how-to-check-powershell-version)
2. [How to upgrade powershell](#how-to-upgrade-powershell)
3. [How to get help?](#how-to-get-help)

---
# How to check `powershell version`?

```powershell
$PSVersionTable
```
You will see like this:
```powershell
Name                           Value
----                           -----
PSVersion                      5.1.26100.4652
PSEdition                      Desktop
PSCompatibleVersions           {1.0, 2.0, 3.0, 4.0...}
BuildVersion                   10.0.26100.4652
CLRVersion                     4.0.30319.42000
WSManStackVersion              3.0
PSRemotingProtocolVersion      2.3
SerializationVersion           1.1.0.1
```

# How to upgrade powershell?
```powershell
iex "& {$(irm https://aka.ms/install-powershell.ps1)}-UseMSI"
```

> After installation `powershell 7` won't show when you type `$PSVersionTable` due to `Powershell 7` installed on side. To use `Powershell 7` type `pwsh` in your `CMD` or `powershell terminal`.

---
# How to get help?

```markdown
# PowerShell `dir` Command Help

## Description
`dir` is an alias for the `Get-ChildItem` cmdlet in PowerShell. It lists files and subdirectories in a specified location.

## Basic Syntax
```powershell
dir [[-Path] <string[]>] [[-Filter] <string>] [<CommonParameters>]
```

## Common Parameters
| Parameter | Description |
|-----------|-------------|
| `-Path`   | Specifies the path to list (default: current directory) |
| `-Filter` | Filters items using wildcards (e.g., `*.txt`) |
| `-Recurse`| Lists items in all subdirectories |
| `-Force`  | Shows hidden/system files |
| `-File`   | Lists only files |
| `-Directory` | Lists only directories |

## Examples

### 1. List current directory contents
```powershell
dir
```

### 2. List specific directory
```powershell
dir C:\Users
```

### 3. Filter by file type

```powershell
dir *.pdf -Recurse
```

### 4. Show only directories
```powershell
dir -Directory
```

### 5. Show hidden/system files
```powershell
dir -Force
```

## Notes
- Unlike CMD's `dir`, PowerShell's version is object-based (returns `FileInfo`/`DirectoryInfo` objects)
- Use `Format-Table` or `Format-List` to control output display
- For detailed help: `Get-Help Get-ChildItem -Full`

---
