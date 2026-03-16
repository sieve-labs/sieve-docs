# Installation & Setup

This page walks you through downloading Sieve, installing it on your device, and completing the first-time setup. The whole process takes about five minutes.

---

## Step 1 — Download the right version

Go to the [GitHub Releases page](https://github.com/sieve-sort/sieve-app/releases) and download the file for your platform.

| Platform | File to download |
|----------|-----------------|
| Android | `app-release.apk` |
| Linux | `sieve-linux.zip` |
| Windows | `sieve-windows.zip` |
| macOS | `sieve-macos.zip` |

Always download from the latest release unless you have a reason to use an older version.

---

## Step 2 — Install it

### Android

Android will warn you when installing an APK that didn't come from the Play Store. This is normal and expected — Sieve is distributed directly to keep it free with no marketplace fees.

1. Open the downloaded `.apk` file on your phone
2. Android will show a prompt saying the file is from an unknown source
3. Tap **Settings** and toggle on **Allow from this source**
4. Go back and tap **Install**
5. Once installed, open Sieve from your app drawer

> **Why no Play Store?** Google charges a fee on all paid apps and in-app purchases. Since Sieve is free and donation-supported, distributing directly means 100% of any donation goes to development rather than fees.

---

### Linux

1. Download `sieve-linux.zip`
2. Extract it to wherever you keep your applications, for example `~/Applications/sieve/`
3. Open a terminal in the extracted folder and run:
```bash
chmod +x sieve
./sieve
```
4. Optionally create a desktop shortcut pointing to the executable

---

### Windows

1. Download `sieve-windows.zip`
2. Extract the folder somewhere permanent — do not run it directly from the zip
3. Open the extracted folder and double click `sieve.exe`
4. Windows may show a SmartScreen warning since the app is not from the Microsoft Store — click **More info** then **Run anyway**

---

### macOS

1. Download `sieve-macos.zip`
2. Extract it and move `sieve.app` to your Applications folder
3. On first launch, macOS may block it because it is not from the App Store
4. Go to **System Settings → Privacy & Security** and click **Open Anyway**

---

## Step 3 — First launch: storage setup

The first time you open Sieve it will ask for permission to access your storage and ask you to choose a folder where sorted images will be saved.

**On Android:**
Sieve will show a permission dialog asking for storage access. Tap **Allow**. Without this, Sieve cannot save or organise your images.

If you accidentally tap Deny, go to your phone's **Settings → Apps → Sieve → Permissions** and enable storage manually.

**On desktop:**
A folder picker will open. Choose or create a folder where you want Sieve to store your organised images. This can always be changed later in Settings.

> **Screenshot placeholder — storage setup screen**

---

## Step 4 — First launch: API key setup

After storage setup, Sieve will ask you to choose an AI provider and enter an API key.

If you are not sure which provider to use, we recommend **OpenRouter** — it has a free tier that requires no credit card and works well for getting started.

See [Setting Up Your API Key](api-key-setup.md) for detailed instructions for each provider.

---

## You are ready

Once storage and API key setup are complete, you will land on the main screen and Sieve is ready to use.

Next: [Setting Up Your API Key](api-key-setup.md)
