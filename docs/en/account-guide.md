# Account Management Guide

[🏠 Document Top](../index.md) | [⚖️ Terms of Service](./terms.md) | [🔒 Privacy Policy](./privacy.md)

---

The Account Management screen lets you check your VSA account status and configure account-linked features such as cloud save, share links, and X posting. This guide covers what is generally available and how rollout-gated features are described.

## Overview

Depending on your environment, Account Management may offer:

- **VSA Account**: Sign-in, plan, and connection status
- **Cloud Save (optional)**: Cloud backup for favorites and related data
- **Share Links (optional)**: Photo sharing via generated links
- **X Posting**: X connection and posting status

## About Account-Linked Features (Important)

Cloud save, share links, X posting, and related account-linked features are in **staged rollout**. Availability depends on **release status, plan, account status, and environment**.

If a menu or button does not appear in the app, that feature may not be available in your environment yet. Step-by-step instructions in this guide will be updated over time. For now, follow the **in-app UI** and these canonical documents:

- [Terms of Service](./terms.md)
- [Privacy Policy](./privacy.md)

Pricing, monthly limits, free tiers, and eligible features follow the website or in-app display. This documentation does not promise fixed overage pricing or uniform feature availability.

## Accessing Account Settings

Click **Account** in the sidebar to open the Account Management screen.

## VSA Account

A VSA account may be required for some optional features (cloud save, share links, X posting). Core local features—import, gallery, local favorites—do not require an account.

**Typical flow** (when shown in the app):

1. Open the Account screen
2. Follow on-screen prompts to sign in or connect services
3. Review plan, connection status, and any error messages

Sign-in and third-party connections may open a browser for OAuth. Your password is not stored in VSA; tokens are kept locally in encrypted form.

## Cloud Save and Favorites

Favorites work **locally** without cloud features. When cloud save is available in your environment, settings may appear on the Account screen or in favorites-related UI. Labels, toggles, and manual upload options vary by version and rollout—**follow the in-app UI**.

For local favorites usage, see the [Favorites Guide](favorites-guide.md).

## Share Links

Share links are released in stages. When available, you may create links from photo details or share menus. Scope, expiry, and pricing follow in-app display and the Terms of Service.

## X Posting

X posting is also subject to staged rollout. See the [X Posting Feature Guide](x-post-guide.md) for frames, presets, and posting workflow. Connection status may appear on the Account screen when enabled.

## Privacy and Security

### Where Data Is Stored

- **Local favorites and metadata**: On your PC (e.g. under `%APPDATA%\VSA\`)
- **Authentication tokens**: Encrypted locally; used only by VSA
- **Cloud-saved data**: Depends on the cloud service and VSA delivery model—see the [Privacy Policy](./privacy.md)

### External Communication

VSA account, cloud save, share links, X posting, update checks, and server status may involve network requests.

## Troubleshooting

### Sign-In or Connection Does Not Complete

**Symptom**: Browser auth finishes but the app does not return, or times out

**Steps**:

1. Allow pop-ups in your browser
2. Try another browser (Chrome recommended)
3. Check internet and firewall settings
4. Restart VSA and try again

### Cloud Save or Sharing Unavailable

**Symptom**: Menus missing or operations fail

**Possible causes**:

- Feature not rolled out to your environment yet
- Plan or account status does not meet requirements
- Temporary network or third-party outage

**Steps**:

1. Update to the latest app version
2. Check plan and connection status on the Account screen
3. Review the [Terms of Service](./terms.md) and in-app pricing/limit display
4. Keep important photos backed up locally

### Logout and Disconnect

Use logout or disconnect actions shown on the Account screen. After disconnecting, cloud save and share links may stop working. Local photos and favorites usually remain on disk.

## Tips

- **Local first**: Back up important photos locally regardless of cloud features
- **Trust the UI**: During rollout, in-app labels and enabled items are the source of truth
- **Read the terms**: Pricing and data handling are defined in Terms and Privacy on GitHub Pages

## Related Documentation

- [Favorites Guide](favorites-guide.md) - Local favorites and cloud save overview
- [X Posting Feature Guide](x-post-guide.md) - X posting (staged rollout)
- [Settings Guide](settings-guide.md) - App configuration
- [Troubleshooting Guide](troubleshooting.md) - Detailed problem solutions
