Fedora 42 for WSL
==================

This project provides a ready-to-use Fedora 42 root filesystem packaged as a `.tar` archive for use with Windows Subsystem for Linux (WSL). It allows you to manually import and run Fedora 42 on Windows without needing the Microsoft Store.

The package is designed to help users get started quickly with a minimal, working Fedora environment on WSL 2.  
**This release supports systemd** out-of-the-box and is published as **Release v1**.

-------------------------------------------------------
How to Get Started
-------------------------------------------------------

1. Download the Fedora 42 tarball:
   - From the GitHub Releases section 

2. Create a target directory to hold the distribution:

   PowerShell:
   mkdir C:\WSL\Fedora42

3. Import the distro into WSL:

   PowerShell (run from the directory containing the tar file):
   wsl --import fedora42 C:\WSL\Fedora42 .\fedora42-wsl-v1.tar.gz --version 2

4. Launch Fedora:
   wsl -d fedora42

5. Open VS Code and connect to your Fedora instance through WSL:
   - Install the "Remote - WSL" extension in VS Code.
   - Click on the green >< icon in the lower-left corner and select "Remote-WSL: New Window".
   - From there, you can open the Fedora 42 filesystem and start developing with all the conveniences of VS Code.

-------------------------------------------------------
Default User Info
-------------------------------------------------------

The current image has a default user preconfigured:

- Username: myuser
- Password: user

This is for demonstration purposes and **should be changed** after first login. In future releases, a dynamic setup script will allow setting your username and password on first launch, similar to official WSL distributions from the Microsoft Store.

-------------------------------------------------------
Plans for Future Improvements
-------------------------------------------------------

- Add a welcome script to set up a new user interactively on first launch
- Provide multiple flavor options (minimal, developer-ready, etc.)
- Make installation even easier via a script

-------------------------------------------------------
Credits
-------------------------------------------------------

Special thanks to Jonathan Bowman for his helpful article on setting up Fedora on WSL:
https://dev.to/bowmanjd/install-fedora-on-windows-subsystem-for-linux-wsl-4b26

This guide made the packaging process much simpler.

-------------------------------------------------------
Transparency and Build Steps
-------------------------------------------------------

This repository also includes an extra file containing the exact commands used to extract and package the Fedora root filesystem (`rootfs-extraction-instructions.txt`). This is for transparency and reproducibility.

-------------------------------------------------------
License
-------------------------------------------------------

This project is licensed under the MIT License.

Fedora® is a registered trademark of Red Hat, Inc., and is used here in a community capacity for educational and practical purposes. This project is not affiliated with or endorsed by Red Hat.
