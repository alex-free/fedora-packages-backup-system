Fedora Packages Backup System allows you to download all of the currently installed packages on a Fedora Linux system to a directory. Later, you can install any of the RPM files in the backup directory with the 'dnf install' command or use Fedora Packages Backup System to install all of them.

Notes:
'fpbs' must be executed with sudo or as root since it is uses 'dnf install' and 'dnf reinstall'.
'fpbs -r' assumes yes when installing packages, be sure that you know what your doing and that you really want to install all packages in the backup.

To backup all packages installed on your current Fedora installation, execute the 'fpbs -b' command. This will create a new directory in the current directory that you executed the script in, and will download every installed package to that directory.

To install all packages contained in a backup directory created by the 'fpbs -b' command, execute 'fpbs -r /replacethiswith/your/backupdirectory'.

This is free and unencumbered software released into the public domain, see 'unlicense.txt'.

=Changelog
-v1.0.3(3/7/2021)
For packages that are not archivable (part of the OS, not installed from a currently available repository, installed manually) Fedora Packages Backup System now reviews the names of these packages.

-v1.0.2 (3/7/2021)
Download function now uses use dnf reinstall in download-only mode instead of dnf download to improve UX and functionality (backup function now also requires sudo however).
Restore function now creates and uses a local dnf repo in offline only mode, assumes yes.

-v1.0.1
More verbose error for wrong number of args in restore mode.
Consistent echo format.
Displays version number on execution.

-v1.0
