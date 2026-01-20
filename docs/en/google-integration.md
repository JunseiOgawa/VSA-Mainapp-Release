# Google Integration

VSA can connect with your Google account to enable backup and synchronization to Google Photos and Drive. This guide explains how to set up Google login and use the backup features.

## Feature Overview

By enabling Google integration, the following features become available:

- Sign in with Google account
- Automatic image upload to Google Photos
- Backup synchronization to Google Drive
- Image sharing across multiple devices

## Google Login

### How to Login

1. Open the Settings screen
2. Select "Google Integration" section
3. Click "Sign in with Google" button
4. Select your Google account in the browser
5. Grant access to VSA

### Required Permissions

VSA requests access to the following Google services:

| Permission | Purpose |
|------------|---------|
| Google Photos (read/write) | Upload and manage images |
| Google Drive (read/write) | Store backup files |
| User info (basic) | Account identification |

### Logout

You can disconnect your Google account at any time by selecting "Logout" in the "Google Integration" section of the Settings screen.

## Google Photos Integration

### Automatic Upload

Images imported to VSA can be automatically uploaded to Google Photos.

#### Configuration Options

| Option | Description |
|--------|-------------|
| Auto Upload | Automatically upload new images |
| Upload Quality | Original quality / High quality (storage saver) |
| Album Settings | Specify destination album |
| Preserve Metadata | Upload with VSA metadata preserved |

#### Album Management

- Automatically create albums by capture date
- Organize albums by world
- Custom album assignment

### Manual Upload

You can also upload selected images individually from the gallery.

1. Select images in the gallery
2. Right-click and select "Upload to Google Photos"
3. Choose the destination album
4. Execute upload

## Google Drive Integration

### Backup Synchronization

Use Google Drive to backup VSA's database and settings to the cloud.

#### Backup Contents

| Item | Description |
|------|-------------|
| Image Files | Original images and thumbnails |
| Metadata | Extracted VRChat information |
| Database | Image index information |
| Settings | Application configuration |

#### Sync Options

| Option | Description |
|--------|-------------|
| Auto Sync | Automatically backup on changes |
| Sync Interval | Periodic backup interval (1 hour/1 day/1 week) |
| Sync Folder | Destination folder on Drive |
| Bandwidth Limit | Upload speed limitation |

### Restore

When using a new device or reinstalling VSA, you can restore data from Google Drive.

1. Launch VSA
2. Sign in with Google account
3. Select "Restore from Backup"
4. Choose the backup to restore
5. Execute restore

## Checking Sync Status

### Status Indicator

You can check the Google sync status in VSA's status bar.

| Icon | Status |
|------|--------|
| Cloud (check) | Sync complete |
| Cloud (arrow) | Syncing |
| Cloud (x) | Sync error |
| Cloud (offline) | Offline |

### Sync Log

You can view detailed sync logs from the Settings screen.

- Upload/download history
- Error details
- Bandwidth usage

## Privacy and Security

### Data Handling

- Images and metadata are stored only in your Google account
- Data does not pass through VSA servers
- Secure authentication via OAuth 2.0

### Managing Access

You can review or revoke VSA's access permissions at any time from your Google account settings.

1. Go to [Google Account Settings](https://myaccount.google.com/)
2. Select "Security" → "Third-party apps & services"
3. Select VSA to manage access permissions

## Troubleshooting

### Cannot Login

1. **Check internet connection**
   - Verify your network connection is working

2. **Check browser settings**
   - Disable popup blockers
   - Ensure cookies are enabled

3. **Check Google account status**
   - Complete 2-factor authentication if enabled

### Sync Not Completing

1. **Check storage capacity**
   - Verify available space in Google Drive/Photos

2. **Check file size**
   - Large files may take longer to upload

3. **Check network status**
   - Retry with a stable network connection

### Upload Failing

1. **Check file format**
   - Supported image formats: PNG, JPEG, WEBP, JXL

2. **Check permissions**
   - Verify VSA has the required permissions

3. **Re-authenticate**
   - Log out and log in again

