# Windows 10 reset memo

<!-- TOC -->

- [Windows 10 reset memo](#windows-10-reset-memo)
  - [Before reset](#before-reset)
    - [Backup](#backup)
    - [Reset](#reset)
  - [During reset](#during-reset)
  - [After reset](#after-reset)
    - [Basics](#basics)
    - [Softwares](#softwares)
      - [Creativity](#creativity)
      - [Dev](#dev)
      - [Browsers](#browsers)
      - [Files](#files)
      - [Gestion](#gestion)
      - [Others](#others)

<!-- /TOC -->

## Before reset

### Backup

- Backup firefox profile:
  - `appdata/local/mozilla/firefox/profiles/`
  - `appdata/roaming/mozilla/firefox/profiles/`
- Backup VSC settings:
  - `users/.vscode` (extension)
  - `appdata/roaming/code/user` (user's options, bindings, snippets)
- Backup XAMPP settings:
  - `xampp/apache/conf/httpd.conf`
  - `xampp/php/php.ini`
- Backup Adobe's app settings:
  - `appdata/roaming/adobe/`
- Others :
  - Mind checking documents, images, etc.
  - Copy RSA keys

### Reset

Go to:
`Settings > Update & security > Recovery > Reset this PC`

Or [download Windows 10](https://www.microsoft.com/fr-fr/software-download/windows10) (for full format or upgrade)

## During reset

Just follow install step, disabled everything and don't connect to internet, wifi, etc. to use with local account.

## After reset

### Basics

- Uninstall crap with [Revo Uninstaller](https://www.revouninstaller.com/revo_uninstaller_free_download.html) for that.
- Remove windows apps by launching `Get-AppxPackage -allusers | Remove-AppxPackage` in PowerShell (can be too brutal and lead to some issues).
- Disable windows notifications in `Notifications & actions`.
- Tweak battery options
- Tweak stuff in `services.msc` and `msconfig`.
- Install the basic with [Ninite](https://ninite.com/).
- Stop telemetry with [ShutUp10](https://www.oo-software.com/fr/shutup10) this time.
- Config folder options (make `File explorer` show `This PC` in `View > Options` and show hiddens files)
- Copy your backed up file back.

### Softwares

#### Creativity

- [Adobe Creative Cloud](https://www.adobe.com/creativecloud/desktop-app.html)
  - Adobe Photoshop
  - Adobe Illustrator
  - Adobe InDesign
  - Adobe After Effect
- [Audacity](https://www.audacityteam.org/download/)\*
- [Figma](https://www.figma.com/downloads/)

#### Dev

- [Cheat Engine](https://www.cheatengine.org/downloads.php)
- [Composer](https://getcomposer.org/download/)
- [FileZilla](https://filezilla-project.org/)\*
- [Git](https://git-scm.com/downloads)
> create a new ssh key for the machine:
> 1. activate *OpenSSH* in *services.msc* with *Automatic (Delayed Start)* option
> 2. in terminal: `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`
> 3. add the key to the ssh agent: `ssh-add key_rsa`
> 4. add the public key to GitHub settings
> 5. set *gitconfig* *email* property to *username@users.noreply.github.com*:
```
git config --global user.email "username@users.noreply.github.com"
```
> 6. create an environment variable at *GIT_SSH* with the path of the *OpenSSH* executable: *C:\Windows\System32\OpenSSH\ssh.exe*
- [Gow](https://github.com/bmatzelle/gow/releases)
 > Fix terminal:
 ```
text:       [255, 250, 230]
background: [7, 10, 20]
```
- [Chocolatey](https://chocolatey.org/) (from an elevated terminal)
```
@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
```
- [Windows Terminal](https://github.com/microsoft/terminal)
> 1. Install `choco install microsoft-windows-terminal`
> 2. Copy `./terminal` inside `%LOCALAPPDATA%`
> 3. Execute `wt.reg`
> 4. Resume your settings
- [Docker](https://docs.docker.com/toolbox/overview/)
> 1. Install (not on the SSD if space is a concern)
> 2. Add folders to default machine:
>     1. Open virtual box, select go to default configuration, shared folders, then add desired folders
>     2. Open a docker terminal, get into the machine `docker-machine ssh`, then mount shared folders: `sudo mount -t vboxsf -o uid=1000,gid=50 d /d` (exemple to map `d to /d`)
- [Insomnia](https://insomnia.rest/)
- [MongoDB Compass](https://www.mongodb.com/download-center/compass)
- [Notepad++](https://notepad-plus-plus.org/download/)\*
- [NPM & node.js](https://nodejs.org/en/)
- [NVM](https://github.com/coreybutler/nvm-windows)
> `npm -g` following:
```
npm install -g node-gyp@latest
npm install -g --production windows-build-tools
```
- [PuTTY](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)\*
- [Visual Code Studio](https://code.visualstudio.com/Download)\*
- [XAMPP](https://www.apachefriends.org/download.html)
- [Yarn](https://yarnpkg.com/fr/docs/install)

#### Browsers

- [Chrome](https://www.google.com/chrome/)\*
- [Firefox](https://www.mozilla.org/en-US/firefox/new/)\*
- [Opera](https://www.opera.com/fr)\*

#### Files

- [Deluge](https://dev.deluge-torrent.org/wiki/Download)\*
- [Nexusfont](http://www.xiles.net/)
- [Powerpoint viewer](https://www.01net.com/telecharger/windows/Bureautique/presentation/fiches/1587.html)
- [VLC](https://www.videolan.org/vlc/download-windows.html)\*
- [WinRAR](https://www.win-rar.com/start.html?&L=10)\*
- [Word viewer](https://www.01net.com/telecharger/windows/Bureautique/editeur_de_texte/fiches/3192.html)

#### Gestion

- [Discord](https://discordapp.com/download)\*
- [GanttProject](https://www.ganttproject.biz/)
- [Slack](https://slack.com/intl/fr-fr/downloads/windows)
- [Skype](https://www.skype.com/en/get-skype/)\*

#### Others

- Antidote
- [Java](https://www.java.com/fr/download/manual.jsp)\*
- Microsoft Office
- [Steam](https://store.steampowered.com/about/)\*
- [SVG Explorer](https://github.com/maphew/svg-explorer-extension)
- [Typora](https://typora.io/#download)

> \* <small>can be installed with ninite</small>
