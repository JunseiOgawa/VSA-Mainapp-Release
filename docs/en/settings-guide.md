# Settings Guide - Complete Reference

The Settings panel allows you to customize all aspects of VSA's appearance, behavior, and functionality across 8 different configuration panels.

## Accessing Settings

Click the gear icon (⚙️) in the sidebar to open the Settings screen.

The left menu displays 10 tabs, each controlling different aspects of the application:

1. **Appearance** - Theme and color settings, language selection
2. **Animation** - Visual effects configuration
3. **File** - File operations settings
4. **Notification** - Notification settings
5. **Shortcut** - Keyboard shortcut configuration
6. **VDI** - VDI integration settings
7. **Favorites** - Favorites management
8. **System** - Auto-launch settings
9. **X Post** - X posting preset management
10. **Update** - Update settings

## Appearance Panel

Configure how VSA looks and displays information.

### Theme Settings

Choose the visual theme for the application.

**Theme Options**:
- **Light**: White background with dark text (for bright environments)
- **Dark**: Dark background with light text (reduces eye strain)
- **System Linked**: Automatically follows Windows theme settings (Recommended)

**How to Change**:
1. Select your preferred theme
2. Changes apply immediately with smooth fade transition
3. Window content updates in real-time

### Language Setting

Choose the UI language for the entire application.

**Available Languages**:
- **Japanese**: Complete UI, menus, and dialogs in Japanese
- **English**: Complete UI, menus, and dialogs in English

**How to Change**:
1. Select language from dropdown
2. Application UI updates immediately
3. All dialogs and tooltips change to selected language
4. Setting persists across sessions

**Note**: Documentation language can be set independently in the Documents panel.

### Theme Color Selector

Choose an accent color for the application interface.

**15 Preset Colors Available**:
- Blues: Sky Blue, Blue, Steel Blue
- Purples: Purple, Lavender, Violet
- Reds: Red, Pink, Hot Pink
- Oranges: Orange, Amber
- Greens: Green, Lime Green
- Teals: Cyan, Turquoise
- Grays: Gray, Charcoal
- Others: Gold, Custom

**How to Use**:
1. Click on desired color swatch
2. Color preview appears in real-time
3. All UI elements (buttons, accents, highlights) change immediately
4. Selection applies to entire application

**Animation Effects**:
- Color transitions include smooth animation
- Fade-in effect when selecting new color
- Multiple interactive elements animate simultaneously

## Animation Panel

Control visual effects and transitions throughout the application.

### Animation Effects Toggle

Enable or disable UI animations and transition effects.

**When Enabled**:
- Fade transitions between views
- Smooth scroll animations
- Button press animations
- Panel opening/closing animations

**When Disabled**:
- UI changes appear instantly
- No transition effects
- Faster perceived responsiveness
- Lower GPU usage

**Use Cases**:
- Enable for modern, polished feel
- Disable if animations cause discomfort or on low-end systems

## File Panel

Manage file handling and history settings.

### Auto-Save Configuration

Control automatic file saving behavior.

**Options**:
- Enable/Disable auto-save
- Set save interval (configurable)
- Manual save still available via Ctrl+S

### History Management

**Recent Files Display**:
- Control how many recent items are shown
- Range: 5 to 50 items

**Clear History**:
1. Click "Clear History" button
2. Confirm in dialog
3. Recent files list clears

### Preview Settings

Configure preview quality and performance.

**Preview Quality**:
- Low: Faster loading, lower quality previews
- Medium: Balanced quality and speed
- High: Best quality (may impact performance with large libraries)

## Notification Panel

Configure desktop notifications and alerts.

### Desktop Notifications

Control whether VSA sends Windows notifications.

**Enable/Disable**:
- Toggle desktop notifications ON or OFF
- When disabled, no system notifications appear

### Notification Types

Choose which events trigger notifications:

**Import Notifications**:
- Trigger when importing folder completes
- Shows file count and status

**Photo Import In-Progress**:
- Notify when new screenshots detected
- Shows count of incoming photos

**Compression Complete**:
- Notify when JXL compression finishes
- Shows compression statistics

**Error Notifications**:
- Alert when errors occur
- Prevents silent failures

**VRChat Startup/Shutdown**:
- Notify when VRChat detected starting/stopping
- Useful for workflow awareness

### Notification Sound

**Enable/Disable Sound**:
- Toggle notification sounds ON or OFF
- When enabled, audible alert for each notification

**Volume Control**: (if available)
- Adjust notification volume level
- Range typically 0-100%

## Shortcut Panel

Manage keyboard shortcuts for frequent operations.

### Implemented Shortcuts (4 total)

**Display Operations**:
- **Screen Size Toggle** (F10): Cycle through window sizes (1280×720 → 1600×900 → 1920×1080 → 2560×1440)
- **Fullscreen Toggle** (F11): Switch between window and fullscreen modes
- **Gallery Zoom In** (Ctrl + =): Increase thumbnail size
- **Gallery Zoom Out** (Ctrl + −): Decrease thumbnail size

### Customizing Shortcuts

**How to Change a Shortcut**:
1. Locate the shortcut you want to change
2. Click on the shortcut field (becomes highlighted)
3. Enter your new key combination:
   - Press and hold modifier keys (Ctrl, Shift, Alt, Win)
   - While holding modifiers, press your desired key
   - Release all keys
4. New combination displays in the field
5. Click "Save" to confirm

**Example Combinations**:
- Single key: `F5`
- With modifier: `Ctrl + Shift + S`
- Multiple modifiers: `Ctrl + Alt + Delete`

### Resetting to Defaults

**Reset All Shortcuts**:
1. Open Settings > Shortcut panel
2. Click "Reset to Default" button
3. Confirm in dialog
4. All shortcuts return to default values

**Warning**: This action cannot be undone. Note current customizations if needed.

See [Keyboard Shortcuts Complete List](keyboard-shortcuts.md) for detailed information.

## VDI Panel

Configure VDI (Virtual Desktop Infrastructure) integration features.

### VDI Linked Features

**VDI Auto-Launch**:
- Automatically launch associated VDI when starting VSA
- Useful for remote desktop workflows

### Camera Integration

**VDI Camera Options**:
- Configure camera access in VDI environments
- May vary depending on VDI setup

## Favorites Panel

Manage favorites data and legacy folder migration.

### Favorites Folder Migration

**Purpose**: Move favorites data from old locations to new database.

**Legacy Folder Import**:
1. Click "Import Legacy Folder"
2. Select old favorites folder location
3. VSA imports all legacy data
4. Favorites appear in Favorites view

**Note**: Modern VSA uses SQLite database for favorites. Legacy folder migration preserves existing data.

### Database Management

**View Favorites Database**:
- Location: `%APPDATA%\VSA\favorites.db`
- Automatically created on first favorites action

**Backup Favorites**:
1. Locate `%APPDATA%\VSA\favorites.db`
2. Copy to safe location
3. Keep as backup

**Restore from Backup**:
1. Copy backup file to `%APPDATA%\VSA\`
2. Overwrite current `favorites.db`
3. Restart VSA

See [Favorites Guide](favorites-guide.md) for complete favorites information.

## Update Panel

Control automatic update checking and version information.

### Auto-Update Check

**Enable/Disable Checking**:
- Toggle automatic update checking
- When enabled, VSA checks for updates periodically

### Version Information

**Current Version Display**:
- Shows installed VSA version
- Format: X.X.X

**GitHub Releases Link**:
- Click link to open GitHub Releases page in browser
- View available versions
- Download latest release if desired
- Read changelog for each version

### Update Notifications

When new version available:
- Notification appears in UI
- Can download or dismiss
- Check can be done manually anytime

## Resetting All Settings

**Reset to Defaults**:
1. Settings > scroll to bottom
2. Click "Reset All Settings" button
3. Confirm in dialog
4. All settings revert to default values
5. Application restarts automatically

**Warning**: This action cannot be undone. All customizations will be lost.

## Settings Storage

Settings are stored in:
```
%APPDATA%\VSA\settings.json
```

**Backup Settings**:
1. Navigate to `%APPDATA%\VSA\`
2. Copy `settings.json` to safe location
3. Keep as backup before major changes

**Restore Settings**:
1. Copy backup `settings.json` to `%APPDATA%\VSA\`
2. Overwrite current file
3. Restart VSA

## System Panel

Configure system-level application settings.

### Auto-Launch Settings

Configure automatic VSA launch when Windows starts.

#### Enable/Disable Auto-Launch

**When Enabled**:
- VSA automatically launches each Windows startup
- Available immediately after startup
- Runs in background

**When Disabled**:
- Manual VSA launch required
- Save Windows resources

#### Startup Registration

**How to Register**:
1. Open "System" panel
2. Toggle "Auto-Launch" ON
3. Click "Register to Startup"
4. Click "Yes" when admin dialog appears
5. Registration to startup folder complete

**Registration Location**:
```
C:\Users\[Username]\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup
```

**How to Unregister**:
1. Toggle "Auto-Launch" OFF
2. Optionally delete from startup folder manually

### Startup Options

#### Background Launch

VSA launches in background when Windows starts.

**Background Launch**:
- Window not displayed, minimized to taskbar
- Photo monitoring auto-enables
- File monitoring auto-starts

#### Startup Behavior

Select initial behavior on auto-launch.

**Options**:
- **Normal Launch**: Display gallery screen
- **Background**: Launch without display
- **Minimize**: Launch minimized to taskbar

**Recommended**: "Background" (optimal for photo auto-monitoring)

### Related Documentation

See [Setup Wizard Guide](setup-wizard.md) for details.

## X Post Panel

Configure X posting feature settings.

### Preset Management

Save and manage frequently used posting settings.

#### Preset List

**Display Information**:
- Preset name
- Creation date/time
- Last used date/time
- Settings summary

#### Create/Edit/Delete Presets

**Create Steps**:
1. Click "New Preset"
2. Enter preset name
3. Customize frame settings
4. Click "Save"

**Edit Steps**:
1. Select preset to edit
2. Change settings
3. Click "Save"

**Delete Steps**:
1. Select preset to delete
2. Click "Delete" button
3. Click "Delete" in confirmation dialog

### Template Settings

Configure default text for X posting.

#### Text Template

**Default Text Field**:
1. Enter initial post text in template field
2. Can use variables (`{world}`, `{date}`, etc.)
3. Click "Save"

**Available Variables**:
- `{world}` - World name
- `{date}` - Capture time
- `{camera}` - Camera type
- `{user}` - Photographer name

**Example**:
```
VRChat photo taken.
World: {world}
Time: {date}
```

#### Hashtag Settings

Pre-register frequently used hashtags.

**Add Hashtags**:
1. Click "Add" in "Hashtags" section
2. Enter hashtag (starts with `#`)
3. Click "Save"

**Using Hashtags**:
- Registered hashtags display as suggestions
- One-click add when posting

**Delete Hashtags**:
1. Select hashtag to delete
2. Click "Delete" button

### X Account Authentication

Manage X (Twitter) account authentication.

#### Check Auth Status

**Display Information**:
- Auth username
- Auth date/time
- Token expiration

#### Re-authenticate

Re-authenticate when token expires.

**Re-auth Steps**:
1. Click "Re-authenticate" button
2. Browser opens to X (Twitter) auth page
3. Click "Authorize"
4. Return to VSA

#### Remove Auth

Remove X posting feature integration.

**Remove Steps**:
1. Click "Remove Authentication" button
2. Click "Remove" in confirmation dialog
3. X posting feature becomes inactive

### Related Documentation

See [X Posting Feature Guide](x-post-guide.md) for details.

## Tips

- **Performance**: Disable animations if VSA feels slow on older hardware
- **Notifications**: Disable non-critical notifications to reduce distractions
- **Shortcuts**: Create shortcuts for operations you perform frequently
- **Backup**: Backup settings.json periodically in case of corruption
- **Theme**: Use System-Linked theme for automatic light/dark switching

## Related Documentation

- [Keyboard Shortcuts Complete List](keyboard-shortcuts.md) - All shortcut details
- [Favorites Guide](favorites-guide.md) - Favorites feature overview
- [Game Configuration Guide](game-config.md) - VRChat integration settings
- [Troubleshooting Guide](troubleshooting.md) - Settings-related issues
