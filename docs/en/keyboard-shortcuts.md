# Keyboard Shortcuts List

Here is a list of keyboard shortcuts available in the VSA app. This guide explains all shortcuts and how to customize them.

## Implemented Shortcuts

Currently, the following 4 shortcuts are implemented.

### Display Shortcuts

| Operation | Shortcut | Description |
|-----------|----------|-------------|
| Screen Size Toggle | `F10` | Switch window size between presets (1280×720 → 1600×900 → 1920×1080 → 2560×1440) |
| Fullscreen Toggle | `F11` | Toggle between windowed and fullscreen modes |
| Gallery Zoom In | `Ctrl` + `=` | Increase gallery thumbnail size |
| Gallery Zoom Out | `Ctrl` + `-` | Decrease gallery thumbnail size |

### Shortcut Details

#### Screen Size Toggle (F10)

Change the window size in stages.

**Size Order**:
1. 1280 × 720 (default)
2. 1600 × 900
3. 1920 × 1080 (Full HD)
4. 2560 × 1440 (2K)
5. Back to 1280 × 720 (cycle)

**Use Cases**:
- Optimize screen size in multi-monitor environments
- Check display on different resolutions

#### Fullscreen Toggle (F11)

Switch between windowed and fullscreen modes.

**In Fullscreen Mode**:
- Title bar and taskbar are hidden
- Application displays on entire screen
- Photo viewing area is maximized

**In Windowed Mode**:
- Title bar and window frame are visible
- Resizing and dragging are possible
- Other applications can be displayed simultaneously

#### Gallery Zoom In (Ctrl + =)

Increase the thumbnail size in the gallery.

**Behavior**:
- Each press increases thumbnail size by approximately 10px
- Maximum size: 300×300px
- Further expansion is not possible when maximum is reached

**Use Cases**:
- View photo details in larger size
- Use with high-resolution monitors

#### Gallery Zoom Out (Ctrl + -)

Decrease the thumbnail size in the gallery.

**Behavior**:
- Each press decreases thumbnail size by approximately 10px
- Minimum size: 50×50px
- Further reduction is not possible when minimum is reached

**Use Cases**:
- Display many photos at once
- Quick review of large photo collections
- View date grouping

## Customization

### Changing Shortcut Keys

You can change default shortcuts to different key combinations.

**Steps**:

**Step 1: Open Settings**
1. Click the gear icon (⚙️) in the sidebar
2. The "Settings" screen appears

**Step 2: Select Shortcut Panel**
1. Click "Shortcut" from the left menu
2. All registered shortcuts are displayed

**Step 3: Click the Shortcut to Change**
1. Click the shortcut row you want to change
2. The field becomes active (highlighted)

**Step 4: Enter New Key Combination**
1. Hold modifier keys (Ctrl, Shift, Alt, Meta, etc.) and press the main key
2. Input appears on screen
3. Release keys to confirm

**Step 5: Save**
1. Click the "Save" button
2. Shortcut is updated

### Input Examples

**Example 1: Change to Ctrl + Shift + =**
1. Click the shortcut to change
2. Hold Ctrl key
3. Hold Shift key
4. Press = key
5. "Ctrl + Shift + =" appears
6. Click "Save"

**Example 2: Change to Single Key Only**
1. Click the shortcut to change
2. Press only the main key without modifier keys
3. Example: "F5"
4. Click "Save"

### Reset to Default

To restore all shortcuts to default values:

**Steps**:
1. Open Settings > "Shortcut" panel
2. Look for "Reset to Default" button
3. Click it
4. Select "Reset" in the confirmation dialog
5. All shortcuts return to defaults

**Note**: This action cannot be undone. If important, note current settings beforehand.

## Important Notes

### System Shortcut Conflicts

Conflicts may occur with Windows system shortcuts.

**Common Conflicting Shortcuts**:
- `Alt + Tab`: Window switching
- `Ctrl + C`: Copy
- `Ctrl + V`: Paste
- `Win` key combinations: Windows-specific operations

**If Conflict Occurs**:
- VSA shortcuts may take priority in some cases
- System shortcuts may take priority in others
- Behavior varies by environment

**Solution**:
- Change to a different key combination
- Use non-conflicting keys in Windows settings

### Application-Wide Scope

Shortcuts are active throughout the application.

**Shortcuts Active Only in Specific Screens**:
- Gallery Zoom (In/Out): Active only in gallery view
- Other shortcuts work on most screens

### Keyboard Layout Differences

Display may differ depending on your keyboard layout.

**Examples**:
- Japanese keyboard: = key position differs
- US layout keyboard: Key positions differ

**Solution**:
- Test input to confirm expected keys are entered
- If different, change to another key

## Future Additions

The following shortcuts are planned for future updates:

### File Operations
- Save (Ctrl + S)
- Save As (Ctrl + Shift + S)

### Navigation
- Go to Gallery (Ctrl + G)
- Go to Favorites (Ctrl + F)
- Open Search (Ctrl + /)

### Editing
- Delete (Delete)
- Undo (Ctrl + Z)
- Redo (Ctrl + Y)

### Display
- Show/Hide Sidebar (Ctrl + B)

See [Settings Guide](settings-guide.md) "Shortcut" section for details.

## Troubleshooting

### Shortcut Not Working

**Symptom**: Keys do not respond

**Causes and Solutions**:

**Modifier Keys Not Recognized Correctly**:
1. Check Settings > Shortcuts for registered key combinations
2. Confirm expected keys are set

**VSA Window Not Active**:
1. Click the VSA window
2. Confirm window is active (in front)
3. Ensure no other app is active

**Windows System Shortcut Takes Priority**:
1. Change to different key combination
2. Check Windows settings for conflicting shortcuts

### Shortcut Settings Reset

**Symptom**: Custom shortcuts return to default after app restart

**Causes**:
- Settings file corruption
- Insufficient disk space
- Permission issues

**Solution**:
1. Reconfigure settings
2. Restart app
3. If still unresolved, rebuild database in developer mode

### Keyboard Layout Not Recognized

**Symptom**: Keyboard layout differs, expected keys don't input correctly

**Solution**:
1. Check Windows keyboard settings
2. Adjust for your keyboard layout
3. If problem persists, try different key combinations

## Tips

- **Frequent Shortcuts**: Screen size toggle is convenient in large monitor environments
- **Zoom Feature**: Ctrl + = and Ctrl + - quickly adjust thumbnail sizes
- **Fullscreen**: F11 for fullscreen to view photos on large display
- **Dual Monitor**: Use F10 to adjust size and move windows between monitors

## Related Documentation

- [Settings Guide](settings-guide.md) - Shortcut settings details
- [Gallery Guide](gallery-guide.md) - Gallery zoom feature details
