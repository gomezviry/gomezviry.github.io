---
layout: default
title: Moop
subtitle: Home
permalink: /moop/
---

# Moop

<p class="tagline">A multiplatform notes app, kept on your devices.</p>

Moop is a notes application for iOS, Android, Web, Windows, macOS, and
Linux. It is local-first: notes live on your device, in an encrypted
database, and never touch a server controlled by us. Optional cloud sync
lets you mirror your notes to your own Dropbox, Google Drive, or OneDrive
account so the same notes are available on every device you sign in from.

## What Moop does

- **Write notes** in a Notion-style WYSIWYG editor with headings, lists,
  checkboxes, and inline formatting.
- **Attach files and images** to any note.
- **Organize** with nested notes (parent / child hierarchy) and tags.
- **Protect** sensitive notes behind a biometric or system-password unlock,
  and hide them from the main list entirely.
- **Export** any note as Markdown or PDF.
- **Sync** (optional) between devices through your own cloud account.

## Supported platforms

| Platform | Status |
|---|---|
| iOS | Supported |
| Android | Supported |
| Web | Supported |
| Windows | Supported |
| macOS | Supported |
| Linux | Supported |

A single Moop build runs on all six. The same notes appear everywhere once
cloud sync is configured.

## Why Moop asks for the data it asks for

Moop only requests data and permissions when you turn on the feature that
needs them. Every request is explained below.

### Google Drive access (`drive.file`, `drive.appdata`)

Requested only if you enable cloud sync with Google Drive. Moop uses the
narrowest possible scopes:

- **`drive.file`** — read and write only the files Moop itself creates in
  your Drive. Moop cannot see or modify any other file you store in Drive.
- **`drive.appdata`** — read and write Moop's hidden application folder
  in your Drive, used for sync metadata.

Moop uses this access exclusively to upload your notes to your Drive and
download them back to other devices you sign in from. Your notes are never
sent to any server we control and are never shared with anyone else.

### Dropbox and OneDrive access

Requested only if you enable cloud sync with that provider. Moop uses
*app-folder* permission, which limits access to a single folder Moop
creates inside your account. Moop cannot see the rest of your files. The
purpose is identical to the Drive case: upload and download your own notes.

### Biometric / device authentication

Requested only when you mark a note as protected or hidden. Moop calls the
operating system's authentication API and receives a yes / no result.
Biometric data never leaves the operating system and is never sent to Moop
or any third party.

### Files, storage, photos, camera

Requested only when you attach a file or image to a note, or export a
note. The selected file is stored inside Moop's encrypted database; no
broader access is taken or retained.

## What Moop never collects

Moop has no analytics, no crash reporting, no advertising identifiers, and
no Moop-operated account system. It does not collect personal information,
device identifiers, IP addresses, or behavioral data of any kind. There is
no server we control that could receive such data.

For the full statement, see the
[Moop Privacy Policy](/moop/privacy/).

## Get the app

Moop is currently in development. Distribution channels and download links
will be listed here when public builds are available. In the meantime, the
source is being prepared for release and questions are welcome by email.

## Help and contact

- [Support and FAQ](/moop/support/)
- [Privacy Policy](/moop/privacy/)
- Email: [gomez.viry@gmail.com](mailto:gomez.viry@gmail.com)
