# Favorites Feature Guide

The Favorites feature allows you to mark important screenshots and manage them in a dedicated view. You can also automatically back up your favorite photos to Google Drive.

## Overview

With Favorites, you can:

- **Mark Important Photos**: Add star marks to special screenshots
- **Dedicated View**: Browse only your favorite photos in one place
- **Google Drive Integration**: Automatically backup favorites to cloud storage
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
- **Upload to Google Drive**: Send selected favorites to cloud
- **Remove from Favorites**: Bulk delete from favorites (keeps original files)

## Google Drive Integration

Automatically backup your favorite photos to Google Drive.

### Login Process (OAuth2 Authentication)

**Step 1: Access Account Settings**:
1. Click "Account" in the sidebar
2. Account management screen opens

**Step 2: Click "Login with Google Drive"**:
1. Click the login button
2. Web browser opens automatically
3. Google login page displays

**Step 3: Select Account**:
- Enter email/password if needed
- Select account if multiple exist
- Click "Use another account" for different account

**Step 4: Authorize VSA**:
1. Permission request screen appears
2. Review requested permissions
3. Click "Allow" or "Authorize" button
4. Permissions shown:
   - Google Drive read/write access
   - VSA folder creation and management
   - File upload capability

**Step 5: Return to VSA**:
1. Browser automatically returns to VSA
2. Account screen shows "Logged in"
3. Email address displayed
4. Logout button appears

**Step 6: Confirmation**:
- "Logged in" status visible
- Google account email shown
- Ready for sync operations

### Auto-Upload Configuration

Enable automatic cloud backup when marking photos as favorites.

**Enable Auto-Upload**:
1. Open Account settings
2. Find "Auto-Upload" toggle
3. Toggle ON
4. Setting saves automatically

**How It Works**:
1. Click favorite star on photo
2. Upload to Google Drive starts automatically
3. Takes seconds to minutes depending on file size
4. Status updates in UI

**Upload Destination**:
- Google Drive folder: `VSA` (auto-created)
- Your private folder
- Accessible from Google Drive web interface

**Note**: Requires internet connection. Upload pauses if connection drops.

### Manual Upload

Upload favorite photos immediately without waiting for auto-upload.

**Perform Manual Upload**:
1. Open Account settings
2. Click "Upload Now" button
3. Upload process begins
4. Progress bar shows status

**Progress Indicators**:
- Percentage complete (0-100%)
- Files processed count ("3 / 10")
- Current file information
- Time remaining (if available)

**Upload Duration**:
- 1-10 photos: Several seconds to 1 minute
- 11-50 photos: 1 to 5 minutes
- 50+ photos: 5 to 30+ minutes (network dependent)

**Network Requirements**:
- Internet connection required
- If connection drops, upload pauses
- Resume by clicking "Upload Now" again
- Previously uploaded files skipped automatically

### Checking Upload Progress

Real-time feedback during upload operations.

**Displayed Information**:
- Progress percentage: 0% to 100%
- File count: "Current / Total"
- Filename or thumbnail of current file
- Speed and time remaining (if available)

**Status Updates**:
- Real-time progress shown
- No need to refresh manually
- Completion notification appears when done

## Error Handling

### Upload Failures

**Symptom**: "Upload failed" error message

**Possible Causes**:

**No Internet Connection**:
- Check network connection
- Verify WiFi/Ethernet active
- Wait for connection restore
- Retry upload

**Google Drive Storage Full**:
- Check Google Drive storage usage
- Delete unnecessary files
- Upgrade to paid plan if needed
- Retry after freeing space

**Authentication Expired**:
- Click "Re-login" button in Account settings
- Re-authenticate with Google
- Retry upload

**File Size Issues**:
- Some files too large for upload
- Try uploading in smaller batches
- Check file sizes on disk

### Authentication Errors

**Symptom**: "Authentication failed" message

**Solutions**:

**Browser Popup Blocked**:
1. Check browser address bar
2. Look for popup block notification
3. Allow VSA popups
4. Try login again

**Security Software Blocking**:
1. Check firewall settings
2. Add VSA to firewall exceptions
3. Disable antivirus temporarily (carefully)
4. Try login again

**Google Account Security**:
1. Visit https://myaccount.google.com
2. Open Security section
3. Review "Less secure apps" setting
4. May need to allow VSA access

**Solution Steps**:
1. Clear browser cache (Ctrl + Shift + Delete)
2. Try different browser (Chrome recommended)
3. Restart VSA
4. Attempt login again

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

### Google Drive Upload Fails

**Symptom**: Upload stops with error midway

**Solutions**:

**Network Connection Lost**:
- Check internet connection
- WiFi may have disconnected
- Reconnect to network
- Retry upload (continues where left off)

**Google Drive Full**:
1. Open Google Drive in browser
2. Check storage usage
3. Delete old files
4. Upgrade storage if needed
5. Retry upload

**File Too Large**:
- Individual files exceeding limit
- Upload smaller batches
- Check file sizes locally

**Retry Steps**:
1. Check network/storage
2. Click "Upload Now" again
3. Previously uploaded files skip
4. Resume from where stopped

### Authentication Lost

**Symptom**: "Re-login required" message appears

**Causes**:
- Google security system revoked token
- Extended period without use
- Suspected unauthorized access
- Google password changed

**Solution**:
1. Click "Re-login" button
2. Complete Google authentication again
3. Resume uploads

## Privacy and Security

### Data Protection

**Authentication Tokens**:
- Stored locally, encrypted
- VSA application access only
- Never sent to servers
- Deleted on logout

**Photo Data**:
- Stored in your Google Drive only
- "VSA" folder is private by default
- Share folder if desired (your choice)
- Google Drive encryption applies

### Permissions

**VSA Requests**:
- Google Drive read/write permissions
- VSA folder access only
- File upload capability

**VSA Does NOT Request**:
- Email access
- Calendar access
- Contacts access
- Other Google services
- Account password (OAuth2 only)

## Tips

- **Regular Backups**: Backup favorites.db periodically
- **Drive Sharing**: Share VSA folder on Google Drive with friends
- **Offline Use**: Can mark favorites offline; uploading done later when online
- **Selective Backup**: Only favorites are uploaded, not entire library
- **Auto-Upload**: Enable for hands-free cloud backup workflow

## Related Documentation

- [Account Management Guide](account-guide.md) - Google Drive authentication details
- [Gallery Operation Guide](gallery-guide.md) - Photo browsing and selection
- [Troubleshooting Guide](troubleshooting.md) - Detailed problem solutions
