# FreeSO Launcher

![image](https://i.imgur.com/eWYBVuY.png)

# Installing FreeSO
To install FreeSO you will also need to install OpenAL, .NET Framework >= 4.0 and the original The Sims Online client. These dependencies are all included in the launcher.

By clicking the **Complete Installation** button in the **Installer** tab you can install FreeSO and all of its dependencies all together.

If you already have some of the dependencies installed, you can install the ones you don't have by clicking them separately in the installer tab. 

# Using a previous FreeSO/TSO installation
If you have already installed FreeSO or The Sims Online before, you can reuse your installation by installing it in the same directory. If the game files are already present, the launcher will not perform a reinstallation. It will set your previous installation as the primary one.

For example, if you already have FreeSO installed in C:/Program Files/FreeSO, then install FreeSO from the launcher choosing the **Program Files** directory. For The Sims Online, this would be C:/Program Files/The Sims Online.

The folder needs to be named **FreeSO** or **The Sims Online** in order for the launcher to pick up previous installations.

Please note that a **Complete Installation** overrides any installations that may already be present on your computer. To use a previous installation, you should use the solo installers from the installer tab.

### Using a previous Simitone installation
The folder needs to be named "Simitone for Windows" in order for the launcher to pick it up.

### Linking a FreeSO folder to the launcher using AutoDetection
The launcher (since 1.7.0) detects a running FreeSO instance and checks if the path is set as the installation directory. If it isn't set as the installation directory, an alert will appear in the Installer tab of the launcher giving you the option to reset it:

![image](https://i.imgur.com/79loHnb.png)

# Extra features
* You can right click the Play button to run FreeSO along with the Volcanic IDE.
* You can change your game language in settings.
* You can change your game mode (3D or 2D).
* You can change the graphics mode (DirectX, OpenGL or Software).

# How to build your code
1. Install node.js.
2. Install the asar library globally: `npm i -g asar`.
3. Clone this repository.
4. Install launcher npm dependencies by running `npm i` in the root source folder.
5. Run `npm run buildasar` in the root source folder to generate a compressed launcher asar package with your code. This will generate an `app.asar` file and an `app.asar.unpacked` folder. You can change the path where these are created in the `package.json` file.
6. Replace the `app.asar` file and the `app.asar.unpacked` folder in the resources folder of your current launcher installation (C:\Program Files (x86)\FreeSO Launcher\resources or wherever it may be) with your newly generated ones.
7. Run the launcher executable.

**PRs are welcome to improve the launcher!**

# Simitone Support

To celebrate Simitone's progress, the launcher (since 1.6.0) now features a Simitone installer (latest release from GitHub: https://github.com/riperiperi/Simitone), a TSCC installation locator, and a brand new Simitone launcher theme.

![image](https://i.imgur.com/7p9VLBA.png)

## Updating Simitone through the launcher

The launcher keeps track of the Simitone version installed, and checks for new releases on the official Simitone GitHub repository (https://github.com/riperiperi/Simitone). Whenever there's a new Simitone release, an update button will appear on the launcher's Simitone screen. Here's an image to demonstrate:

![image](https://i.imgur.com/UrX8s45.png)

## Launching Simitone without TS1 registry entries

Although the launcher does check for The Sims Complete Collection registry entries and displays a big red error message when not found, the launcher will still let you launch Simitone once downloaded and installed.
Simitone will pick up your The Sims Complete Collection files when placed in one of these locations (ordered by priority):
1. A folder named "The Sims" adjacent to the Simitone installation folder. For example, if you installed Simitone in C:\Program Files\Simitone, you'd need to place your The Sims Complete Collection files in C:\Program Files\The Sims.
2. The default The Sims installation folder: C:\Program Files (x86)\Maxis\The Sims\


