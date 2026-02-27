# FAQ/Troubleshooting

This section covers frequently asked questions and solutions for common problems.

> **Note (Integral support status)**
> Integral support is currently in progress. Some Integral camera parameter values may not be recorded or displayed correctly.

## Frequently Asked Questions

### Images Not Displaying

**Symptom:** Images don't appear in the gallery, or thumbnails won't load

**Solutions:**

1. **Check if folders are properly imported**
   - Go to "Import" in the sidebar and verify folders are added
   - Confirm folder status shows "Enabled"

2. **Check if image files are PNG format**
   - VSA only supports PNG files
   - JPG and other formats are automatically skipped

3. **Check if files are corrupted**
   - Verify you can open the images in an image viewer

4. **Try reloading**
   - Click the reload button (refresh icon) on the gallery screen

---

### Metadata Not Being Captured

**Symptom:** World name or username shows as "Unknown"

**Solutions:**

1. **Confirm VRChat was running**
   - Metadata is captured in real-time from VRChat
   - If photos were taken without VRChat running, metadata won't be recorded

2. **Confirm VSA was running in background**
   - VSA must be running at the time of capture

3. **Check OSC settings**
   - Verify OSC is enabled in VRChat settings
   - Verify OSC output is enabled on supported cameras (VirtualLens2/Integral)

4. **Check log files**
   - Verify VRChat log files are being output correctly
   - Location: `%LOCALAPPDATA%Low\VRChat\VRChat\`

---

### JXL Compression Not Progressing

**Symptom:** Compression process doesn't start or stops midway

**Solutions:**

1. **Check disk space**
   - Compression requires approximately 1.2x the input file size in free space

2. **Check file permissions**
   - Read permission for input folder
   - Write permission for output folder

3. **Check if VRChat is running**
   - If "Consider VRChat State" is enabled, compression pauses while VRChat is running

4. **Check process in Task Manager**
   - Verify VSA process is responding
   - If not responding, restart the application

---

### Gallery is Slow

**Symptom:** Scrolling is choppy, loading is slow

**Solutions:**

1. **Adjust thumbnail size**
   - Larger thumbnails require more processing power
   - Try zooming out to display smaller thumbnails

2. **Close other applications**
   - High memory usage can degrade performance

3. **Check sort mode**
   - Sorting loads all data, which may cause slowdowns

4. **Optimize database**
   - The database may become fragmented after long-term use
   - Run database optimization from the settings screen

---

### App Won't Start

**Symptom:** VSA doesn't start when clicked

**Solutions:**

1. **Close existing processes**
   - Check if VSA process remains in Task Manager
   - If so, end it and restart

2. **Run as administrator**
   - Right-click > "Run as administrator"

3. **Reset settings files**
   - Settings files may be corrupted
   - Delete the `%APPDATA%\vsa-mainapp` folder and restart

---

## Troubleshooting

### Finding VRChat Logs

VRChat log files are located at:

```
%LOCALAPPDATA%Low\VRChat\VRChat\
```

You can access this by entering the path in Windows Explorer's address bar.

Log file names follow the format `output_log_date_time.txt`.

### Verifying OSC Communication

To check if OSC communication is working correctly:

1. Open VRChat settings
2. Navigate to the OSC section
3. Verify "OSC" is enabled
4. If needed, enable "OSC Debug Console" to monitor communication

### Rebuilding the Database

If there are database issues, rebuilding may be necessary.

**Warning:** This operation will lose favorites and other saved information.

1. Close VSA
2. Delete the `%APPDATA%\vsa-mainapp\database` folder
3. Restart VSA
4. Re-import folders

### Checking Log Files

VSA log files are located at:

```
%APPDATA%\vsa-mainapp\logs\
```

When problems occur, error information is recorded in these log files.

## Contact

If the above methods don't solve your issue, please contact us through the following:

1. **GitHub Issues**
   - Bug reports and feature requests are accepted on GitHub Issues
   - Attaching log files helps identify problems more easily

2. **Attaching Log Files**
   - When contacting us, please provide the following information:
     - Detailed description of the problem
     - Steps to reproduce
     - VSA version
     - Windows version
     - Related log files

## Known Issues

The following are known issues we are aware of. Fixes are planned for future updates.

- Filter function not implemented
- Search function not implemented
- Metadata may not be correctly captured in some VRChat worlds
