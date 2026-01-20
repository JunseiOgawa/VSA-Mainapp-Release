# Game Configuration Guide

The Game Config panel allows you to configure VRChat integration settings and enable automatic metadata extraction for your screenshots.

## Overview

The Game Config settings enable VSA to communicate with VRChat and automatically extract metadata such as world names, user information, and camera parameters.

**Access Method**:
1. Click the settings gear icon (⚙️) in the sidebar
2. Select "Game Config" from the left menu

## Monitoring Status Management

### Starting/Stopping Monitoring

The monitoring toggle controls whether VSA actively monitors VRChat's activity.

**How to Enable**:
1. Locate the monitoring toggle switch
2. Click to toggle ON
3. VSA will now monitor VRChat processes

**What Monitoring Does**:
- Detects when VRChat starts and stops
- Monitors for new screenshots
- Prepares metadata extraction
- Triggers automatic import if enabled

**Monitoring Status Indicator**:
- Green indicator: Monitoring is active
- Gray indicator: Monitoring is inactive

### Checking Monitoring Status

**Current Status Display**:
- The indicator at the top shows if monitoring is currently active
- Status updates in real-time
- Visual confirmation when VRChat is detected

## Detailed Settings (Accordion Sections)

Expand the accordion sections to access detailed configuration options.

### Folder Settings

Configure the folders where VSA reads and writes data.

**Screenshot Folder**:
- Default: `C:\Users\[Username]\Pictures\VRChat`
- The location where VRChat saves screenshot files
- Used for automatic photo detection and import
- **How to Change**:
  1. Click "Select Folder" button
  2. Browse to your VRChat screenshot folder
  3. Click "Select Folder" to confirm
- **Tooltip**: Hover over the folder path field to see the full path

**Metadata Output Folder**:
- Where VRChat logs metadata (world names, user information)
- Critical for extracting world and user metadata
- Default: VRChat's built-in log directory
- **How to Change**:
  1. Open VRChat Settings
  2. Find the output log location in VRChat settings
  3. Paste that path in VSA's "Metadata Output Folder" field
- **VRChat Log Location**: `C:\Users\[Username]\AppData\LocalLow\VRChat\VRChat\`

**Log Folder**:
- VSA's internal log directory for troubleshooting
- Default: `%APPDATA%\VSA\logs\`
- Contains debugging information if issues occur
- **Reset to Default**:
  1. Click "Reset" button next to the field
  2. Folder returns to default location

**Folder Path Display with Tooltip**:
- Full paths are hidden by default (shows shortened version)
- Hover over any folder path to see the complete path
- Useful for verifying correct folder configuration

### Auto Functions Settings

Configure automatic processes when VRChat is detected.

**Automatic Import**:
- When enabled: New screenshots are automatically imported into VSA when detected
- When disabled: Manual import required
- **Recommendation**: Enable for seamless workflow during VRChat sessions

**Automatic Compression**:
- When enabled: Screenshots matching compression criteria are automatically compressed
- When disabled: Manual compression required
- See [JXL Compression Guide](jxl-compression.md) for compression details

**Background Processing**:
- Determines whether to process files in the background or foreground
- Low priority background processing allows continued app usage
- See [JXL Compression Guide](jxl-compression.md) for more information

### OSC Settings

OSC (Open Sound Control) enables camera parameter extraction from VRChat.

**OSC Port Configuration**:
- Default Port: 9001
- This is the port VSA uses to receive OSC messages from VRChat
- **How to Configure**:
  1. Verify VRChat OSC setting uses the same port (9001 by default)
  2. If port conflict exists, change to another port (e.g., 9002)
  3. Update both VRChat and VSA to use the same port

**OSC Communication Overview**:
- VRChat sends camera parameter data via OSC protocol
- VSA receives and stores these parameters
- Parameters are embedded in screenshot metadata
- Requires compatible camera (VirtualLens2 or Integral)

**Supported Cameras for OSC**:
- VirtualLens2 (recommended for parameter extraction)
- Integral (advanced lens with OSC support)
- Standard VRChat camera (no OSC parameters)

**How OSC Works**:
1. User adjusts camera settings in VRChat
2. VRChat broadcasts OSC messages with camera data
3. VSA listens on OSC port and stores the parameters
4. When screenshot is taken, parameters are embedded
5. VSA can later display detailed camera information

**Verifying OSC is Working**:
1. Adjust a camera parameter (e.g., Aperture) in VRChat
2. Check VSA logs for OSC messages
3. Open Developer Mode to see OSC statistics
4. See Troubleshooting section if no data received

## Saving Settings

Changes to Game Config settings are automatically detected.

**Auto-Save Behavior**:
- Settings save automatically when changed
- No manual save button required
- Visual confirmation shows when changes are saved

**Change Indicators**:
- Fields highlight when modified
- Status message confirms successful save
- Error messages display if save fails

**Important**: Do not close the app immediately after changing settings - allow a moment for changes to save.

## Troubleshooting

### Monitoring Cannot Be Started

**Symptom**: Toggle switch won't enable or monitoring shows as inactive

**Causes and Solutions**:

**VSA doesn't have permission to monitor VRChat**:
1. Run VSA as Administrator
   - Right-click VSA shortcut → "Run as Administrator"
2. Check Windows Defender isn't blocking VSA
   - Open Windows Security
   - Add VSA to Firewall exceptions
3. Disable antivirus monitoring temporarily
   - Some security software blocks process monitoring

**VRChat isn't installed or not running**:
1. Install VRChat from official source
2. Launch VRChat at least once to initialize
3. Close VRChat completely before testing VSA monitoring
4. Try toggling monitoring again

### Metadata Not Extracted

**Symptom**: World names and user information showing as "Unknown"

**Check VRChat Log Output**:
1. Confirm VRChat is outputting logs
2. Check location: `C:\Users\[Username]\AppData\LocalLow\VRChat\VRChat\`
3. Look for `output_log_*.txt` files dated today
4. If not found, VRChat logging may be disabled

**Verify Game Config Settings**:
1. Open Game Config panel
2. Confirm "Metadata Output Folder" is set to VRChat log directory
3. Verify folder path is correct
4. Try changing to absolute path if using shortcuts

**Test Metadata Extraction**:
1. Open VRChat and enter a world
2. Wait 5-10 seconds for world information to be logged
3. Take a screenshot in VRChat
4. Return to VSA and check if metadata appears
5. If still not working, check troubleshooting below

### OSC Communication Not Established

**Symptom**: Camera parameters not showing in screenshot details

**Verify VRChat OSC Settings**:
1. Open VRChat Settings
2. Navigate to OSC configuration
3. Ensure OSC is enabled
4. Confirm port matches VSA setting (default 9001)
5. If port is different, update VSA to match

**Check Port Availability**:
1. Open Command Prompt (Windows + R, type `cmd`)
2. Run: `netstat -ano | findstr :9001`
3. If port is in use, change to different port:
   - VSA: Change "OSC Port" to 9002
   - VRChat: Change OSC port to 9002
4. Restart both applications

**Test OSC Connection**:
1. Start VSA and enable monitoring
2. Open VRChat
3. Select VirtualLens2 camera
4. Adjust Aperture slider
5. Return to VSA and check logs
6. Look for OSC message confirmation

**Enable Developer Mode for OSC Debugging**:
1. Go to Settings > Developer Mode
2. Enable Developer Features
3. Check OSC statistics in Developer panel
4. Review received/sent message counts

### Configuration File Corruption

**Symptom**: Settings reset to defaults or won't save

**Solution**:
1. Close VSA completely
2. Navigate to: `%APPDATA%\VSA\`
3. Delete `config.json` file
4. Restart VSA
5. Reconfigure Game Config settings

## Related Documentation

- [VRChat Integration Guide](vrchat-integration.md) - Understanding metadata extraction
- [JXL Compression Guide](jxl-compression.md) - Auto compression configuration
- [Troubleshooting Guide](troubleshooting.md) - Detailed problem solutions
- [FAQ](faq.md) - Common questions

## Tips

- **Automatic Monitoring**: Enable monitoring when planning to use VRChat for smooth metadata extraction
- **OSC Verification**: If camera parameters aren't extracting, verify OSC is working before troubleshooting other settings
- **Log Review**: Check VSA logs (`%APPDATA%\VSA\logs\`) for detailed error information
- **Port Conflicts**: Use `netstat` command to check if port 9001 is available before configuring
- **Regular Testing**: After changing settings, take a test screenshot in VRChat to verify settings work correctly
