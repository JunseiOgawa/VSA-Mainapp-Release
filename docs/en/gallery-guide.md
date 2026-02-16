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

### Image Detail Sidebar Buttons

The following buttons are arranged at the top of the detail sidebar:

#### QR Code Read Button

A "Read QR Code" button displays above the preview image in the detail sidebar.

**Features**:
- Auto-detect QR codes in images
- Support for multiple QR codes (detects all in image)
- Detected QR codes display with overlay on image

**How to Use**:
1. Click photo to open detail sidebar
2. Click "Read QR Code" button
3. QR codes auto-detect
4. Box displays on detected QR code

**Processing Detected Results**:
- **URL**: Click "Open in Browser" to open in browser
- **Text**: Click "Copy to Clipboard" to copy content
- Multiple code detection displays all codes

#### X Post Button

"Post to X" button displays in detail sidebar (per photo).

**Features**:
- Open selected photo in X post modal
- Support simultaneous posting of multiple photos (maximum 4)

**How to Use**:
1. Click photo to open detail sidebar
2. Click "Post to X" button
3. X post modal displays
4. Configure text and presets then post

See [X Posting Feature Guide](x-post-guide.md) for details.

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

## User Search

Search for photos containing specific users from the user list displayed in the detail sidebar.

### Click Username to Search

**Steps**:
1. Click photo to open detail sidebar
2. Click username from "List of users in the instance" section
3. Auto-navigate to user search screen
4. Photos containing that user display in list

### AND Search with Multiple Users

Search multiple users simultaneously to display only photos with all users.

See [Person Search Guide](person-search-guide.md) for details.

## Bulk Selection Feature

Select multiple photos simultaneously to perform bulk favorite registration or trash move operations.

### Start Selection Mode

**Steps**:
1. Open Gallery tab
2. Click "Selection Mode" button in toolbar
3. Bulk selection mode enables
4. Toolbar display changes showing selection operation buttons

### Photo Selection and Deselection

**Selection Method**:
- Grid view: Click thumbnail to select
- Table view: Click row to select
- Click selected photos again to deselect

**Select All**:
1. Click "Select All" button in toolbar
2. All photos on screen select

**Deselect**:
1. Click "Deselect" button in toolbar
2. Clear all selections

### Selection Display

Selected photos show:

- Grid view: Checkmark on thumbnail
- Table view: Row highlight, checkbox on left
- Toolbar shows "n selected"

### Bulk Operations

With multiple photos selected, perform these operations:

#### Add Favorites in Bulk

**Steps**:
1. Select multiple photos
2. Click "Add to Favorites" button in toolbar
3. All selected photos add to favorites

#### Move to Trash in Bulk

**Steps**:
1. Select multiple photos
2. Click "Move to Trash" button in toolbar
3. Click "Move" in confirmation dialog
4. All selected photos move to trash

### X Post Mode (Photo Selection)

Special selection mode to select maximum 4 photos for X posting.

**Start**:
1. Click "X Post Mode" button in toolbar
2. Special selection mode enables

**Selection**:
1. Click X post photos (maximum 4)
2. Selection stops when reaching 4
3. Click selected photos to deselect

**Post**:
1. Click "Post to X" button
2. X post modal displays
3. Configure text and presets then post

See [X Posting Feature Guide](x-post-guide.md) for details.

### Exit Selection Mode

**Steps**:
1. Click "End Selection Mode" button in toolbar again
2. Or click "Cancel" button
3. Selection mode ends, all selections clear

## Trash Tab

In the trash tab, confirm deleted photos, restore them, or permanently delete.

### Access Trash Tab

**Steps**:
1. Check tab menu above Gallery
2. Three tabs display: "Gallery", "Favorites", "Trash"
3. Click "Trash"

### Trash View Features

Trash view supports same display formats as normal gallery (grid/table).

**Deleted Photo List**:
- All photos moved to trash display
- Confirm file name, deletion time, original world name, etc.
- Toggle grid or table view

### Restore Feature

Restore deleted photos to gallery.

**Steps**:
1. Open Trash tab
2. Click photo to restore
3. Click "Restore" button in detail sidebar
4. Click "Restore" in confirmation dialog
5. Photo returns to gallery

**Bulk Restore**:
1. Select multiple photos
2. Click "Restore" button in toolbar
3. All selected photos restore

### Permanently Delete Feature

Move photos to system trash, permanently delete from VSA.

**Steps**:
1. Select photo to delete from Trash tab
2. Click "Permanently Delete" button in detail sidebar
3. Click "Permanently Delete" in confirmation dialog
4. Photo moves to system trash

**Bulk Permanent Delete**:
1. Select multiple photos
2. Click "Permanently Delete" button in toolbar
3. Click "Delete" in confirmation dialog
4. All selected photos permanently delete

### Notes

**Restore Period**:
- No limit on storage period in trash
- Maintained until manually restored or permanently deleted

**About Permanent Deletion**:
- Moved to Windows trash, may be recoverable from Windows trash
- Once Windows trash empties, recovery impossible
- Recommend backup of important photos beforehand

**Clear Trash**:
- "Empty Trash" button permanently deletes all photos
- This action cannot be undone

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
