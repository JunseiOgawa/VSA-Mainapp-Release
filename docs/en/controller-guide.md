# VirtualLens Controller Guide

VirtualLens Controller allows you to operate VirtualLens2 camera settings in real-time. Integration with VirtualLens2 avatars in VRChat is possible via OSC (Open Sound Control).

## VirtualLens Controller Overview

Using VirtualLens Controller:

- **Real-time Control**: Parameters reflect in VRChat real-time
- **Multiple Parameters**: Support focal distance, aperture, exposure, and more
- **Preset Saving**: Save frequently used settings as presets
- **Intuitive UI**: Easy operation with sliders and knobs

## Access Controller Screen

### Open from Menu

**Steps**:
1. Check sidebar menu (left side)
2. Look for "Controller" item
3. Click to open controller screen

### Keyboard Shortcut

Controller screen may have dedicated shortcut keys. See [Keyboard Shortcuts](keyboard-shortcuts.md) for details.

## Using Controller Screen

### Screen Composition

Controller screen consists of these sections:

- **Parameter Section**: Various camera parameter settings
- **Preset Section**: Preset save and load
- **OSC Status Display**: Communication status confirmation
- **Preview**: Real-time preview of settings reflected in VRChat

### Parameter Settings

#### Focal Length

Corresponds to VirtualLens2 zoom setting.

**Range**: 16mm - 300mm
**Unit**: mm
**Operation**:
- Drag slider left/right to adjust
- Direct input to specify value
- "Reset" button returns to default (50mm)

**Examples**:
- 16mm: Suitable for wide-angle shooting
- 50mm: Standard portrait shooting
- 200mm: Captures distant subjects large

#### Aperture

Controls image brightness and depth of field (bokeh).

**Range**: F1.4 - F16
**Unit**: F-stop
**Operation**:
- Drag slider left/right
- Direct input value
- "Reset" button returns to default (F4.0)

**Examples**:
- F1.4-F2.8: Background bokeh emphasizes subject (portrait-oriented)
- F4.0-F8.0: Balanced exposure and bokeh
- F11-F16: Overall sharp, background clear

#### Exposure

Adjusts overall image brightness.

**Range**: -5.0 - +5.0
**Unit**: EV (Exposure Value)
**Operation**:
- Drag slider left/right
- Direct input value
- "Auto" button sets to auto exposure

**Examples**:
- -5.0 - -2.0: Adjust darker environment shots (darker)
- 0.0: Standard exposure
- +2.0 - +5.0: Shoot dark areas brighter

#### Depth of Field

Controls bokeh strength.

**Range**: 0 - 100
**Operation**:
- Drag slider left/right
- Direct input value

**Examples**:
- 0: No bokeh (overall sharp)
- 50: Moderate bokeh
- 100: Maximum bokeh (strong background bokeh)

### Real-time Reflection

Parameter changes immediately reflect in VRChat camera.

**Verification**:
1. Equip VirtualLens2 in VRChat
2. Adjust parameters in controller screen
3. Confirm reflection in VRChat screen (viewfinder)

**Notes**:
- OSC communication must be properly established
- Network latency may cause frame delay reflection

## OSC Communication Settings

### What is OSC?

OSC (Open Sound Control) is a protocol that transmits parameters real-time over network. Exchange numerical data between VRChat and VSA.

### Port Settings

#### Default Port

**Default Value**: 9001

VRChat initial settings use port 9001. Usually works with this setting.

#### Change Port Number

**When Change Needed**:
- Port 9001 already in use by another app
- Network requires different port

**How to Change**:
1. Open "OSC Settings" section in controller screen
2. Enter desired port number in "Port Number" field
3. Click "Apply"
4. Set same port number on VRChat side too

### Verify Communication Status

#### Status Display

Communication status displays on controller screen:

- **Connected (green)**: Properly communicating with VRChat
- **Disconnected (gray)**: Communication not established with VRChat
- **Error (red)**: Communication error occurred

#### Diagnosis Method

**Steps**:
1. Equip VirtualLens2 in VRChat
2. Open controller screen
3. Wait until status becomes "Connected"
4. Change one parameter to test, confirm VRChat reflection

## Preset Management

### What are Presets?

Save preset settings combining camera parameters (focal distance, aperture, exposure, etc.).

### Save Preset

**Steps**:
1. Adjust each parameter to desired value
2. Click "Save" button in "Preset" section
3. Enter preset name (e.g., "Portrait", "Wide-angle")
4. Click "Save"

### Load Preset

**Steps**:
1. Select preset to load from list in "Preset" section
2. Click "Load" button
3. Saved parameter values all apply
4. Auto-reflect in VRChat

### Edit Preset

**Steps**:
1. Load preset
2. Change parameters
3. Click "Overwrite" button next to original preset name
4. Click "Overwrite" in confirmation dialog

### Delete Preset

**Steps**:
1. Select preset to delete
2. Click "Delete" button
3. Click "Delete" in confirmation dialog

## VRChat Side Settings

### Equip VirtualLens2 Avatar

VirtualLens Controller requires equipping avatar with VirtualLens2 camera in VRChat.

**Verification**:
1. Equip avatar in VRChat
2. Check View > Viewfinder if VirtualLens2 viewfinder displays

### Enable OSC (VRChat Side)

**VRChat Setup**:
1. Launch VRChat
2. Open Settings > OSC
3. Check "Enable OSC"
4. Verify port number is 9001 (or VSA-specified value)
5. Save settings

### Verify VirtualLens2 Parameters

Confirm VRChat VirtualLens2 supports these parameters:

- `/avatar/parameters/VL2_FocalLength` - Focal distance
- `/avatar/parameters/VL2_Aperture` - Aperture
- `/avatar/parameters/VL2_Exposure` - Exposure
- `/avatar/parameters/VL2_DepthOfField` - Depth of field

**Verification**:
1. VRChat Settings > Developer > Display advanced info
2. Check avatar parameters list

## Troubleshooting

### OSC Communication Not Established

**Symptom**: Status remains "Disconnected"

**Solutions**:
1. Verify VRChat OSC settings
   - Confirm "Enable OSC" checked
   - Confirm port number matches (default: 9001)
2. Check firewall settings
   - Confirm firewall not blocking communication
   - Check security software settings
3. Verify port not in use
   ```
   netstat -ano | findstr :9001
   ```
   - If port in use by other process, change to different port
4. Restart VRChat and VSA
   - Completely close both and restart

### Parameters Not Reflecting

**Symptom**: Controller changed but VRChat doesn't reflect

**Solutions**:
1. Check communication status
   - Verify controller screen status is "Connected"
   - If "Disconnected", see "OSC Communication Not Established"
2. Verify VirtualLens2 equipped
   - Confirm correct avatar equipped in VRChat
   - Confirm VirtualLens2 viewfinder displays
3. Check parameter names
   - Verify correct parameter names configured on avatar
4. Restart VSA
   - Reset OSC connection by completely restarting VSA

### Parameter Response Slow

**Symptom**: Parameter changes delayed in VRChat reflection

**Solutions**:
1. Check network connection
   - Verify internet connection stability
   - Check ping value (`ping 127.0.0.1`)
2. Check other app loads
   - Stop apps consuming network bandwidth
   - Check CPU usage not high
3. Check VRChat load
   - Many players in instance may reduce performance

### Parameter Reset Not Working

**Symptom**: Reset button clicked but value doesn't return

**Solutions**:
1. Check target parameter reset settings
   - Verify correct parameter selected
2. Check avatar settings
   - Verify VirtualLens2 reset value configured correctly on VRChat
3. Restart controller
   - Close controller screen and reopen

## Usage Examples

### Example 1: Portrait Shooting Preset

**Goal**: VRChat portrait-focused shooting

**Settings**:
- Focal Length: 85mm (portrait standard)
- Aperture: F2.0 (background bokeh)
- Exposure: 0 EV (standard brightness)
- Depth of Field: 80 (background bokeh)

**Steps**:
1. Set above values in controller
2. Save as "Portrait" preset
3. Click "Load" for portrait shooting

### Example 2: Landscape Shooting Preset

**Goal**: Capture world full-view

**Settings**:
- Focal Length: 35mm (wide-angle)
- Aperture: F8.0 (overall sharp)
- Exposure: 0.5 EV (slightly bright)
- Depth of Field: 20 (minimal bokeh)

**Steps**:
1. Set above values in controller
2. Save as "Landscape" preset
3. Click "Load" for landscape shooting

### Example 3: Night Shooting Preset

**Goal**: Sufficient brightness in dark world

**Settings**:
- Focal Length: 50mm (standard)
- Aperture: F1.4 (maximum brightness)
- Exposure: +3.0 EV (bright adjust)
- Depth of Field: 50 (moderate bokeh)

**Steps**:
1. Set above values in controller
2. Save as "Night Shooting" preset
3. Click "Load" for night shooting

## Related Documentation

- [VRChat Integration](vrchat-integration.md) - General VRChat integration info
- [Game Config Guide](game-config.md) - Detailed OSC settings
- [Keyboard Shortcuts](keyboard-shortcuts.md) - Shortcut list
