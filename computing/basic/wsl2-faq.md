# WSL2 Tips 

- Make sure the Windows version is up to date.
- Make sure all drivers are also up to date and installed; By going through
  1) Settings      
  2) Update and security     
  3) View additional Options   
  4) install and update ALL drivers that are listed.
- When (if) joining the "Windows Insider Program" I found that it's best to choose the "developer" option (which will be the top/first option) instead of the "recommended" option (which will be the second option on the list).
- Make sure to enable Virtual Machine Feature from BIOS on start up before entering the " `dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart `" command on PowerShell.
- It's best to install the "ARM64 package" that includes ("wsl_update_arm64" and "wsl_update_x64") after making sure all updates are completed and the PC is rebooted.
- Make sure to have "Ubuntu 20.04 LTS" and register on it
  - **Disclaimer**: if you're using Ubuntu for the first time you might think that you're not typing anything while entering your password upon registration; while in fact it's just invisible, after entering password the first time press "Enter" in order to confirm password.
- Last but not least make sure you're running PowerShell/CMD as an administrator before entering any command. 