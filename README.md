# Windows Copy File Path Context Menu Utility

This utility adds a "Copy File Path" option to the Windows Explorer right-click context menu, allowing you to easily copy the absolute file path of any file or directory to the clipboard.

## Features

- Right-click context menu integration for files and folders
- Copies absolute file paths including drive letter and full directory structure  
- Works with both files and directories
- Works when right-clicking on folder background
- Simple installation and uninstallation
- No additional software dependencies required

## Installation Methods

### Manual Registry Installation

1. Double-click `Absolute_Path.reg` 
2. Click "Yes" when prompted to add entries to registry
3. The context menu option will be immediately available

## Usage

After installation:
1. Right-click on any file or folder in Windows Explorer
2. Select "Copy File Path" from the context menu
3. The full absolute path will be copied to your clipboard
4. Paste anywhere using Ctrl+V

## Examples

- Right-click on `document.pdf` → Copy File Path → Clipboard contains: `C:\Users\YourName\Documents\document.pdf`
- Right-click on `Projects` folder → Copy File Path → Clipboard contains: `C:\Users\YourName\Projects`
- Right-click on desktop background → Copy File Path → Clipboard contains current folder path

## Uninstallation

### Manual Registry Removal  
1. Double-click `Uninstall_Absolute_Path.reg`
2. Click "Yes" to remove registry entries

## Technical Details

### Registry Locations
The utility adds entries to these registry locations:
- `HKEY_CLASSES_ROOT\*\shell\CopyFilePathMenu` (for files)
- `HKEY_CLASSES_ROOT\Directory\shell\CopyFilePathMenu` (for folders)  
- `HKEY_CLASSES_ROOT\Directory\Background\shell\CopyFilePathMenu` (for folder background)

### Command Implementation
- Basic version uses: `cmd.exe /c echo "%1" | clip`

## System Requirements

- Windows 7, 8, 10, or 11
- Administrator privileges for installation
- No additional software required

## Troubleshooting
1. Ensure you ran the installation script as Administrator
2. Try logging out and back in to Windows
3. Restart Windows Explorer from Task Manager
4. Temporarily disable antivirus software during installation

## Security Notes

- The utility only reads file paths and writes to clipboard
- No network access or file modifications
- Registry changes are minimal and easily reversible
- Source code provided for transparency

## Advanced Usage

For power users, you can customize the registry entries to:
- Change the context menu text
- Add custom icons  
- Modify the command behavior
- Add keyboard shortcuts

## License

This utility is provided as-is for educational and productivity purposes. Feel free to modify and distribute.
