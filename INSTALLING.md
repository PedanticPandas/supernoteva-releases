# Installing SuperNoteva on a Mac (test builds)

For someone given a `SuperNoteva_<version>_universal.dmg` to try. This is a
**test build**: don't keep anything in it you can't afford to lose.

The app runs on both Apple Silicon and Intel Macs.

## 1. Install

1. Double-click the `.dmg`.
2. Drag **SuperNoteva** onto **Applications**.
3. Eject the disk image (the eject arrow beside it in Finder's sidebar).

## 2. Open it the first time

macOS blocks the first launch. The app is signed, but not by a developer
registered with Apple, so macOS can't vouch for it. You only do this once.

**macOS 15 (Sequoia) and later**

1. Open **SuperNoteva** from Applications. macOS says it could not verify
   the app. Click **Done** (not "Move to Trash").
2. Open **System Settings → Privacy & Security** and scroll down to
   **Security**.
3. Beside "SuperNoteva was blocked to protect your Mac", click
   **Open Anyway**.
4. Confirm with your password or Touch ID, then click **Open Anyway** in
   the dialog that follows.

**macOS 14 (Sonoma) and earlier**

1. In Applications, **right-click** (or Control-click) SuperNoteva and
   choose **Open**.
2. Click **Open** in the dialog.

**If you're comfortable in Terminal**, this one line does the same thing:

```bash
xattr -dr com.apple.quarantine /Applications/SuperNoteva.app
```

After this, SuperNoteva opens like any other app.

## 3. Sign in

Choose **Create account** and sign up with an email and password. Your
notes are stored under that account and sync to any other device you sign
in on, including the web version.

## 4. The notes folder

SuperNoteva keeps a plain-Markdown copy of your notes in a folder on your
Mac (by default inside Documents). macOS asks once for permission to use
that folder: click **Allow**. You can change the folder in
**Settings → Files & sync → Notes folder**.

## Updating

There is no automatic update yet. When you're sent a newer `.dmg`:

1. Quit SuperNoteva.
2. Open the new `.dmg` and drag SuperNoteva onto Applications, choosing
   **Replace**.

Your notes are in your account, not in the app, so replacing it loses
nothing. macOS may ask you to repeat step 2 above for the new copy.

## Removing it

Quit SuperNoteva and drag it from Applications to the Trash. The Markdown
folder stays where it is until you delete it yourself.
