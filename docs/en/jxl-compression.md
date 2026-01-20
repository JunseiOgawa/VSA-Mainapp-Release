# JXL Compression Guide

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

Automatically executes compression on a regular schedule.

### Schedule Settings

| Setting | Description |
|---------|-------------|
| Interval | Compression interval (monthly) |
| Start Day | Which day of the month to start |
| Next Run | Next scheduled execution date |

### Background Processing Settings

| Setting | Description |
|---------|-------------|
| Auto Start | Automatically start when conditions are met |
| Start Trigger | File count threshold for auto start |
| Monitor Interval | Folder monitoring interval (minutes) |
| Consider VRChat State | Pause while VRChat is running |

### VRChat Active Behavior

When "Consider VRChat State" is enabled, compression processing pauses while VRChat is active. This prevents performance degradation during gameplay.

### Snooze Feature

When a compression reminder appears, you can select from the following snooze options:

- Remind in 1 hour
- Remind tomorrow
- Remind in 1 week
- Postpone until next scheduled run

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
