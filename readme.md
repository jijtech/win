<img src='desktop.png' alt='Windows' align='center'/>

Activate running scripts
```
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned
```

To setup powershell, Run as admin:
```
irm "https://github.com/jijtech/win/raw/main/setup.ps1" | iex
```

some tools i use on NT systems
* GlazeWM:              https://github.com/glzr-io/glazewm
* Chris titus debloat, Run as admin:
```
iwr -useb https://christitus.com/win | iex
```
* PowerToys:            https://learn.microsoft.com/en-us/windows/powertoys/ ( cant live without )

Microwin / microsoft adk-oscdimg

---
pwsh
```

 PrivCheck
if (-NOT ([Security.Principal.WindowsPrincipal][Security.Principal.WindowsIdentity]::GetCurrent()).IsInRole([Security.Principal.WindowsBuiltInRole] "Administrator")) {
    Write-Warning "Please run this script as an Administrator!"
    Exit
}

```

CMD(batch)
```
:: Check for admin privileges
net session >nul 2>&1
if %errorLevel% neq 0 (
    echo Please run this script as an Administrator!
    exit /b 1
)
```
