# Gallery Guide

The gallery screen allows you to view imported photos in a list format, check detailed information, and perform operations such as adding favorites.

## Display Modes

The gallery has two display modes.

### Grid View

Displays photos in a thumbnail grid format.

- Easy to visually check images
- Adjustable thumbnail size (50px-300px)
- Date-based grouping (when thumbnail size is small)

### Table View

Displays photos in a list format.

- View file name, capture time, world name at a glance
- Click column headers to sort
- Resizable columns

Switch display modes using the toolbar button.

## Sorting

You can sort by the following items.

| Sort Item | Description |
|-----------|-------------|
| Created Date | File creation date (default) |
| World Name | VRChat world name |
| File Name | Alphabetical order of file names |
| File Size | File size |
| Capture Time | Photo capture time |
| Photographer | User who took the photo |

How to sort:

1. Select an item from the sort dropdown in the toolbar
2. Toggle ascending/descending with the arrow button
3. In table view, you can also click column headers to sort

## Zoom Controls

You can change the thumbnail size in grid view.

### Keyboard Shortcuts

| Action | Shortcut |
|--------|----------|
| Zoom In | `Ctrl` + `=` |
| Zoom Out | `Ctrl` + `-` |

### Mouse Controls

- `Ctrl` + Mouse Wheel: Zoom centered on mouse position

### Slider

You can also adjust the size using the slider in the toolbar.

## Image Detail Sidebar

Click a photo to display a sidebar on the right showing detailed information.

### Displayed Information

**Basic Info:**
- Preview image (click to open in default app)
- File path
- File hash

**VRChat Info:**
- World name (copyable)
- Photographer name
- Capture time
- List of users in the instance

**Camera Info:**
- Camera type (VirtualLens2/Integral/Normal Camera)
- VirtualLens2 parameters (Aperture, FocalLength, Exposure, etc.)
- Integral parameters (ShutterSpeed, BokehShape, etc.)

Camera information is displayed in an accordion format and can be expanded by clicking.

## Favorites

You can mark photos as favorites.

### How to Use

- Click the star icon on the thumbnail
- Click the star button in the detail sidebar
- Click the star icon in table view

Favorite status is saved to the database and persists after restarting the app.

## Deleting Images

You can move unwanted images to the trash.

1. Click an image to open the detail sidebar
2. Click the trash icon
3. Select "Delete" in the confirmation dialog

Deleted images are moved to the system trash (not permanently deleted).

## Keyboard Shortcuts

| Action | Shortcut |
|--------|----------|
| Zoom In | `Ctrl` + `=` |
| Zoom Out | `Ctrl` + `-` |
| Fullscreen | `F11` |

## Toolbar Operations

The toolbar is displayed at the top of the screen.

- Move mouse to the top of the screen (within 100px) to show
- Expand/collapse button to pin display
- Reload button to refresh the image list

## Performance

The gallery performs smoothly even with large numbers of images thanks to virtualization technology.

- Only renders images visible on screen
- Lazy loading of thumbnails
- Page caching for fast redisplay

## Current Limitations

The following features are currently under development.

- Filter function (filtering by date, world, user, etc.)
- Search function (keyword search)

These features will be added in future updates.
