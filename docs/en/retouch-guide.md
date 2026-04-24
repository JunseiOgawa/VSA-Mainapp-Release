# Retouch Feature Guide

The retouch feature lets you edit photos directly within the application. You can adjust brightness, contrast, color temperature, tone curves, and more.

## Opening the Retouch Editor

Select a photo in the gallery and click the "Retouch" button to open the retouch editor.

## Screen Layout

The retouch editor consists of three main areas:

### Left Area (Main Editing)

- **Zoom Controls** — Adjust the display scale of the photo
- **Preview Canvas** — View real-time preview of edits
- **Filmstrip** — Quick access to recent photos for fast switching

### Right Panel (Parameter Adjustment)

Adjust editing parameters using sliders or numeric input.

## Editing Parameters

### Basic Parameters

| Parameter | Description | Range |
|-----------|-------------|-------|
| **Brightness** | Adjust overall brightness of the photo | -100% ～ +100% |
| **Contrast** | Adjust the difference between light and dark areas | -100% ～ +100% |
| **Saturation** | Adjust color vividness | -100% ～ +100% |
| **Color Temperature** | Adjust warm/cool color tone | 2000K ～ 10000K |
| **Highlights** | Adjust bright areas (whites) | -100% ～ +100% |
| **Shadows** | Adjust dark areas (blacks) | -100% ～ +100% |

### How to Adjust Parameters

#### Using Sliders

Drag the slider next to each parameter to adjust the value.

#### Direct Numeric Input

Click the numeric field to enter values directly or as percentages.

- `50` or `50%` for +50%
- `-30` or `-30%` for -30%

#### Reset to Default

Click the reset button (↻ icon) at the end of each parameter row to restore the default value.

## Tone Curve Editor

Use the tone curve editor for more detailed color correction.

### Tone Curve Basics

The tone curve shows the relationship between input values (horizontal axis) and output values (vertical axis).

- **RGB** — Adjust all color channels simultaneously
- **R (Red)** — Adjust red channel only
- **G (Green)** — Adjust green channel only
- **B (Blue)** — Adjust blue channel only

### Operating the Tone Curve

1. Open the "Tone Curve" section in the left panel
2. Click a channel button (RGB/R/G/B) to select the channel to adjust
3. Click anywhere on the curve to add a point
4. Drag the point to adjust the curve
5. Delete unnecessary points using the delete icon

### Tone Curve Adjustment Examples

**Lift Shadows** — Drag the lower-left portion of the curve upward to brighten dark areas

**Control Highlights** — Drag the upper-right portion of the curve downward to manage bright area exposure

**Enhance Contrast** — Create an S-curve to emphasize the difference between shadows and highlights

## Zoom Operations

### Zoom Buttons

Use the zoom controls above the preview canvas:

- **Zoom In (+)** — Enlarge details
- **Zoom Out (-)** — Display smaller
- **Fit Window** — Fit entire photo to screen (default)

### Keyboard Shortcuts

| Action | Shortcut |
|--------|----------|
| Zoom In | `Ctrl` + `=` |
| Zoom Out | `Ctrl` + `-` |
| Fit Window | `Ctrl` + `0` |

## Filmstrip

The filmstrip at the bottom displays up to 100 recent photos.

### Filmstrip Operations

- **Photo Selection** — Click a photo in the filmstrip to switch instantly
- **Scroll** — Scroll left/right using mouse wheel or scrollbar

## Toolbar Buttons

### Edit Operations

| Button | Function |
|--------|----------|
| **Undo** | Cancel the last operation (`Ctrl` + `Z`) |
| **Redo** | Reapply the last undone operation (`Ctrl` + `Shift` + `Z`) |
| **Reset** | Reset all parameters to default values |

### Apply & Save

| Button | Function |
|--------|----------|
| **Apply** | Apply edits to photo and save |
| **Cancel** | Discard edits and exit retouch |
| **Export** | Export edits as a new file |

### Export Feature

Click the **Export** button to save with these options:

- **File Format** — Select from PNG, JPEG, and other supported formats
- **Filename** — Specify save location and new filename
- **Quality** — Adjust compression quality for JPEG saving

## Common Operations

### Brighten a Dark Photo

1. Move the **Brightness** slider to the right to brighten overall
2. Adjust **Highlights** as needed to prevent blown-out whites

### Warm Up Photo Color

1. Move the **Color Temperature** slider to the right (higher = warmer)
2. Preview the result

### Increase Color Vividness

Move the **Saturation** slider to the right for more vivid colors

### Balance Shadows and Light

1. Adjust **Shadows** to fine-tune dark areas
2. Adjust **Highlights** to fine-tune bright areas
3. Verify overall balance and make fine adjustments

## Notes

- **Auto-save** — Edits are NOT automatically saved when closing the editor. You must press **Apply** to save
- **Original File Impact** — Pressing **Apply** overwrites the original photo. For important photos, use **Export** to save as a new file
- **Large File Processing** — High-resolution photos may take time to process
- **Memory Usage** — Retouching multiple photos simultaneously consumes memory

## Keyboard Shortcuts Summary

| Action | Shortcut |
|--------|----------|
| Undo | `Ctrl` + `Z` |
| Redo | `Ctrl` + `Shift` + `Z` |
| Zoom In | `Ctrl` + `=` |
| Zoom Out | `Ctrl` + `-` |
| Fit Window | `Ctrl` + `0` |
