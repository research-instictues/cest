![Cest](https://i.imgur.com/WML4rpZ.png)
# Coming soon
Cest is a UEFI powered operating system currently being developed at the research instictues headquarters (my house). It will use the FAT32 filesystem, so permissions will not exist, neither users. When a program is executed, the access it will have will be defined by the following values:

* Is the program a superuser? (Full RAM and storage access)
* Can it access the user's home directory directly? (If not superuser)
* Can it have its own data? (In the application's folder)

## New concepts

### Secure file access
A program such as the text editor will open a file chooser dialog for the user to select a file to open. If the user selects a file, the selected file will be accessible by the executable regardless of its "Direct access" permission. That way, ransomware and spyware can be prevented.

### Fake home directory
Apps will be able to detect when a user hasn't allowed access to their home directory. That way, a creepy app can only work if the user gives direct access to his files. To solve that problem, the user will be able to use diffrent folders as fake home directories. The apps won't be able to exit their assigned folders, but also they won't know that they are being tricked.

### Saved permissions
When an executable first starts, the user will be asked to choose what permissions to allow. When the permissions are chosen, the shell will take the checksum of the executable and save the permissions. The permissions will be saved for only that checksum, so if the executable is altered, they will be asked again.

### New window manager
We are designing a new way for the window manager to work. We are trying to find a way to introduce tiling window management to the average user.

## Our goals

- [x] UEFI assembly environment
- [ ] AHCI driver
- [ ] FAT32 filesystem
- [ ] USB storage driver
- [ ] Internet
- [ ] Graphics
- [ ] Shell
- [ ] Proccesses & Memory protection
- [ ] WiFi
- [ ] Sound
- [ ] OpenGL
- [ ] Better window manager

### Applications
For much later

- [ ] Text editor
- [ ] File manager
- [ ] App store
- [ ] Image viewer
- [ ] Office
- [ ] Web browser
- [ ] Video player
- [ ] Printing system
- [ ] Video editor
- [ ] PC emulator
