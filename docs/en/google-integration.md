# Cloud and Account Integration (formerly Google Integration)

[🏠 Document Top](../index.md) | [⚖️ Terms of Service](./terms.md) | [🔒 Privacy Policy](./privacy.md)

---

VSA provides and expands account-linked features such as cloud save, share links, and X posting. Some environments may use third-party authentication (e.g. Google OAuth, X OAuth), but **this guide does not assume Google Drive or Google Photos are generally available to all users**.

## Feature Overview (Staged Rollout)

The following are subject to **staged rollout**. Availability depends on release status, plan, account status, and environment.

- Sign-in with a VSA account
- Cloud save (optional backup for favorites and related data)
- Share link generation
- X posting integration
- Cross-device sync (when offered)

If the relevant UI does not appear in the app, the feature may not be enabled for your environment yet.

## Guide Update Status

Earlier versions documented Google Photos and Google Drive steps in detail. Because public scope and implementation are evolving, **specific step-by-step instructions are being revised**.

For now, rely on:

1. **In-app UI** (menus, buttons, error messages)
2. **Canonical Terms and Privacy** on GitHub Pages
   - [Terms of Service](./terms.md)
   - [Privacy Policy](./privacy.md)
3. Related guides
   - [Account Management Guide](account-guide.md)
   - [Favorites Guide](favorites-guide.md)
   - [X Posting Feature Guide](x-post-guide.md)

## Typical Authentication Flow (When Shown)

When external account linking is enabled:

1. Open Settings or the Account screen
2. Follow prompts for the VSA account or linked service
3. Complete authentication in the browser and return to the app
4. Verify connection status and plan

Requested permissions vary by service and rollout stage. See the auth screen and [Privacy Policy](./privacy.md).

## Privacy and Security

- Local data (favorites, settings) stays on your PC
- Cloud save and sharing are described in the Privacy Policy
- OAuth flows request least-privilege access where possible
- Disconnect via the Account screen or the third-party service settings when available

## Troubleshooting (General)

### Linking Menu Not Visible

- Your environment may not be in the current rollout
- Update the app and check account status

### Authentication Does Not Complete

1. Verify internet connectivity
2. Disable popup blockers
3. Try another browser
4. Restart VSA

### Sync or Upload Fails

1. Check plan, monthly limits, and free tiers in the app
2. Use a stable network
3. Keep local backups of important data
4. See [Troubleshooting](troubleshooting.md) and [FAQ](faq.md) if issues persist

## Related Documentation

- [Account Management Guide](account-guide.md)
- [Terms of Service](./terms.md)
- [Privacy Policy](./privacy.md)
