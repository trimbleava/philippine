# Philippine Project
Matlab files to GIS data format, from modeling in Philippine using DeltFM

# System Installation
## Git Command
url: https://git-scm.com/downloads/win  
download: [Git-2.47.0.2-64-bit.exe](https://github.com/git-for-windows/git/releases/download/v2.47.0.windows.2/Git-2.47.0.2-64-bit.exe)
install: C:\Users\Beheen.Trimble\AppData\Local\Programs\Git
## Github Desktop
If you have GitHub Desktop installed, you can use it to clone repositories and not deal with SSH keys.
url: https://desktop.github.com/download/
file: "GitHubDesktopSetup-x64.exe"
permission: trimbleava@github.com
## Install Python
You'll need both Python and pip installed to create and manage Python packages

### Install Python:
- Go to python.org/downloads
- Download Python 3.12.6 Windows Installer: https://www.python.org/downloads/release/python-3126
- During Windows installation, make sure to check "Add Python to PATH"
- Test Installation:
 `python --version`

> C:\Users\Beheen.Trimble>python --version
> 
> Python 3.12.6
 
#### Default File Location
- C:\Users\Beheen.Trimble\AppData\Local\Programs\Python\Python312\Scripts\
- C:\Users\Beheen.Trimble\AppData\Local\Programs\Python\Python312\
- C:\Users\Beheen.Trimble\AppData\Local\Programs\Python\Launcher\
  
#### Test PIP
`pip --version`

> C:\Users\Beheen.Trimble>pip --version
> 
> pip 24.2 from C:\Users\Beheen.Trimble\AppData\Local\Programs\Python\Python312\Lib\site-packages\pip (python 3.12)

# Create Repositoy
Go to your GitHub/GitLab site and manually creat the repository.
(i.e. https://github.com/trimbleava/philippine)

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
In a new **admin elevated PowerShell window**, ensure the ssh-agent is running:
```
# Start the ssh-agent in the background
Get-Service -Name ssh-agent | Set-Service -StartupType Manual
Start-Service ssh-agent
```
In a terminal window without elevated permissions, add your SSH private key to the ssh-agent:

`ssh-add c:/Users/YOU/.ssh/id_ed25519 (i.e.) C:\Users\Beheen.Trimble\.ssh`

Add the SSH public key to your account on GitHub:
- In the upper-right corner of any page on GitHub, click your profile photo, then click  Settings.
- In the "Access" section of the sidebar, click  SSH and GPG keys.
- Click New SSH key or Add SSH key.
- In the "Title" field, add a descriptive label for the new key. For example, if you're using a personal laptop, you might call this key "Personal laptop".
- Select the type of key, either authentication or signing. For more information about commit signing, see "About commit signature verification."
- In the "Key" field, paste your public key.
- Click Add SSH key.
- If prompted, confirm access to your account on GitHub.

Check ssh Connection:
`ssh -T git@github.com`

## Clone Repository
`ssh clone: git clone git@github.com:trimbleava/philippine.git`

  
