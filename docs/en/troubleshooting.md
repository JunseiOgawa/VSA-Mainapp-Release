# Troubleshooting Detailed Guide

This guide provides solutions for problems that may occur in the VSA application. It is organized to help you resolve issues systematically, with specific symptoms and step-by-step solutions provided for each problem.

## Common Problems and Solutions

### Import-Related Issues

#### Photos Are Not Automatically Imported

**Symptom**: Screenshots taken in VRChat are not automatically imported into VSA

**Possible Causes**:
- Monitoring function is disabled
- Folder path is incorrect
- Firewall is blocking the application

**Solution (Step-by-Step)**:

**Step 1: Check Monitoring Function**
1. Open the Game-Side Settings
2. Verify that the toggle switch is enabled (ON)
3. If disabled, click to enable it
4. Take a screenshot in VRChat

**Step 2: Verify Folder Path**
1. Open the Game-Side Settings
2. Check the "Screenshot Folder" setting
3. Default path is typically `C:\Users\[YourUsername]\Pictures\VRChat`
4. Verify the path is correct and re-select if necessary

**Step 3: Verify VRChat**
1. Confirm that screenshots are actually being taken in VRChat
2. Open Windows Explorer and check if photo files exist in the specified folder
3. Verify that the filename and capture time match

**Step 4: Check Firewall Settings**
1. Open Windows Security Center
2. Click on "Firewall & network protection"
3. Click on "Allow an app through firewall"
4. Verify that VSA is included in the allowed apps list
5. If not, add it by clicking "Allow another app"

**Step 5: Restart the Application**
1. Completely close VSA
2. Close VRChat as well
3. Restart VSA
4. Launch VRChat
5. Take a screenshot

**If Still Not Resolved**:
Refer to [Checking Log Files](#how-to-check-log-files) to examine detailed errors.

#### Thumbnails Are Not Displayed

**Symptom**: Thumbnails in the gallery appear gray or are not displayed at all

**Possible Causes**:
- Thumbnail generation is in progress
- Thumbnail generation failed
- Cache is corrupted

**Solution (Step-by-Step)**:

**Step 1: Wait for Processing to Complete**
1. Display the gallery
2. Check the "Processing..." indicator at the top of the screen
3. Wait until the indicator disappears (may take several minutes)

**Step 2: Try Scrolling**
1. Scroll up and down in the gallery
2. Thumbnails will be loaded dynamically while scrolling
3. Verify network connection (if using external storage)

**Step 3: Restart the Application**
1. Completely close VSA
2. Wait a few seconds
3. Restart VSA
4. Display the gallery

**Step 4: Clear Cache**
1. Close VSA
2. Delete the following folder:
   ```
   %APPDATA%/VSA/cache/
   ```
3. Restart VSA
4. Thumbnails will be regenerated (may take time)

**Step 5: Rebuild Database**
1. Enable Developer Mode (Settings > Appearance > Developer Mode)
2. A "Developer" menu will appear in the sidebar
3. Click on "Developer"
4. Click "Rebuild Database"
5. Select "OK" in the confirmation dialog
6. Restart VSA

**Note**: Rebuilding the database may result in loss of favorites, tags, and other custom data.

### Gallery Display-Related Issues

#### Gallery Performance Is Slow

**Symptom**: Photo display or scrolling is slow, or the application freezes occasionally

**Possible Causes**:
- Large number of photos being loaded
- Thumbnail size is too large
- Animation settings are enabled
- Insufficient memory

**Solution (By Priority)**:

**Solution 1: Reduce Thumbnail Size**
1. Display the gallery
2. Drag the zoom slider in the toolbar to the left
3. This will reduce the thumbnail size
4. Check if scroll speed improves

**Solution 2: Disable Animations**
1. Open Settings
2. Select the "Animation" panel
3. Disable animation effects
4. Screen effects will be lighter

**Solution 3: Delete Unnecessary Photos**
1. Select unnecessary photos in the gallery
2. Click the Delete button
3. Reducing total file count will reduce processing load

**Solution 4: Restart the Application**
1. Completely close VSA
2. Wait a few seconds
3. Restart VSA
4. Memory will be reset

**Solution 5: Check PC Memory**
1. Open Task Manager (Ctrl + Shift + Esc)
2. Click on the "Performance" tab
3. Check memory usage
4. If usage is 90% or higher, your PC has insufficient memory
5. Close other applications

#### Photos Are Not Displayed

**Symptom**: Nothing is displayed in the gallery, or "No photos" is shown

**Possible Causes**:
- Import has not completed
- Folder path is incorrect
- Photo files have been deleted

**Solution (Step-by-Step)**:

**Step 1: Verify Import Folder**
1. Open the Game-Side Settings
2. Check the "Screenshot Folder" path
3. Open that folder in Windows Explorer
4. Verify that photo files exist (`.png` or `.jpg` files)

**Step 2: Check Import Process**
1. Open the Import Folder view
2. Check the processing indicator
3. Wait until the indicator disappears

**Step 3: Manual Reload**
1. Display the gallery
2. Click the "Reload" button (⟲) in the toolbar
3. This will refresh the photo list

**Step 4: Check Database**
1. Enable Developer Mode
2. Display "Database Info" from the Developer menu
3. Check "Total Photos"
4. If it shows 0, the firewall may be blocking the application

### JPEG XL Compression-Related Issues

#### Compression Does Not Start

**Symptom**: Auto-compression does not start at the scheduled time, or the scheduling feature is not working

**Possible Causes**:
- Auto-compression feature is disabled
- VRChat is running
- System time is incorrect

**Solution (Step-by-Step)**:

**Step 1: Verify Auto-Compression Is Enabled**
1. Open the Game-Side Settings
2. Expand Advanced Settings
3. Verify that "Auto-Compression Feature" is enabled (toggle ON)
4. If disabled, enable it and save

**Step 2: Check VRChat Status**
1. Verify that VRChat is not running
2. If it is, close it
3. Wait until the scheduled time after completely closing VRChat

**Step 3: Verify System Time**
1. Check Windows system time
2. Click the time in the taskbar
3. Verify the time is accurate
4. If incorrect, synchronize with the time server (usually automatic)

**Step 4: Manually Run Compression**
1. Open the JPEG XL Compression view
2. Click "Select Folder" to choose the folder to compress
3. Click the "Run Compression" button
4. Verify that manual execution works

#### Image Quality Degrades After Compression

**Symptom**: After JPEG XL compression, images appear corrupted or colors have changed

**Solution**:

VSA's JPEG XL compression uses **lossless (reversible) compression**, so image quality should not degrade. The following causes are possible:

**Cause 1: Original Image Is Already Compressed**
- Images output by VRChat are already compressed, so no visual changes from further compression are expected
- This is normal behavior

**Cause 2: Viewer Does Not Support JXL**
- Windows standard "Photos" app does not support JXL
- Install a JXL-compatible viewer:
  - IrfanView (Free)
  - FastStone Image Viewer (Free)
  - Other JXL-compatible image viewers

**Cause 3: File Is Corrupted**
1. Check detailed logs (Developer Mode)
2. If errors exist, redo the compression
3. If the same error occurs, the original file may be corrupted

### VRChat Integration-Related Issues

#### Metadata Cannot Be Retrieved

**Symptom**: World name, user name, capture time, and other photo metadata are not displayed

**Possible Causes**:
- Metadata output is disabled
- Log folder path is incorrect
- VRChat is an old version

**Solution (Step-by-Step)**:

**Step 1: Verify Metadata Output Folder**
1. Open the Game-Side Settings
2. Expand Advanced Settings
3. Check if "Metadata Output Folder" is configured
4. If not, specify the VRChat log folder

**Step 2: Verify VRChat Settings**
1. Open VRChat settings menu
2. Verify that metadata output is enabled
3. If disabled, enable it
4. Restart VRChat

**Step 3: Check Log Folder**
1. Verify the log folder path shown in Game-Side Settings
2. Open that folder in Windows Explorer
3. Verify that log files such as `output.log` exist
4. If not, reconfigure the log folder path

**Step 4: Take New Screenshots**
1. After completing all settings, take new screenshots
2. Metadata will not be applied to existing photos
3. Verify that metadata is applied to new photos

#### OSC Communication Cannot Be Established

**Symptom**: Camera parameters (such as VirtualLens2) cannot be retrieved

**Possible Causes**:
- OSC port numbers do not match
- OSC is disabled on VRChat side
- Firewall is blocking
- Port number is in use

**Solution (Step-by-Step)**:

**Step 1: Verify Port Number**
1. Open the Game-Side Settings
2. Expand Advanced Settings
3. Check the "OSC Port" (Default: 9001)
4. Verify the same port number is configured on VRChat side

**Step 2: Enable OSC on VRChat Side**
1. Launch VRChat
2. Open the Settings menu
3. Check "Enable OSC"
4. Restart VRChat

**Step 3: Check Firewall Settings**
1. Open Windows Security Center
2. Click on "Firewall & network protection"
3. Click on "Advanced settings"
4. Verify that the OSC port (9001, etc.) is allowed in both "Inbound rules" and "Outbound rules"
5. If not allowed, add a new rule

**Step 4: Check for Port Conflicts**
1. Open Command Prompt (Windows + R → cmd)
2. Run the following command:
   ```
   netstat -ano | findstr :9001
   ```
3. Verify that no other processes are using the port
4. If in use, change to a different port number

**Step 5: Restart VSA**
1. Completely close VSA
2. Wait a few seconds
3. Restart VSA
4. Use the camera in VRChat

#### VRChat Launch Is Not Detected

**Symptom**: VSA does not detect when VRChat is launched (notification does not appear)

**Possible Causes**:
- Monitoring function is disabled
- VRChat process detection failed

**Solution**:

**Step 1: Verify Monitoring Function Is Enabled**
1. Open the Game-Side Settings
2. Verify the toggle switch is enabled (ON)

**Step 2: Restart VRChat**
1. Completely close VRChat
2. Restart VSA as well
3. Launch VRChat

### Google Drive Integration-Related Issues

#### Upload Fails

**Symptom**: Attempting to upload favorite photos to Google Drive results in an error

**Possible Causes**:
- No network connection
- Google Drive storage is full
- Authentication has expired

**Solution (Step-by-Step)**:

**Step 1: Verify Network Connection**
1. Check the Windows network icon
2. Verify internet connection is working properly
3. Try accessing Google Drive in another browser
4. If unable to access, restart your Wi-Fi router

**Step 2: Check Google Drive Storage**
1. Open Google Drive in a browser
2. Check storage usage
3. If full, delete unnecessary files
4. For free plan, consider upgrading to a paid plan

**Step 3: Verify Authentication Status**
1. Open Account Settings
2. Check Google Drive authentication status
3. Click "Logout"
4. Click "Login with Google Drive" to re-authenticate

**Step 4: Try Manual Upload**
1. Follow the manual upload instructions in the Favorites Guide
2. Verify that manual upload is possible
3. If possible, review automatic upload settings

#### Authentication Error Occurs

**Symptom**: "Authentication failed" error is displayed when logging in to Google Drive

**Possible Causes**:
- Browser cache is corrupted
- Google account security settings
- Pop-up blocker is blocking login

**Solution (Step-by-Step)**:

**Step 1: Clear Browser Cache**
1. Open a browser (Chrome recommended)
2. Press Ctrl + Shift + Delete
3. Check "Cached images and files"
4. Click "Clear browsing data"

**Step 2: Check Pop-up Blocker**
1. Check the icon on the left side of the browser address bar
2. If pop-ups are blocked, allow them

**Step 3: Try Another Browser**
1. Try with another browser (Edge or Firefox)
2. Verify if authentication succeeds

**Step 4: Google Account Security Settings**
1. Open Google Account Settings
2. Click on "Security"
3. Check "Allow less secure app access"
4. Adjust settings as needed

**Step 5: Restart VSA**
1. Completely close VSA
2. Wait a few seconds
3. Restart VSA and try logging in again

### Notification-Related Issues

#### Notifications Are Not Displayed

**Symptom**: Settings show notifications are enabled, but desktop notifications do not appear

**Possible Causes**:
- VSA is not allowed in Windows notification settings
- Focus Assist is enabled
- Notification volume is muted

**Solution (Step-by-Step)**:

**Step 1: Check Windows Notification Settings**
1. Open Windows Settings (Windows + I)
2. Click on "System"
3. Click on "Notifications"
4. Verify that VSA is included in the allowed apps list
5. If not, add it from "Allowed notifications"

**Step 2: Check Focus Assist**
1. Open Windows Action Center (Win + A)
2. Verify that "Focus Assist" is not turned "On"
3. If on, turn it off

**Step 3: Check Notification Settings**
1. Open VSA Settings
2. Select the "Notifications" panel
3. Verify that "Desktop Notifications" is enabled
4. Verify that individual notification types are enabled

**Step 4: Check Notification Volume**
1. Check Windows Volume Mixer
2. Verify that VSA app is not muted
3. Check master volume level

### Performance-Related Issues

#### Application Startup Is Slow

**Symptom**: VSA takes tens of seconds or more to start

**Possible Causes**:
- Database is large
- Large number of photos
- Disk is slow

**Solution (By Priority)**:

**Solution 1: Delete Unnecessary Photos**
1. Select old photos in the gallery
2. Click the Delete button
3. Database size will be reduced
4. Verify if startup speed improves

**Solution 2: Optimize Disk**
1. Open Windows Settings
2. Click on "Storage"
3. Click on "Drive optimization"
4. Select the drive and click "Optimize"

**Solution 3: Install on SSD**
- Installing VSA on an SSD will improve startup speed
- If running on HDD, consider migrating to SSD

#### Memory Usage Is High

**Symptom**: VSA memory usage keeps increasing or your PC becomes slow

**Possible Causes**:
- Large number of photos being loaded
- Memory leak
- Thumbnail cache is large

**Solution (By Priority)**:

**Solution 1: Reduce Thumbnail Size**
1. Display the gallery
2. Drag the zoom slider to the left
3. Reduce thumbnail size
4. Check if memory usage decreases

**Solution 2: Close Photo Details Sidebar**
1. Close the open photo details panel
2. Check if memory usage decreases

**Solution 3: Restart the Application**
1. Completely close VSA
2. Wait a few seconds
3. Restart VSA
4. Memory will be reset

**Solution 4: Clear Cache**
1. Close VSA
2. Delete the following folder:
   ```
   %APPDATA%/VSA/cache/
   ```
3. Restart VSA

## How to Check Log Files

By examining VSA's detailed logs, you can more accurately identify the cause of problems.

### Log File Location

```
%APPDATA%/VSA/logs/
```

**Shortcut**:
1. Windows Key + R
2. Type `%APPDATA%` and press Enter
3. Double-click the `VSA` folder
4. Double-click the `logs` folder

### Log File Structure

Log files are generated on a daily basis:

```
logs/
├── 2024-01-10.log
├── 2024-01-09.log
└── 2024-01-08.log
```

**To open the latest log file**: Open the file with today's date.

### How to Read Log Files

Log files are text files that can be opened in Notepad or VSCode.

**How to Identify Log Levels**:

| Log Level | Symbol | Meaning |
|-----------|--------|---------|
| ERROR | [ERROR] | Critical error (problem has occurred) |
| WARN | [WARN] | Warning (caution needed) |
| INFO | [INFO] | Normal information (reference info) |
| DEBUG | [DEBUG] | Debug information (for developers) |

**How to Check for Errors**:
1. Open the latest log file in a text editor
2. Use Ctrl + F to search for "ERROR"
3. Check the error message
4. Take action based on the error message

**Example**:
```
[2024-01-10 14:32:15] [ERROR] Failed to connect to screenshot folder: Access Denied
```

This error indicates that there are no access permissions to the screenshot folder.

## Database Rebuild

If the database becomes corrupted, it can be rebuilt.

**Warning**: Rebuilding the database may result in loss of favorite tags and other custom data. Back up your data before proceeding.

### Steps

**Step 1: Enable Developer Mode**
1. Open Settings
2. Select the "Appearance" panel
3. Enable "Developer Mode"
4. Click "Save"

**Step 2: Open Developer Menu**
1. A "Developer" menu will appear in the sidebar
2. Click on "Developer"

**Step 3: Rebuild Database**
1. Find the "Rebuild Database" button
2. Click it
3. Select "Rebuild" in the confirmation dialog

**Step 4: Restart the Application**
1. VSA will automatically restart
2. Database rebuild will complete

**Step 5: Verify**
1. Display the gallery
2. Verify that photos are displayed correctly

## Reset Settings File

If the settings file becomes corrupted, it can be reset.

**Warning**: After reset, all settings will revert to defaults. Take note of important settings beforehand.

### Steps

**Step 1: Close VSA**
1. Completely close VSA
2. Verify all VSA processes have closed (check Task Manager)

**Step 2: Delete Settings File**
1. Windows Key + R
2. Type `%APPDATA%` and press Enter
3. Open the `VSA` folder
4. Delete the `settings.json` file

**Step 3: Restart VSA**
1. Launch VSA
2. Setup wizard will appear
3. Perform initial setup again

**How to Create a Backup**:
1. Close VSA
2. Copy `%APPDATA%/VSA/settings.json`
3. Save it to a safe location as `settings.json.backup`

**How to Restore from Backup**:
1. Copy `settings.json.backup` to the `%APPDATA%/VSA/` folder
2. Rename it to `settings.json`
3. Restart VSA

## How to Contact Support

If the above solutions do not resolve your issue, you can contact support.

### Information Required for Inquiry

Please provide the following information:

**1. Environment Information**:
- VSA version (check in Settings > Update)
- Windows version (Windows + R → winver)
- PC specifications (CPU, memory, disk)

**2. Problem Details**:
- Specific symptoms occurring
- When the problem started occurring
- Steps to reproduce the problem

**3. Error Messages**:
- Take a screenshot of any displayed error messages

**4. Log Files**:
- Latest log file (`%APPDATA%/VSA/logs/[date].log`)

### Contact Methods

**GitHub Issues**:
- [VSA-MainApp Issues](https://github.com/your-repo/issues)
- GitHub account is required
- Provide detailed information according to the template

**Email**:
- support@vsa-app.com (provisional)
- Include detailed inquiry and the above information

## Related Information

- [FAQ](faq.md) - Frequently Asked Questions
- [Game-Side Configuration Guide](game-config.md) - Configuration Troubleshooting
- [Settings Screen Complete Guide](settings-guide.md) - Settings Details
- [Favorites Guide](favorites-guide.md) - Google Drive Integration Troubleshooting
