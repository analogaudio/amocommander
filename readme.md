# AMO Commander

AMO Commander is a portable Windows file-management utility intended for
quick access to files and common file operations. It can also be used in
Windows Preinstallation Environment (WinPE), provided the required
Windows components and runtime dependencies are available.

## Quick Start

### Standard Windows

1.  Download the AMO Commander executable.
2.  Run the executable.
3.  If Windows displays a security warning, review it and allow the app
    only if you trust the source.

### Windows PE (WinPE)

1.  Copy the executable to your tools drive or USB drive.

2.  Optionally rename the executable to `a.exe`.

3.  Open Command Prompt and run it using its full path. For example:

    ``` cmd
    E:
    cd \Tools
    a.exe
    ```

    Or launch it directly:

    ``` cmd
    E:\Tools\a.exe
    ```

The `a.exe` name is simply a convenient filename; it is not required by
the application.

## Features

Based on the available project description, AMO Commander provides or is
intended to provide:

-   Two-pane file browsing.
-   Access to available drives and folders.
-   File viewing and editing.
-   Archive handling through 7-Zip integration.
-   FTP functionality.
-   Keyboard-driven file operations, including copying files with `F5`
    where supported by the current build.

The exact features and integrations depend on the version you are
running.

## Example: Copy Files

1.  Open the source folder in one pane.
2.  Open the destination folder in the other pane.
3.  Select the files or folders to copy.
4.  Press `F5` if the current build supports the copy shortcut.
5.  Confirm the destination and check that the files were copied
    successfully.

Example workflow:

-   Source: `C:\Users\Documents`
-   Destination: `E:\Backup`

Check the destination after copying to verify the result.

## Portable / WinPE Notes

-   AMO Commander is intended to run without a conventional installation
    workflow when using the portable executable.
-   Running from WinPE depends on the WinPE image, available system
    components, architecture compatibility, and any dependencies
    required by the executable.
-   Drive letters can differ between Windows and WinPE. Confirm the
    correct drive letters before copying or modifying files.
-   Back up important files before performing bulk file operations.
-   Avoid running tools or scripts from sources you do not trust.

## Alternative Download

If a separate setup-helper script is provided alongside the main
download, it is an optional alternative. The portable executable can be
run directly when it is compatible with the target environment. A `.bat`
helper is a Windows command script and may trigger security warnings;
inspect it before running.

## Troubleshooting

**The application does not start in WinPE** - Verify that the executable
matches the WinPE architecture. - Try launching it from Command Prompt
to see any error output. - Check whether the WinPE image includes the
system components or runtime dependencies the application needs.

**The drive letters are different** - Use DiskPart or Command Prompt to
identify the correct volumes, then update the source and destination
paths.

**Files did not copy** - Confirm that the destination drive is writable
and has enough free space. - Check the selected files, destination path,
and any error messages. - Verify the copied files at the destination.

## Disclaimer

This README describes the application using the available project
context. Feature availability may vary by build. Always verify important
file operations and keep backups of critical data.
