# First, verify Wazuh agent is installed
Get-Service WazuhSvc

# Backup current config
Copy-Item "C:\Program Files (x86)\ossec-agent\ossec.conf" "C:\Program Files (x86)\ossec-agent\ossec.conf.backup"

# Open the config file in Notepad
notepad "C:\Program Files (x86)\ossec-agent\ossec.conf"
