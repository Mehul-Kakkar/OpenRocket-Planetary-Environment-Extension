# OpenRocket-Planetary-Environment-Extension

This guide explains how to install the Planetary Environment plugin/extension into **OpenRocket** on **Windows, macOS, and Linux** and how to use it.
Version = 24.12
---

## Table of Contents

* [Before Installing the Plugin](#before-installing-the-plugin)
* [Plugin Directory by Operating System](#plugin-directory-by-operating-system)
  * [Windows](#windows)
  * [macOS](#macos)
  * [Linux](#linux)
* [Installing the Plugin](#installing-the-plugin)
* [Adding the Plugin Extension to a Simulation](#adding-the-plugin-extension-to-a-simulation)

---

# Before Installing the Plugin

Before installing the plugin:

1. **Close OpenRocket completely.**
2. Download the plugin `.jar` file.
3. Check if OpenRocket version is supported.

---

# Plugin Directory by Operating System

OpenRocket uses a different user-specific plugin directory depending on the operating system.

| Operating System | Plugin Directory                                    |
| ---------------- | --------------------------------------------------- |
| **Windows**      | `%APPDATA%\OpenRocket\Plugins\`                     |
| **macOS**        | `~/Library/Application Support/OpenRocket/Plugins/` |
| **Linux**        | `~/.openrocket/Plugins/`                            |

Where applicable, `~` represents your user's home directory.

---

# Windows

## Default Plugin Directory

```text
%APPDATA%\OpenRocket\Plugins\
```

Usually this corresponds to:

```text
C:\Users\<USERNAME>\AppData\Roaming\OpenRocket\Plugins\
```

For example:

```text
C:\Users\Mehul\AppData\Roaming\OpenRocket\Plugins\
```

OpenRocket's documentation specifies `%APPDATA%\OpenRocket\Plugins` as the normal Windows plugin directory.

---

## Opening the Plugin Directory

### Method 1 — Using File Explorer

1. Press:

```text
Windows + R
```

2. Enter:

```text
%APPDATA%\OpenRocket\Plugins
```

3. Press **Enter**.

If the directory exists, Windows Explorer will open it.

---

### Method 2 — Navigate Manually

Open:

```text
C:\Users\<USERNAME>\AppData\Roaming\
```

Then open:

```text
OpenRocket
```

Then:

```text
Plugins
```

The final directory should look like:

```text
C:\Users\<USERNAME>\AppData\Roaming\OpenRocket\Plugins\
```

---

## If the Plugins Folder Does Not Exist

If the `Plugins` directory does not exist, create it manually.

Create:

```text
OpenRocket
└── Plugins
```

The final path should be:

```text
C:\Users\<USERNAME>\AppData\Roaming\OpenRocket\Plugins\
```

Then copy your plugin JAR into it.

Example:

```text
Plugins
└── MyPlugin.jar
```

---

# macOS

## Default Plugin Directory

The standard plugin directory on macOS is:

```text
~/Library/Application Support/OpenRocket/Plugins/
```

Which corresponds to:

```text
/Users/<USERNAME>/Library/Application Support/OpenRocket/Plugins/
```

OpenRocket's documentation specifies this location for macOS plugins.

---

## Opening the Plugin Directory

### Method 1 — Finder

1. Open **Finder**.
2. Click **Go** in the menu bar.
3. Select **Go to Folder...**
4. Enter:

```text
~/Library/Application Support/OpenRocket/Plugins/
```

5. Press **Enter**.

---

### Method 2 — Terminal

Open Terminal and run:

```bash
open ~/Library/Application\ Support/OpenRocket/Plugins/
```

---

## If the Plugins Folder Does Not Exist

Create the directory manually.

The directory structure should be:

```text
~/Library/Application Support/OpenRocket/
└── Plugins/
```

Then copy your plugin into it:

```text
Plugins/
└── MyPlugin.jar
```

---

## macOS Security Warning

Depending on how the plugin was downloaded, macOS may display security warnings.

If OpenRocket itself is working but a downloaded plugin is not loading, first verify that:

1. The plugin is in the correct directory.
2. The plugin is actually a `.jar`.
3. The plugin is compatible with your OpenRocket version.
4. OpenRocket was completely restarted after installing the plugin.

Do not disable macOS security protections simply to make an unknown plugin work.

---

# Linux

## Default Plugin Directory

The standard Linux plugin directory is:

```text
~/.openrocket/Plugins/
```

Which corresponds to:

```text
/home/<USERNAME>/.openrocket/Plugins/
```

For example:

```text
/home/mehul/.openrocket/Plugins/
```

The `.openrocket` directory is hidden because its name begins with a dot.

---

## Opening the Directory Using a File Manager

Enable **Show Hidden Files** in your file manager.

You should then be able to see:

```text
~/.openrocket/
```

Inside it, create:

```text
Plugins/
```

Then place the plugin JAR inside it.

---

## Using Terminal

You can create the directory with:

```bash
mkdir -p ~/.openrocket/Plugins
```

Then copy your plugin:

```bash
cp MyPlugin.jar ~/.openrocket/Plugins/
```

The final structure should be:

```text
~/.openrocket/
└── Plugins/
    └── MyPlugin.jar
```

---
# Installing the Plugin

The actual installation process is the same on all three operating systems.

## Step 1 — Download the Plugin

Download the plugin JAR.

Example:

```text
MyPlugin.jar
```

---

## Step 2 — Close OpenRocket

Make sure **all OpenRocket windows and processes are closed**.

Plugins are loaded during application startup, so installing a plugin while OpenRocket is running will generally require restarting OpenRocket before it can be detected.

---

## Step 3 — Open the Plugin Directory

Use the directory corresponding to your operating system:

### Windows

```text
%APPDATA%\OpenRocket\Plugins\
```

### macOS

```text
~/Library/Application Support/OpenRocket/Plugins/
```

### Linux

```text
~/.openrocket/Plugins/
```

---

## Step 4 — Copy the JAR

Copy the plugin JAR into the directory.

Example:

```text
Plugins/
├── MyPlugin.jar
├── AnotherPlugin.jar
└── ExamplePlugin.jar
```

You can install multiple plugins at the same time.

---

## Step 5 — Restart OpenRocket

Launch OpenRocket again.

OpenRocket should scan the plugin directory during startup and load compatible plugins.

---

## Method 3 — Look for Startup Errors

If OpenRocket starts normally and the plugin's functionality appears, the installation was likely successful.

If OpenRocket fails to start after installing a plugin, remove the newly installed plugin and try again.

---

# Adding the Plugin Extension to a Simulation

This is a **simulation extension**.

To use one:

1. Open an `.ork` file.
2. Go to **Flight Simulations**.
3. Select or create a simulation.
4. Click **Edit Simulation**.
5. Open **Simulation Options**.
6. Click **Add Extension**.
7. Select the **Planetary Environment**.
8. Choose the planet to your liking.

---

## License

This guide is provided for educational purposes.
This is no way associated with OpenRocket.
