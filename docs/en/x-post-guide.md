# X Posting Feature Guide

The X posting feature allows you to post photos edited in VSA to X (formerly Twitter). You can select multiple photos (up to 4) and post them with camera info frames.

## X Posting Feature Overview

The X posting feature has the following characteristics:

- **Multiple Photo Support**: Select and post up to 4 photos simultaneously
- **Camera Info Frames**: Auto-generate frames with camera information overlaid
- **Preset Management**: Save and reuse frequently used posting settings
- **Template Settings**: Specify default text and hashtags

## How to Use X Posting

### Pre-Posting Setup

X account authentication is required before using the X posting feature.

**Initial Authentication Steps**:
1. Open Settings screen
2. Open "X Post" panel
3. Click authentication button in "X Account Authentication" section
4. Browser opens to X (Twitter) authentication page
5. Click "Authorize"
6. Authentication completes and returns to VSA

### Photo Selection

#### From Gallery

**Steps**:
1. Open Gallery tab
2. Click "X Post Mode" button in toolbar
3. Enter X post selection mode
4. Click photos to select (maximum 4)
5. Selection count displays on screen

**Notes**:
- X posts support maximum 4 photos simultaneously
- Cannot select more than 4
- Click selected photos to deselect

#### From Favorites

**Steps**:
1. Open Favorites tab
2. Click "X Post Mode" button in toolbar
3. Click photos to select (maximum 4)
4. After selection complete, click "Post to X" button

### Exit Selection Mode

**Steps**:
1. Click "X Post Mode" button again in toolbar
2. Or click "Cancel" button
3. Selection clears

## Camera Info Frame Feature

### Camera Info Frame Overview

The camera info frame feature auto-generates frames visually displaying camera information (camera type, parameters, etc.) overlay on photos.

**v0.4.3+ Support**:
- Generate multiple camera info frames simultaneously
- Auto-apply frames during X post

### Frame Customization

**Frame Setting Options**:

| Option | Description | Default |
|--------|-------------|---------|
| Frame Enable | Toggle frame generation on/off | ON |
| Frame Position | Frame placement (top, bottom, left, right) | Bottom |
| Frame BG Color | Frame background color | Black |
| Text Color | Camera info text color | White |
| Frame Width | Frame thickness (pixels) | 50 |

**Change Frame Settings**:
1. After photo selection, click "Frame Settings"
2. Adjust each item
3. Confirm in preview
4. Click "Apply"

### Aspect Ratio Feature

Customize photo aspect ratio for optimal posting.

**Supported Ratios**:
- 1:1 (square, social media standard)
- 16:9 (wide)
- 9:16 (portrait)
- 4:3 (standard)
- 3:4 (portrait standard)

**Specify Ratio**:
1. Select desired ratio from "Ratio Settings" section
2. Frame position auto-adjusts
3. Confirm in preview

## Preset Management

### What are Presets?

Save frequently used posting settings (frame settings, text templates, hashtags, etc.) as presets.

### Create Preset

**Steps**:
1. Open Settings screen
2. Open "X Post" panel
3. Click "New Preset" in "Presets" section
4. Enter preset name
5. Customize frame settings
6. Click "Save"

### Edit Preset

**Steps**:
1. Open Settings screen "X Post" panel
2. Click preset to edit from list
3. Modify items
4. Click "Save"

### Delete Preset

**Steps**:
1. Open Settings screen "X Post" panel
2. Click "Delete" button next to preset from list
3. Click "Delete" in confirmation dialog

### Apply Preset

Select preset to apply when opening X post modal.

**Steps**:
1. Select photos and open X post modal
2. Select preset from "Preset" dropdown
3. Frame settings and text template auto-apply

## Template Settings

### Text Template

Pre-set default text when posting to X.

**Template Variables**:

| Variable | Description |
|----------|-------------|
| `{world}` | World name |
| `{date}` | Capture time |
| `{camera}` | Camera type |
| `{user}` | Photographer name |

**Example**:
```
VRChat photo taken.
World: {world}
Time: {date}
Camera: {camera}
```

### Configure Template

**Steps**:
1. Open Settings screen
2. Open "X Post" panel
3. Edit template in "Text Template" section
4. Click "Save"

### Hashtag Settings

Pre-register frequently used hashtags.

**Steps**:
1. Open Settings screen "X Post" panel
2. Click "Add" in "Hashtags" section
3. Enter hashtag
4. Click "Save"

**Using Hashtags**:
- Registered hashtags display as suggestions when posting
- One-click add available

## Posting Steps (Step-by-Step)

### Basic Posting Flow

**Step 1: Select Photos**
1. Open Gallery or Favorites tab
2. Click "X Post Mode" button
3. Select photos to post (maximum 4)

**Step 2: Open X Post Modal**
1. Click "Post to X" button
2. X post modal displays

**Step 3: Verify Settings**
1. Select preset (frame settings)
2. Customize frame settings if needed
3. Enable camera info frame if needed
4. Confirm in preview

**Step 4: Enter Text**
1. Enter post text
2. Add hashtags if needed
3. Insert variables from template

**Step 5: Execute Post**
1. Click "Post" button
2. Post to X (Twitter) executes
3. Success message displays

### Advanced Posting with Custom Settings

**Combine Multiple Presets**:
1. Select preset in Step 3
2. Customize settings individually if needed
3. Confirm in preview before posting

**Custom Frame Settings**:
1. Customize individually in "Frame Settings" section
2. Click "Save as New Preset" for future reuse

## Troubleshooting

### X Authentication Fails

**Symptom**: Error displays during X account authentication

**Solutions**:
1. Confirm internet connection
   - Check firewall settings
   - Check proxy settings
2. Clear browser cache
   - Clear Chrome or Firefox cache
3. Retry authentication
   - Click "Re-authenticate" from Settings screen
4. Restart app
   - Fully close and restart

### Post Fails

**Symptom**: "Post failed" error displays

**Solutions**:
1. Confirm X authentication
   - Verify account auth is active
   - Verify auth token is valid
2. Check text content
   - Confirm text length within limit (280 chars max)
   - Check for prohibited characters
3. Verify photo size
   - Check X (Twitter) compatibility
   - Recommended: 1200x675px+, JPEG or PNG format
4. Check network connection
   - Verify internet stability
   - Test internet with other apps

### Frame Not Generated Correctly

**Symptom**: Camera info frame doesn't display

**Solutions**:
1. Confirm frame enabled
   - Check "Frame Enable" checkbox is ON
2. Verify frame settings
   - Check position and background color
   - Confirm preview displays correctly
3. Check photo info
   - Verify photo metadata is complete
   - Confirm camera info recorded correctly

### Template Variables Not Expanded

**Symptom**: Variables like `{world}` display as text

**Solutions**:
1. Check photo metadata
   - Verify photo details contain world name, etc.
2. Verify template format
   - Confirm variables in correct format `{variable}`
3. Switch to manual entry
   - Replace template variables with manual text

## Related Documentation

- [Gallery Guide](gallery-guide.md) - Photo selection and gallery operations
- [Settings Guide](settings-guide.md) - X Post settings panel details
- [VRChat Integration](vrchat-integration.md) - VRChat integration and metadata retrieval
