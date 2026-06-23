# Privacy Policy

[🏠 Document Top](../index.md) | [⚖️ Terms of Service](./terms.md) | [🔒 Privacy Policy](./privacy.md)

---

> **Canonical source:** This GitHub Pages document is the latest official version. If bundled app copies or website summary pages differ, this page takes precedence.

Last updated: June 23, 2026

## 1. Introduction

This Privacy Policy explains how FefaEther (the "Operator") handles data in the photo management application "Virtual Snap Archive" ("VSA" or the "App") and the related website.

VSA is local-first. Photos, thumbnails, metadata, and settings are primarily stored on your PC. Some features, including VSA account login, cloud storage, share links, X posting, and update checks, communicate with external services when you use them.

## 2. Data Stored Locally

The App primarily stores the following data on your PC:

- Photos and thumbnails
- Photo metadata such as capture time, world name, users in the same instance, and camera information
- App settings such as import folders, export destinations, display settings, and compression settings
- User-created settings such as X posting presets

Because users can choose watched folders and export destinations, VSA uses broad local file permissions. VSA does not collect or transmit unrelated files on your PC without a user-selected feature or setting.

## 3. Data Sent Externally

The following features send data externally when used.

### 3.1 VSA Account and Authentication

For login, email verification, OAuth login, and desktop app linking, data such as email address, authentication state, device information, and OAuth results may be sent to and stored by the VSA website and Supabase. The desktop app stores authentication-related information in a protected area on your device.

If Google OAuth is used, Google's authorization screen and Google account information are used for authentication. For Google OAuth app publishing settings, use the VSA website privacy policy page (Japanese: `/ja/privacy`, English: `/en/privacy`).

### 3.2 Cloud Storage

When cloud storage is enabled, selected photo files, file names, file sizes, MIME types, capture time, dimensions, and metadata are sent to the VSA website API and stored in cloud storage such as Cloudflare R2. Cloud storage is optional. Availability, plan, and limits may vary.

### 3.3 Share Links

When share links are used, shared photos, link identifiers, and metadata needed for access conditions may be sent to the VSA website API.

### 3.4 X Posting

When X posting is used, the post text, selected images, X account linking status, monthly usage count, and plan information are sent to the VSA website API. VSA shows the monthly limit and post content before posting, and posts to X only after the user explicitly confirms each post. X OAuth authorization links the account; it is not blanket consent for future posts.

### 3.5 Turnstile

The website may use Cloudflare Turnstile on registration, login, verification, and related screens to prevent abuse. When Turnstile is used, Cloudflare may process IP address, User-Agent, browser/network signals, and related data.

### 3.6 External APIs and Update Checks

Server status features may request VRChat status and Steam-related APIs. App update checks may access GitHub Releases or related update endpoints.

## 4. Purposes of Use

The Operator uses collected data for:

- Providing the App and related website
- Running user-selected features such as photo management, cloud storage, share links, and X posting
- Managing login state, plans, and monthly usage counts
- Preventing abuse, spam, and excessive use
- Investigating incidents, improving security, and providing support

## 5. Third-Party Services

VSA may use the following third-party services:

- Supabase: authentication, database, and session management
- Cloudflare R2: cloud photo storage
- Cloudflare Turnstile: bot and abuse prevention
- Cloudflare Workers: website and API hosting
- Google: Google OAuth login
- X: X account linking and posting
- GitHub: update distribution

Each third-party service may also apply its own privacy policy and terms.

## 6. Data Deletion

Local data can be deleted by removing the App's storage folders, database, and settings files. To request deletion of cloud data, account data, share link data, or X account linking data, use the account features on the related website or contact the Operator.

## 7. Security

The Operator applies reasonable safeguards, including encrypted transport, protected on-device storage, and access controls. However, no internet transmission or digital storage is completely secure.

## 8. Minors

You may not use the App or related website if you are under 13 years old. If you are at least 13 but under 18, use VSA only with parental or guardian consent.

## 9. Changes

This Policy may be updated due to feature additions, third-party service changes, or legal requirements. Significant changes will be announced with the revised content, effective date, and notice method on the website, in the App, or in release notes.

## 10. Contact

For privacy questions, contact:

virtualsnaparchive@gmail.com
