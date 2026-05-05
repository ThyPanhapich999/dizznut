# Download the configuration file
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/SwiftOnSecurity/sysmon-config/master/sysmonconfig-export.xml" -OutFile "C:\Sysmon\sysmonconfig.xml"

# Verify download
Get-Content C:\Sysmon\sysmonconfig.xml -First 5
