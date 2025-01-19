## Date:-16/01/2025

**Frappe installation**

Start time:-12:45pm

End time:-6:00pm




**Error while installation:**

Updating system packages...
[sudo] password for abc12:
Hit:1 http://deb.debian.org/debian bookworm InRelease
Hit:2 https://packages.microsoft.com/repos/vscode stable InRelease  	 
Hit:3 https://packages.microsoft.com/repos/code stable InRelease    	 
Err:4 https://packagecloud.io/AtomEditor/atom/any any InRelease
  402  Payment Required [IP: 52.52.120.37 443]
Reading package lists... Done
E: Failed to fetch https://packagecloud.io/AtomEditor/atom/any/dists/any/InRelease  402  Payment Required [IP: 52.52.120.37 443]
E: The repository 'https://packagecloud.io/AtomEditor/atom/any any InRelease' is not signed.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.
An error occurred on line 190 with exit status 0

:-
The error that is occurred above is due to  presence of atom repository after search this on internet and i try to solve this by running this command:-


sudo rm /etc/apt/sources.list.d/archive_uri-https_packagecloud_io_atomeditor_atom_any_-bookworm.list


After that when i again start the erpnext_install.sh then during installations of various packages this has come


Enter the site name (If you wish to install SSL later, please enter a FQDN):
