# Favorites Feature Guide

[🏠 Document Top](../index.md) | [⚖️ Terms of Service](./terms.md) | [🔒 Privacy Policy](./privacy.md)

---


The Favorites feature lets you mark important screenshots and manage them in a dedicated view on your PC. When cloud save is available in your environment, you may also back up favorites to the cloud. This guide focuses on local favorites operations.

## Overview

With Favorites, you can:

- **Mark Important Photos**: Add star marks to special screenshots
- **Dedicated View**: Browse only your favorite photos in one place
- **Cloud Save (optional)**: Cloud backup for favorites in rollout-enabled environments
- **Efficient Management**: Organize and access your best moments quickly

## Adding Favorites

### Method 1: Gallery Grid View

Mark photos as favorite directly from the gallery thumbnail display.

**Steps**:
1. View the gallery grid
2. Locate the star icon (★) on the thumbnail's top-right corner
3. Click the star icon
4. Star fills in, indicating photo is now a favorite

### Method 2: Photo Detail Sidebar

Mark favorites from the detailed photo information panel.

**Steps**:
1. Click a photo in the gallery
2. Photo detail sidebar opens on the right
3. Click the star (★) button at the top of the sidebar
4. Star fills in to confirm favorite status

### Method 3: Table View

Mark favorites from the list/table display.

**Steps**:
1. Switch to Table view
2. Locate the star (★) column
3. Click the star cell for desired photo
4. Favorite status updates immediately

**Sync Note**: Favorite status syncs between Grid and Table views. Mark as favorite in either view and it appears in both.

## Favorites View

### Accessing Favorites

**Steps**:
1. Click "Favorites" in the sidebar
2. Dedicated Favorites view opens
3. All marked favorite photos display

### Display Format

**Grid Display**:
- Thumbnails organized in grid layout
- Responsive columns based on window size
- Same zoom controls as gallery view

**Displayed Information**:
- Thumbnail image
- Metadata on hover (world name, date, etc.)
- Capture timestamp
- World information

### Sorting Options

Arrange your favorite photos in different orders:

**Sort by Addition Date**:
- Newest favorites first
- Shows most recently marked photos at top

**Sort by Capture Date**:
- Photos ordered by screenshot time
- Chronological organization

**Sort by File Size**:
- Smallest or largest files first
- Useful for storage management

**How to Sort**:
1. Open Favorites view
2. Click sort dropdown menu
3. Select desired sort order
4. List updates immediately

### Selection and Bulk Operations

Select multiple photos for batch actions.

**Selection Methods**:
1. Click photo (single select)
2. Ctrl+Click for multiple select
3. Checkbox at photo corner (if available)

**Bulk Operations**:
- **Save to Cloud** (when shown): Send selected favorites to cloud storage
- **Remove from Favorites**: Bulk delete from favorites (keeps original files)

## Cloud Save (Optional, Staged Rollout)

Cloud backup for favorites is in **staged rollout**. Availability depends on release status, plan, account status, and environment.

When enabled, auto-save or manual save settings may appear on the Account screen or in favorites-related UI. Labels and controls vary by version—**follow the in-app UI**.

Detailed steps in this guide will be updated over time. For now, see:

- [Account Management Guide](account-guide.md)
- [Terms of Service](./terms.md) / [Privacy Policy](./privacy.md)

**Local favorites work without cloud features.** Back up `%APPDATA%\VSA\favorites.db` locally for important data.

### When Cloud Save Fails or Is Unavailable

- Check internet and account connection status
- Review plan, monthly limits, and free tiers in the app
- Allow browser pop-ups and try signing in again on auth errors
- See [Troubleshooting](troubleshooting.md) if problems persist

## Data Management

### Favorites Database

Favorite information stored locally in SQLite database.

**Database Location**:
```
%APPDATA%\VSA\favorites.db
```

**Characteristics**:
- Encrypted and secured
- Persistent across restarts
- Auto-backed up with VSA data
- Private to your computer

### Creating Backups

Backup your favorite photos metadata.

**Backup Steps**:
1. Close VSA completely
2. Navigate to: `%APPDATA%\VSA\`
3. Copy `favorites.db` file
4. Save copy to safe location
   - USB drive
   - Cloud storage
   - External hard drive

### Restoring from Backup

Restore favorites from previous backup.

**Restore Steps**:
1. Close VSA
2. Obtain your backup `favorites.db` file
3. Copy it to `%APPDATA%\VSA\`
4. Overwrite current file (confirm replacement)
5. Restart VSA
6. Favorites restored

## Troubleshooting

### Favorites Not Saving

**Symptom**: Marked photos revert to non-favorite after restart

**Possible Causes**:

**Disk Space Issues**:
- Check available disk space
- Ensure at least 1GB free
- Clear unnecessary files
- Retry marking favorites

**File Permission Problems**:
1. Right-click `%APPDATA%\VSA\` folder
2. Open Properties
3. Check Security tab
4. Verify Write permission enabled
5. Apply if needed

**Database Corruption**:
1. Enable Developer Mode
2. Open Developer menu
3. Rebuild database
4. Restart VSA

### Cloud Save Fails or Is Unavailable

**Symptom**: No cloud menu, or save stops with an error

**Solutions**:

**Check Rollout and Plan**:
- Verify plan and connection on the Account screen
- Menus may be hidden if the feature is not offered in your environment

**Network Connection**:
- Verify internet connectivity
- Ensure VSA is allowed through the firewall

**Re-sign-in**:
1. Log out or disconnect on the Account screen
2. Sign in again following on-screen prompts
3. Try manual save in smaller batches if offered

**Keep Local Backups**:
- Copy `favorites.db` regularly; do not rely on cloud save alone

## Privacy and Security

### Data Protection

**Authentication Tokens** (when account linking is used):
- Stored locally, encrypted
- VSA application access only
- Deleted on logout when applicable

**Favorite Data**:
- Stored locally in `favorites.db` on your PC
- Cloud copies, when enabled, follow the Privacy Policy and in-app display

## Tips

- **Regular Backups**: Backup favorites.db periodically
- **Share links**: Available in rollout-enabled environments ([Account Guide](account-guide.md))
- **Offline use**: Mark favorites offline; cloud save runs when connectivity returns
- **Selective backup**: Only favorites may be eligible for cloud save—not the entire library

## Related Documentation

- [Account Management Guide](account-guide.md) - VSA account and cloud save overview
- [Gallery Operation Guide](gallery-guide.md) - Photo browsing and selection
- [Troubleshooting Guide](troubleshooting.md) - Detailed problem solutions
