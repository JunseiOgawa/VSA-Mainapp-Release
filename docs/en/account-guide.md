# Account Management Guide

The Account Management screen allows you to connect to Google Drive and configure cloud backup settings for your favorite photos.

## Overview

Account Management features:

- **Google Drive Authentication**: Secure OAuth2 connection
- **Auto-Upload Configuration**: Automatic photo backup
- **Manual Upload**: Upload on-demand
- **Account Management**: View and manage connections

## Accessing Account Settings

Click "Account" in the sidebar to open the Account Management screen.

## Google Drive Account

### Login Process (OAuth2 Authentication Flow)

Google Drive integration uses secure OAuth2 authentication. Your password is never stored in VSA.

**Step 1: Click Login Button**:
1. Open Account Management screen
2. Find "Login with Google Drive" button
3. Click the button

**Step 2: Browser Opens Automatically**:
1. Default browser launches
2. Google login page appears
3. You're taken to Google's servers (VSA doesn't see password)

**Step 3: Enter Google Credentials**:
1. Enter your Google account email
2. Click Next
3. Enter your Google password
4. Click Next

**Step 4: Account Selection**:
If multiple Google accounts exist:
1. Account selection page shows
2. Choose the account to use
3. Or click "Use another account" for different account

**Step 5: Authorize VSA Access**:
1. Permission request screen appears
2. Review requested permissions:
   - Google Drive read/write access
   - VSA folder creation
   - File upload capability
3. Click "Allow" or "Authorize" button

**Note**: VSA only requests Google Drive access. Email, calendar, and other services are NOT requested.

**Step 6: Automatic Return to VSA**:
1. Browser automatically redirects to VSA
2. No manual copy/paste of codes needed
3. Login completes

**Step 7: Confirmation**:
On Account screen:
- "Logged in" status displays
- Google account email shown
- "Logout" button appears (instead of login button)

### Authentication Waiting State

During OAuth2 flow, VSA shows authentication status.

**What Happens**:
1. After clicking login button
2. Screen shows "Waiting for authentication..."
3. VSA waits for browser authentication completion

**Waiting Duration**:
- Maximum wait time: 5 minutes
- You can use VSA while waiting
- Continue working in other tabs

**During Waiting**:
- No need to rush browser authentication
- Take your time with Google login
- Multiple accounts can be selected
- Waiting status persists until completion

### Authentication Cancellation

Stop authentication if you change your mind.

**Method 1: Close Browser**:
1. Close Google authentication page
2. VSA automatically times out
3. Waiting state clears after timeout

**Method 2: Click Cancel**:
1. If "Cancel" button available
2. Click to stop waiting
3. Return to login state

### Logout Method

Disconnect from Google Drive.

**Steps**:
1. Open Account Management
2. Click "Logout" button
3. Confirmation dialog appears
4. Click "Logout" to confirm
5. Status shows "Not logged in"

**After Logout**:
- Upload functionality disabled
- Must re-login to upload
- Previously uploaded files remain in Google Drive
- To re-login: Click "Login with Google Drive" again

### Opening Google Drive

Access your backed-up photos directly from VSA.

**Steps**:
1. Click "Open Google Drive" button
2. Default browser opens
3. Google Drive web interface appears
4. "VSA" folder visible (contains backed-up favorites)

**What You Can Do**:
- View backed-up photos
- Share VSA folder with others
- Download photos to another computer
- Manage storage
- Organize files

## Upload Configuration

### Auto-Upload Setup

Enable automatic cloud backup of favorite photos.

**How to Enable**:
1. Ensure logged in to Google Drive
2. Find "Auto-Upload" toggle
3. Toggle to ON position
4. Setting saves automatically

**What Auto-Upload Does**:
1. When you mark photo as favorite (click star)
2. Upload to Google Drive starts automatically
3. Takes seconds to minutes based on file size
4. No additional actions needed

**Auto-Upload Behavior**:
- Only favorite-marked photos uploaded
- Upload happens in background
- Other VSA features continue working
- Internet connection required

**Disable Auto-Upload**:
1. Toggle "Auto-Upload" to OFF
2. Photos can be uploaded manually
3. No automatic uploads occur

### Manual Upload

Upload favorite photos immediately without waiting for auto-upload.

**How to Upload Now**:
1. Open Account Management
2. Click "Upload Now" button
3. Upload begins
4. Progress bar shows status

**Progress Indicators**:
- Percentage complete (0-100%)
- File count: "3 / 10" shows 3 of 10 files done
- Current filename or thumbnail
- Time remaining (if available)

**Upload Duration**:
- Depends on photo count and internet speed
- 1-10 photos: Usually seconds to 1 minute
- 11-50 photos: 1 to 5 minutes
- 50+ photos: 5 to 30+ minutes
- Network speed significantly impacts duration

**Network Requirements**:
- Internet connection must be active
- WiFi or wired connection both work
- If connection drops, upload pauses
- Resume by clicking "Upload Now" again
- Already-uploaded files skip automatically

**Upload Destination**:
- Google Drive folder: "VSA"
- Auto-created on first upload
- Private folder (only you can access)
- Can be shared with others using Google Drive sharing

## Privacy and Security

### Data Storage Locations

**Authentication Tokens**:
- Stored locally on your computer
- Encrypted for security
- VSA application only has access
- Never sent to external servers
- Deleted when you log out

**Photo Data**:
- Stored in YOUR Google Drive
- In "VSA" folder you control
- Not on VSA company servers
- Google Drive encryption applied
- You can delete anytime

### Access Permissions

**What VSA Requests**:
- Google Drive read access (to verify connection)
- Google Drive write access (to create/upload files)
- VSA folder creation
- File upload to VSA folder

**What VSA Does NOT Request**:
- Email access or sending
- Calendar access
- Contacts
- Photos from Google Photos
- Docs, Sheets, or other Google services
- Any ability to change your Google Account

**Password Security**:
- Your Google password NEVER enters VSA
- OAuth2 protocol handles authentication securely
- Password stays on Google's servers
- Only access token stored (encrypted)

### Token Expiration

Google may revoke access tokens for security.

**When Tokens Expire**:
- Extended period without use
- Google security policy changes
- Suspected unauthorized access
- You change Google account password
- You revoke app access in Google settings

**When This Happens**:
- "Re-login required" message appears
- Upload functions disabled
- "Re-login" button becomes available

**Re-authentication**:
1. Click "Re-login" button
2. Go through OAuth2 authentication again
3. Grant permissions again
4. Resume uploading

## VSA Account (Supabase Integration)

Note: VSA Account integration currently available in Developer Mode only. Public release planned for future versions.

This account type will enable premium VSA features including advanced cloud storage and synchronization across devices.

## Troubleshooting

### Authentication Times Out

**Symptom**: "Authentication timeout" message appears

**Causes**:

**Browser Popup Blocked**:
1. Check browser address bar
2. Look for popup block icon (usually right side)
3. Click icon to allow popups for this site
4. Add VSA to allowed sites
5. Try login again

**Security Software Blocking**:
1. Check Windows Firewall settings
2. Add VSA to firewall exceptions
3. Check antivirus software
4. Temporarily disable firewall/antivirus
5. Try login again

**Network Issues**:
1. Verify internet is working
2. Check WiFi connection
3. Try wired connection instead
4. Restart router if needed
5. Try login again

**Solutions**:
1. Clear browser cache: Ctrl + Shift + Delete
2. Try different browser (Chrome recommended)
3. Restart VSA
4. Ensure stable internet connection
5. Retry authentication

### Browser Doesn't Return to VSA

**Symptom**: After clicking "Authorize" in Google, browser doesn't return to VSA

**Possible Causes**:

**Browser Cache Corrupted**:
1. Clear browser cache: Ctrl + Shift + Delete
2. Select all items
3. Click "Clear browsing data"
4. Close browser
5. Try login again

**Different Browser**:
1. Close current browser
2. Open different browser (Chrome if possible)
3. Try login in new browser
4. Usually resolves the issue

**Firewall Blocking Return**:
1. Open Windows Security
2. Check Firewall & Network Protection
3. Verify VSA is allowed through firewall
4. Add VSA to firewall exceptions
5. Retry authentication

### Cannot Logout

**Symptom**: Logout button not working or no response

**Solutions**:

**Token Invalid**:
1. Restart VSA completely
2. Open Account screen
3. Try logout again

**Corrupted Settings**:
1. Close VSA
2. Delete: `%APPDATA%\VSA\account.json`
3. Restart VSA
4. Login status clears
5. Login again fresh if desired

### Authentication Errors

**Symptom**: "Google authentication failed" message

**Possible Causes**:

**Google Account Security Settings**:
1. Visit https://myaccount.google.com
2. Open "Security" section
3. Check "Less secure apps" setting
4. May need adjustment for VSA

**Browser Configuration**:
1. Clear browser cache
2. Disable browser extensions
3. Try different browser
4. Update browser to latest version

**VSA Settings**:
1. Restart VSA
2. Clear browser cache
3. Check internet connection
4. Retry authentication

**Solutions Step-by-Step**:
1. Clear browser cache (Ctrl + Shift + Delete)
2. Check all items
3. Click "Clear"
4. Restart VSA
5. Try authentication again
6. If still failing, try different browser

## Tips

- **Multiple Accounts**: Change Google accounts by logging out and logging in again
- **Share with Friends**: Right-click "VSA" folder in Google Drive to share with others
- **Regular Checks**: Periodically verify your uploaded files in Google Drive web interface
- **Offline Marking**: Can mark favorites offline; upload occurs when internet returns
- **Storage Management**: Check Google Drive storage quota to ensure space available

## Related Documentation

- [Favorites Guide](favorites-guide.md) - Favorites management details
- [Settings Guide](settings-guide.md) - App configuration
- [Troubleshooting Guide](troubleshooting.md) - Detailed problem solutions
