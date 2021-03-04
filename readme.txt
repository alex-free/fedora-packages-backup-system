Fedora Packages Backup System allows you to download all of the currently installed packages on a Fedora Linux system to a directory. Later, you can install any of the RPM files in the backup directory with the 'dnf install' commandor use Fedora Packages Backup System to install all of them.

To backup all packages installed on your current Fedora installation, execute 'fpbs -b'. This will create a new directory in the current directory that you executed the script in, and will download every installed package to that directory.

To install all packages contained in a backup directory created by the 'fpbs -b' command, execute 'fpbs -r /replacethiswith/your/backupdirectory'. This requires sudo since it is using 'dnf install'.

This is free and unencumbered software released into the public domain, see 'unlicense.txt'.

=Changelog
-v1.0
