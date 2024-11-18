# Philippine Project
Matlab files to GIS data format, from modeling in Philippine using DeltFM

# System Installation
## git command
  url: https://git-scm.com/downloads/win  
  download: [Git-2.47.0.2-64-bit.exe](https://github.com/git-for-windows/git/releases/download/v2.47.0.windows.2/Git-2.47.0.2-64-bit.exe)
  install: C:\Users\Beheen.Trimble\AppData\Local\Programs\Git
## github desktop
  If you have GitHub Desktop installed, you can use it to clone repositories and not deal with SSH keys.
  url: https://desktop.github.com/download/
  file: "GitHubDesktopSetup-x64.exe"
  permission: trimbleava@github.com
# Create Repositoy
- https://github.com/trimbleava/philippine
## Generate SSH Key
You can generate a new SSH key on your local machine. After you generate the key, you can add the public key to your account on GitHub.com to enable authentication for Git operations over SSH.
```
Beheen.Trimble@VSR-4CRHW44 MINGW64 ~/Documents/PROJECTS
$ ssh-keygen -t ed25519 -C "beheen.trimble@versar.com"
Generating public/private ed25519 key pair.
Enter file in which to save the key (/c/Users/Beheen.Trimble/.ssh/id_ed25519):
Enter passphrase for "/c/Users/Beheen.Trimble/.ssh/id_ed25519" (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /c/Users/Beheen.Trimble/.ssh/id_ed25519
Your public key has been saved in /c/Users/Beheen.Trimble/.ssh/id_ed25519.pub
```
### Adding your ssh key to the ssh-agent
In a new **admin elevated PowerShell window**, ensure the ssh-agent is running.
```
# Start the ssh-agent in the background
Get-Service -Name ssh-agent | Set-Service -StartupType Manual
Start-Service ssh-agent
```
In a terminal window without elevated permissions, add your SSH private key to the ssh-agent
`ssh-add c:/Users/YOU/.ssh/id_ed25519 (i.e.) C:\Users\Beheen.Trimble\.ssh`
Add the SSH public key to your account on GitHub
- ssh clone: git clone git@github.com:trimbleava/philippine.git
  
