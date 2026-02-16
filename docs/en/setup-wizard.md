# Initial Setup Guide

When you launch the VSA app for the first time, the setup wizard appears. This guide explains each step of the setup wizard in detail.

## Setup Wizard Overview

The setup wizard supports basic configuration when using VSA for the first time.

**Time Required**: 2-5 minutes

**When Wizard Appears**:
- When launching VSA for the first time
- When settings file is deleted
- During major version upgrades

**Skippable**: You can skip at any time with the "Skip" button

## Setup Steps

### Step 1: Welcome Screen

An introduction page for the VSA application.

**Display Contents**:
- VSA logo and product name
- Brief description
- Main features of VSA

**Description Includes**:
- VRChat photo management
- JPEG XL compression feature
- Automatic metadata extraction
- Google Drive integration

**Operations**:
- "Next" button: Proceed to next step
- "Skip" button: Skip setup and go to main screen

### Step 2: Language and Theme Selection

Select the app display language and visual theme.

#### Language Settings

**Options**:
- **Japanese**: All UI elements and documents display in Japanese
- **English**: All UI elements and documents display in English

**How to Select**:
1. Select language from radio button or dropdown
2. Selection may be applied immediately

**Change Later**:
- Can be changed in Settings > Appearance > Language Settings

#### Theme Settings

**Theme Modes**:
- **Light**: Bright color scheme (recommended for bright environments)
- **Dark**: Dark color scheme (reduces eye strain)
- **System**: Auto-follow Windows settings (recommended)

**How to Select**:
1. Select theme mode
2. Appearance changes immediately in preview

**Change Later**:
- Can be changed in Settings > Appearance > Theme Settings

#### Theme Color Selector

Select the accent color for the app.

**15 Color Presets**:
- Blue, Sky Blue, Purple, Lavender
- Pink, Hot Pink, Red, Orange
- Green, Lime Green, Turquoise, Cyan
- Gray, Gold, and more

**How to Select**:
1. Click desired color
2. App accent colors change

**Change Later**:
- Can be changed in Settings > Appearance > Theme Color Selector

### Step 3: Folder Settings

Specify the VRChat screenshot folder.

#### Screenshot Folder Setting

Specify the folder where VRChat saves photos.

**Default Path**:
```
C:\Users\[Username]\Pictures\VRChat
```

**How to Set**:
1. Click "Select Folder" button
2. Folder selection dialog opens
3. Select VRChat photo folder
4. Click "Select Folder"

**How to Verify**:
- Path is displayed
- Confirm path is correct

**VRChat Default Folder Location**:
```
Windows: C:\Users\[Username]\Pictures\VRChat
```

#### If Folder Not Found

**Steps**:
1. Open Windows Explorer
2. Manually open `C:\Users\[Username]\Pictures\`
3. Check if `VRChat` folder exists

**If VRChat Not Yet Launched**:
- Launch VRChat and take one screenshot
- `Pictures\VRChat` folder will be auto-created

**If Using Custom Folder**:
1. Click "Select Folder" in wizard
2. Select custom folder configured in VRChat
3. Click "Select Folder"

### Step 4: Auto-Launch Setting

Configure whether to auto-launch VSA when Windows starts.

**Options**:
- **Enabled**: VSA automatically launches each time Windows starts
- **Disabled**: Must launch VSA manually

**Benefits of Enabling**:
- VSA always runs when playing VRChat
- Automatic photo import possible
- No configuration forgotten

**Benefits of Disabling**:
- Don't launch VSA when not needed
- Minimize resource consumption
- Manual complete control

**How to Select**:
1. Select with toggle or checkbox
2. Turn on to enable, off to disable

**Change Later**:
- Settings > System > Auto-launch
- Or from Windows startup settings

### Step 5: Complete

Setup is complete and move to main screen.

**Completion Screen**:
- Confirm settings
- "Complete" button

**After Completion**:
1. Click "Complete"
2. Main screen appears
3. Gallery view displays
4. Import process begins (specified folder is scanned)

## Skipping Setup

To skip setup mid-process:

**Method 1: Click "Skip" at Each Step**
- Skip current step
- Move to main screen
- Remaining steps not shown

**Method 2: Click "Skip" Button (Wizard Side)**
- All steps are skipped
- App launches with default settings

**After Skipping**:
- All settings set to default values
- Can be changed later in settings screen

## Re-running Setup

To redo setup:

### Method 1: Delete Settings File

**Steps**:
1. Close VSA
2. Windows Key + R
3. Type `%APPDATA%` and press Enter
4. Open `VSA` folder
5. Delete `settings.json` file
6. Restart VSA
7. Setup wizard reappears

### Method 2: From Wizard (Planned for Future)

Future versions will add option to re-run setup from settings screen.

## Troubleshooting

### Setup Won't Complete

**Symptom**: Wizard won't progress or becomes unresponsive

**Causes and Solutions**:

**App Not Responding**:
1. Ctrl + Alt + Delete
2. Open Task Manager
3. Select VSA process
4. Click "End Task"
5. Restart VSA

**Insufficient Disk Space**:
1. Check disk space
2. Delete unnecessary files
3. Ensure several GB of free space
4. Restart VSA

**"Next" Button Unresponsive During Wizard**:
1. Click mouse again
2. Press keyboard Enter key
3. Click different button
4. Check if responsive

### Can't Select Folder

**Symptom**: Dialog doesn't appear when trying to select folder

**Causes and Solutions**:

**Insufficient Administrator Rights**:
1. Run VSA as administrator
2. Right-click > "Run as Administrator"
3. Run wizard again

**Folder Access Permissions**:
1. Right-click target folder
2. Open Properties
3. Check Security tab permissions
4. Confirm Read permission exists

### VRChat Folder Not Found

**Symptom**: Can't find VRChat folder despite installation

**Verification Steps**:

**Actual VRChat Installation**:
1. Confirm VRChat is actually installed
2. Launch VRChat and take one screenshot
3. After screenshot, check `Pictures\VRChat` folder

**Folder Display Settings**:
1. Open Windows Explorer
2. Enable "Show hidden files" from View tab
3. Check if hidden folders display

**If Using Custom Folder**:
1. Check custom output folder in VRChat settings
2. Specify that folder in wizard

## Best Practices

### Setup Tips

**Language Settings**:
- Select language you understand well
- Documents display in same language

**Theme Selection**:
- Recommended: "System" to match Windows settings
- Auto-switches based on environment and time

**Folder Settings**:
- If not default folder, check VRChat settings
- If using multiple folders, specify main folder

**Auto-Launch Setting**:
- Enable if you want VSA monitoring when playing VRChat
- Disable if temporarily not using VSA

## After Setup

After completing setup, recommend these steps:

1. **Check Gallery**: Verify imported photos
2. **Check Metadata**: Confirm world name and usernames display in photo details
3. **Verify Game Config**: See [Game Config Guide](game-config.md) for complete VRChat setup
4. **Google Drive Integration**: Perform Google Drive auth in [Account Guide](account-guide.md)
5. **Run Tutorial**: Learn features from in-app tutorial

## Related Documentation

- [Basic Usage](../basic-usage.md) - Overall VSA usage
- [Game Config Guide](game-config.md) - Detailed VRChat integration settings
- [Settings Guide](settings-guide.md) - Detailed settings options
- [Troubleshooting Guide](troubleshooting.md) - If problems occur
