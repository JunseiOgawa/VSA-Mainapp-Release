# VRChat Integration

VSA automatically extracts and saves metadata from photos taken in VRChat. This guide explains the metadata VSA saves and how it works.

## Metadata Overview

When you take a photo in VRChat, VSA automatically embeds the following information into the PNG image.

- World information
- User information
- Camera parameters
- Capture time

This information is saved in the PNG file's tEXt chunk and can be read by other tools without using VSA.

## World Information

Information about the world you were in when the photo was taken is recorded.

| Item | Description | Example |
|------|-------------|---------|
| World Name | VRChat world name | "Japan Shrine" |
| World ID | VRChat internal ID | "wrld_xxx..." |
| Instance ID | Instance identifier | "12345~hidden(usr_xxx)" |
| Instance Type | Access permissions | Public, Friends+, Friends, Invite+, InviteOnly |

## User Information

User information at the time of capture is recorded.

| Item | Description |
|------|-------------|
| Photographer Name | Username of the person who took the photo |
| Photographer ID | VRChat user ID (usr_xxx format) |
| Participants List | All usernames in the instance |

The participants list includes the usernames of everyone who was in the instance at the time of capture.

## Camera Parameters

The camera settings used in VRChat are recorded. VSA supports the following cameras.

### VirtualLens2

Parameters recorded when using VirtualLens2:

| Parameter | Description |
|-----------|-------------|
| Aperture | F-stop value |
| Focal Length | Focal length |
| Exposure | Exposure compensation |
| Zoom | Zoom level |
| Brightness | Brightness |
| Contrast | Contrast |
| Saturation | Saturation |
| Sharpness | Sharpness |
| FOV | Field of view |
| Focus Distance | Focus distance |

### Integral

Parameters recorded when using Integral:

| Parameter | Description |
|-----------|-------------|
| Aperture | F-stop value |
| Focal Length | Focal length |
| Exposure | Exposure compensation |
| Shutter Speed | Shutter speed |
| Bokeh Shape | Bokeh shape |
| Resolution Scale | Resolution scale |
| Render Distance | Render distance |

### Normal Camera

When using the standard VRChat camera, camera parameters are not recorded.

## How OSC Communication Works

VSA communicates with VRChat using the OSC (Open Sound Control) protocol to obtain camera settings.

### How It Works

1. Change camera settings in VRChat
2. Camera sends OSC message
3. VSA receives OSC message and saves to memory
4. When photo is taken, saved camera settings are embedded in the image

### Required Settings

To enable OSC communication:

1. Enable OSC in VRChat settings
2. Enable OSC output on the supported camera (VirtualLens2 or Integral)

## VRChat Log Analysis

World and user information is extracted from VRChat log files.

### Log File Location

```
%LOCALAPPDATA%Low\VRChat\VRChat\
```

Usually located at `C:\Users\[Username]\AppData\LocalLow\VRChat\VRChat\`.

### Extracted Information

- World entry/exit
- User join/leave
- Instance information

## Checking Supported Cameras

You can check which camera was used for each photo in the gallery detail view.

- VirtualLens2: Displayed as "VL2" or "VirtualLens2"
- Integral: Displayed as "Integral"
- Normal camera: Displayed as "Normal Camera"

Camera parameters are displayed in accordion format and can be expanded by clicking.

## Troubleshooting

### Metadata Not Being Recorded

1. **Check if OSC is enabled in VRChat**
   - VRChat Settings > OSC > Enable

2. **Check if using a supported camera**
   - VirtualLens2 or Integral is required

3. **Check if VSA is running in the background**
   - VSA must be running while VRChat is active

### Missing World/User Information

1. **Check VRChat log files**
   - Verify log files are being output correctly

2. **Check capture timing**
   - Photos taken immediately after entering a world may miss log data

