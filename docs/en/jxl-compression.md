# JXL Compression Guide

[🏠 Document Top](../index.md) | [⚖️ Terms of Service](./terms.md) | [🔒 Privacy Policy](./privacy.md)

---


VSA provides image compression functionality using the JPEG XL (JXL) format. This guide explains how to configure and use JXL compression.

## What is JPEG XL?

JPEG XL is a next-generation image format with the following features:

- **High Compression Ratio**: Significantly reduces file size compared to PNG
- **Lossless Compression**: Compress without quality degradation
- **Metadata Preservation**: VSA metadata is preserved after compression
- **Reversible Conversion**: Can be fully restored to original PNG

VRChat screenshots are typically saved as PNG, but JXL compression can reduce file size by over 50%.

## Accessing the Compression Screen

Click "JXL Compression" in the sidebar to open the compression screen.

The screen has two tabs:

- **Auto Compression**: Schedule-based automatic compression
- **Manual Compression**: Manual execution at any time

## Auto Compression

Automatically executes compression based on a schedule. VSA monitors in the background and automatically runs based on conditions.

### Schedule Settings

Fine-tune the auto compression execution schedule.

| Setting | Description |
|---------|-------------|
| **Interval** | Compression interval (days or months) |
| **Start Day** | Date to start compression from |
| **Next Run** | Next scheduled execution date/time (display only) |

**Example**:
```
Interval: 7 days
Start Day: Day 1
```
This schedule automatically runs compression every 7 days.

### Background Processing Settings

Configure detailed settings for auto compression background operation.

| Setting | Default | Description |
|---------|---------|-------------|
| **Auto Start** | Enabled | Automatically start at scheduled time |
| **Start Trigger** | 10 files | Start when unprocessed photos exceed this count |
| **Monitor Interval** | 5 minutes | Check folder at this interval |
| **Consider VRChat State** | Enabled | Pause compression while VRChat is running |

### Detailed Operation Mechanism

#### Schedule vs Trigger Relationship

Auto compression runs under two conditions:

**1. Scheduled Time (Periodic)**
```
Example: Auto compression starts every 1st of month at 00:00
```

**2. Unprocessed File Count Trigger (Event-driven)**
```
Example: Start when unprocessed photos reach 10+
```

When either condition is met, compression runs as a background process.

#### VRChat State Monitoring Details

When "Consider VRChat State" is enabled:

```
Scheduled Time
    ↓
VRChat Running?
    ├─ Yes → Pause compression (waiting)
    │        Resumes after VRChat closes
    └─ No → Start compression
```

This prevents performance degradation during gameplay while automatically resuming after game closes.

#### Monitor Interval Meaning

Monitor interval is how frequently VSA scans the folder to count unprocessed files.

```
5-minute interval example:
Time 0min → Scan (count files)
Time 5min → Scan
Time 10min → Scan (check trigger condition)
...
```

**Recommended Settings**:
- **Frequent VRChat use**: 5-10 minutes (quick detection)
- **Occasional use**: 30 minutes (resource saving)
- **Always-on setup**: 60 minutes (battery saving)

### Snooze Feature

When a compression reminder appears, select from snooze options:

| Option | Description |
|--------|-------------|
| **Remind in 1 hour** | Show reminder again after 1 hour |
| **Remind tomorrow** | Show at same time tomorrow |
| **Remind in 1 week** | Show after 7 days |
| **Postpone until next scheduled run** | Don't show until next scheduled execution |
| **Compress now** | Start compression immediately |

### Schedule Configuration Examples

#### Example 1: Monthly compression on 1st

```
Interval: 30 days
Start Day: 1st
Auto Start: Enabled
Start Trigger: 5 files
Monitor Interval: 10 minutes
Consider VRChat State: Enabled
```

**Operation Flow**:
```
1st Day 00:00 → Compression scheduled
↓
Unprocessed photos ≥ 5?
├─ Yes → Start compression (pause if VRChat running)
└─ No → Skip
↓
(Continue monitoring every 10 min, next scheduled run 31 days later)
```

#### Example 2: Weekly compression (aggressive)

```
Interval: 7 days
Start Day: 5th (assume Friday)
Auto Start: Enabled
Start Trigger: 3 files
Monitor Interval: 5 minutes
```

**Use case**:
- Regular execution every Friday
- Immediate processing if 3+ new photos exist
- Pause during gaming

#### Example 3: Auto-compress when photos accumulate (event-driven)

```
Interval: 0 (no scheduled runs)
Auto Start: Enabled
Start Trigger: 20 files
Monitor Interval: 5 minutes
```

**Use case**:
- No scheduled execution (event-driven only)
- Auto-start when 20+ photos accumulate
- Ideal for batch processing after sessions

### Operations During Compression

Most VSA features remain usable while compression runs:

**Available Operations**:
- ✅ Browse/search gallery
- ✅ View photo details
- ✅ Register/unregister favorites
- ✅ Play VRChat
- ✅ Change settings

**Limitations**:
- ⚠️ Manual compression not allowed concurrently (queued)
- ⚠️ Monitoring may delay during heavy folder operations
- ⚠️ Priority drops if system resources tight

**Performance Considerations**:
- Background processing runs at low priority
- Automatically pauses when VRChat active
- Minimal impact on other applications

### Stop/Pause Auto Compression

#### Disable Auto Execution

Uncheck "Auto Start" to:
- Disable scheduled execution
- Ignore file count triggers
- **Manual compression still available**

#### Stop Current Compression

To stop running compression mid-process:
1. Click "Stop" button in progress panel
2. Current file completes, then stops
3. Can continue at next scheduled time

### Troubleshooting

#### Auto compression not running

**Check**:
1. **Auto Start enabled?**: Verify "Auto Start" checkbox
2. **Schedule timing**: Check if "Next Run" is past or future
3. **Trigger files**: Count unprocessed files vs start trigger
4. **VRChat state**: If "Consider VRChat State" on, check if VRChat running
5. **Disk space**: Verify sufficient free space available

#### Compression started but stopped mid-way

**Fixes by cause**:
- **VRChat started** → Check "Consider VRChat State". Wait for automatic resume after VRChat closes or manually resume
- **Disk space insufficient** → Delete unnecessary files and retry
- **Network drive issues** → Try local drive

#### Compression slower than expected

- Decrease monitor interval (default 5 min → 1 min)
- Lower start trigger (default 10 → 5)
- Or use manual compression for immediate execution

## Manual Compression

Select any folder and execute compression.

### Steps

1. **Select Input Folder**: Folder containing PNG files to compress
2. **Select Output Folder**: Destination for JXL files
3. **Select Processing Mode**: Batch or background processing
4. **Start Compression**: Click the "Start Compression" button

### Processing Modes

**Batch Processing:**
- Processes all files at once
- UI is busy during processing
- Wait for completion

**Background Processing:**
- Processes sequentially at low priority
- Can perform other operations in parallel
- Takes longer to complete

### Checking Progress

During processing, the following information is displayed:

- Processed files / Total files
- Progress percentage
- Currently processing file name

## Extracting JXL Files

You can restore compressed JXL files back to original PNG.

1. Open the "JXL Extract" section in the manual compression tab
2. Select JXL file or folder to extract
3. Select output destination folder
4. Click "Start Extraction"

The extracted PNG files will have the original metadata restored.

## Compression Settings

You can change detailed JXL compression settings in the settings screen.

### Effort

| Value | Description |
|-------|-------------|
| 0-3 | Fast but lower compression ratio |
| 4-6 | Balanced |
| 7-9 | Slow but high compression ratio |

The default value is 7, which balances compression ratio and processing speed.

### Lossless Compression

VSA only supports lossless (reversible) compression. This means:

- Image quality is completely preserved
- Can be restored to original PNG
- Metadata is also preserved

## Compression Results

After compression completes, the following information is displayed:

- Number of files processed
- Total original size
- Total compressed size
- Reduction percentage

A `metadata.json` file is also generated in each folder, recording compression history.

## Important Notes

### Compression While VRChat is Running

Running compression while playing VRChat may cause the following issues:

- Game performance degradation
- Delay when taking photos
- Rare game crashes

It is recommended to exit VRChat before running compression whenever possible.

### Disk Space

During compression, both input and output files exist, so additional disk space is temporarily required.

Ensure sufficient free space (approximately 1.2x the input file size).

### Original File Handling

Original PNG files are not automatically deleted after compression. If you want to save disk space, manually delete them after confirming compression completed successfully.

## Troubleshooting

### Compression Not Progressing

1. **Check disk space**: Is there sufficient free space?
2. **Check file permissions**: Do you have read/write permissions?
3. **Check target files**: Do PNG files exist?

### Low Compression Ratio

Images that are already efficiently compressed or have simple content may have lower compression ratios.

### Metadata Lost

Saving in formats other than JXL may cause VSA metadata to be lost. Always use VSA's compression feature.
