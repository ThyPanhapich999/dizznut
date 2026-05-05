# Create a working directory
New-Item -ItemType Directory -Force -Path C:\Sysmon
Set-Location C:\Sysmon

# Download Sysmon from Microsoft
Write-Host "Downloading Sysmon..." -ForegroundColor Cyan
Invoke-WebRequest -Uri "https://download.sysinternals.com/files/Sysmon.zip" -OutFile "Sysmon.zip"

# Extract Sysmon
Expand-Archive -Path Sysmon.zip -DestinationPath C:\Sysmon -Force

# Download the Sysmon configuration file
Write-Host "Downloading Sysmon configuration..." -ForegroundColor Cyan

# Option 1: SwiftOnSecurity configuration (Recommended - comprehensive coverage)
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/SwiftOnSecurity/sysmon-config/master/sysmonconfig-export.xml" -OutFile "sysmonconfig.xml"

Write-Host "Downloads complete!" -ForegroundColor Green
