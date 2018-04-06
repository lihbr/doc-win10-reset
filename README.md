# Windows 10 reset memo
<!-- TOC -->

- [Windows 10 reset memo](#windows-10-reset-memo)
  - [Before reset](#before-reset)
    - [Backup](#backup)
    - [Reset](#reset)
  - [During reset](#during-reset)
  - [After reset](#after-reset)
    - [Basics](#basics)
    - [Install](#install)

<!-- /TOC -->
## Before reset

### Backup
- Backup firefox profile :
  - `appdata/local/mozilla/firefox/profile/`
- Backup VSC settings :
  - `users/.vscode` (extension)
  - User's options
  - User's bindings
  - User's snippets
- Backup Adobe's app settings :
  - `appdata/roamind/adobe/`
- Others :
  - Mind checking documents, images etc.
  - RSA keys

### Reset

Go to :
`Settings > Update & security > Recovery > Reset this PC`

## During reset

Just follow install step, don't connect to internet, wifi, etc to use with local account.

## After reset

### Basics

- Uninstall crap with [Revo Uninstaller](https://www.revouninstaller.com/revo_uninstaller_free_download.html) for that.
- Remove windows apps by launching `Get-AppxPackage -allusers | Remove-AppxPackage` in PowerShell.
- Disable windows notifications in `Notifications & actions`.
- Tweak battery options
- Tweak stuff in `config.msc` and `msconfig`.
- Install the basic with [ninite](https://ninite.com/) to do so.
- Stop telemetry with [shutup10](https://www.oo-software.com/fr/shutup10) this time.
- Config folder options (make `File explorer` show `This PC` in `View > Options` and show hiddens files)

### Install

- Adobe Creative Cloud
  - Photoshop / Illustrator / Indesign / After Effect / Acrobat
- Antitote
- Audacity
- BitTorrent
- Cinema 4D
- Discord
- Figma
- FileZilla
- GanttProject
- Git
- Chrome
- Insomnia
- Firefox
- Java
- Nexusfont
- Notepad++
- NPM (node.js)
- NVIDIA
- Opera
- Sketchup
- Skype
- Slack
- Steam
- Visual Code Studio
- VLC
- Winrar
- XAMPP