---
layout: default
title: Privacy Policy
subtitle: Privacy Policy
permalink: /moop/privacy/
---

# Privacy Policy

<p class="meta">Last updated: 23 May 2026</p>

Moop is a local-first notes application. By default, your data never leaves
the device it was created on. This policy explains what data Moop handles,
where it is stored, and what choices you have.

## Short version

- Moop stores your notes locally on your device.
- The notes database is encrypted at rest.
- Moop does not operate any server that collects, receives, or stores your notes.
- If you enable cloud sync, your notes are uploaded to **your own** cloud
  storage account (Dropbox, Google Drive, or OneDrive). Moop is not a party
  to that storage.
- Moop contains no analytics, advertising, or third-party tracking.

## What Moop processes

### Notes and attachments

Notes you create — including their title, content, tags, hierarchy,
attachments, and timestamps — are stored on your device in an encrypted
SQLite database. The encryption key is generated on first launch and stored
in the operating system's secure keystore (Keychain on iOS/macOS, Keystore
on Android, Secret Service / libsecret on Linux, Credential Manager on
Windows, secure storage on Web).

### Biometric and device-authentication signals

If you enable biometric or system-password unlock for protected or hidden
notes, Moop calls the operating system's authentication APIs and receives
only a yes/no result. Biometric data itself never leaves the operating
system and is never sent to Moop or any third party.

### Cloud-sync credentials and tokens

If you enable cloud sync, the OAuth access and refresh tokens needed to
connect to your chosen provider are stored locally in the secure keystore
described above. They are sent only to the provider you selected, over
HTTPS, in order to upload and download your notes.

### No analytics or telemetry

Moop does not embed analytics SDKs, crash reporters, advertising
identifiers, or any other telemetry that transmits data off the device.

## Cloud sync (optional)

Cloud sync is off by default. When you enable it and connect a provider:

- Your notes are serialized and uploaded to a folder inside **your** account
  with that provider.
- The provider — Dropbox, Google (Drive), or Microsoft (OneDrive) — receives
  and stores that data under its own terms of service and privacy policy.
  Moop is not the data controller for that storage.
- You can revoke Moop's access at any time from the provider's account
  settings, and you can disable cloud sync in Moop's Settings to stop further
  uploads.
- Disabling cloud sync does not delete files already in your provider
  account. You can delete those files directly through the provider.

Provider privacy policies:

- Dropbox — <https://www.dropbox.com/privacy>
- Google Drive — <https://policies.google.com/privacy>
- Microsoft OneDrive — <https://privacy.microsoft.com/privacystatement>

## Device permissions

Depending on the platform, Moop may request the following permissions. Each
is used only for the stated purpose and only when you trigger the relevant
feature:

- **Biometric / authentication** — to unlock protected and hidden notes.
- **Files / storage / photos / camera** — to attach files or images to a
  note, or to export a note.
- **Network** — only when cloud sync is enabled, and only to communicate
  with the provider you configured.
- **Browser session (OAuth)** — to complete sign-in with Dropbox, Google,
  or Microsoft when you connect cloud sync.

Moop does not request location, contacts, microphone, or
advertising-identifier permissions.

## What Moop does not collect

Moop does not collect, transmit, or sell:

- Personal identifiers (name, email, phone number)
- Account profiles or login credentials for any Moop-operated service
  (there is no such service)
- Device identifiers, advertising IDs, or fingerprints
- IP addresses (Moop has no server to receive them)
- Usage analytics, behavioral data, or crash reports

## Children

Moop is a general-purpose productivity tool and is not directed to children.
We do not knowingly collect data from children. Because Moop does not
collect personal data at all, this clause is stated for clarity rather than
necessity.

## Your choices and controls

- **View and export:** Notes can be exported as Markdown or PDF from within
  the app.
- **Delete:** Deleting a note removes it from the local encrypted database.
  If cloud sync is enabled, the deletion is propagated to your cloud
  provider on the next sync.
- **Disconnect sync:** Disabling cloud sync clears the stored provider
  credentials from your device.
- **Uninstall:** Removing Moop from your device deletes the local database
  and the encryption key from the operating system keystore. Notes stored in
  your cloud provider account remain there until you delete them through
  the provider.

## Changes to this policy

If this policy materially changes, the "Last updated" date at the top of the
document will be revised, and the updated version will be published in this
same location. Continued use of Moop after a change indicates acceptance of
the revised policy.

## Contact

Questions about this policy can be sent to
[gomez.viry@gmail.com](mailto:gomez.viry@gmail.com).
