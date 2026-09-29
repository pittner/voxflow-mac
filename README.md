# VoxFlow Pro for Mac: free offline push-to-talk dictation

Hold a key, say the sentence, let go. The text appears in whatever app you were already typing in. Everything is transcribed on your own Mac with [WhisperKit](https://github.com/argmaxinc/WhisperKit), so it also works on a plane or with Wi-Fi off.

**[Download VoxFlow Pro for Mac (1.9 MB) from the official page](https://bemooore.com/voxflow/mac/?utm_source=github&utm_medium=referral&utm_campaign=voxflow_mac_repo&utm_content=readme_top)**

Free. Version 1.0, macOS 14.0 Sonoma or later, Apple Silicon and Intel (universal binary). Notarized by Apple. No account, no subscription, no trial timer.

> This repository is an information and support page. The app itself is distributed only from the official page above, not from this repository. There is no source code here.

## What you get

| | |
|---|---|
| **Push-to-talk** | Hold Globe, Caps Lock or the right Shift key, speak, release. Text goes into the focused app. Each trigger is toggleable in Settings. |
| **On-device transcription** | WhisperKit runs the model locally on your Mac. No VoxFlow server is involved. |
| **iCloud sync (optional)** | Notes sync through your own iCloud account with the iPhone and Apple Watch app. No VoxFlow account. |
| **Universal binary** | x86_64 and arm64 in one app, native on Intel and Apple Silicon. |
| **Permissions** | Microphone to record. Accessibility to notice the push-to-talk key. Nothing else. |

## The 60 second version

1. Download the disk image from the [official page](https://bemooore.com/voxflow/mac/?utm_source=github&utm_medium=referral&utm_campaign=voxflow_mac_repo&utm_content=readme_steps), drag VoxFlow to Applications, open it.
2. Grant Microphone when asked, then Accessibility in System Settings so it can see the push-to-talk key.
3. Put the cursor in any app. Hold your trigger key, say a sentence, release.

## Verify it before you run it

A direct download is not reviewed by anyone for you, so check it yourself.

```sh
shasum -a 256 ~/Downloads/VoxFlow-1.0.dmg
```

It must print exactly:

```
0abd7dde30fe2dc592e6f114592aa553b8c6a3ba177f84cd70850e27442ba8da
```

`VoxFlow-1.0.dmg`, 1 986 338 bytes. Once the app is in Applications:

```sh
spctl -a -vvv -t exec /Applications/VoxFlow.app
```

The answer should be `accepted`, `source=Notarized Developer ID`, `origin=Developer ID Application: BIT Technology s.r.o. (T3BMR868R2)`. Because it is notarized, it opens with a normal double click. Be suspicious of any Mac download that asks you to disable Gatekeeper.

## What it is not

- **Not on the Mac App Store.** VoxFlow on the App Store is the iPhone, iPad and Apple Watch app and has no Mac build.
- **No auto-update.** Version 1.0 has no updater built in. New builds are published on the official page and you replace the app yourself. Watch this repository (Releases only) if you want a notification when a new build is announced.
- **Not a meeting recorder or a transcription service.** No minute quota because there is no server counting minutes, but also no dashboard, no team workspace and no web app.
- **Not a rewrite of your text.** It writes down what you said, in the app you are already in.

## FAQ

**Does my audio leave the Mac?**
No. Transcription runs locally through WhisperKit on your Mac. There is no VoxFlow backend to upload recordings to. This is a description of how the app works, not a legal or compliance claim.

**What does it cost?**
Nothing. If it saves you time there is a voluntary [support button](https://bemooore.com/voxflow/mac/?utm_source=github&utm_medium=referral&utm_campaign=voxflow_mac_repo&utm_content=readme_support) on the official page. It changes nothing about the app, there is no licence and no extra features.

**Is there an iPhone or Apple Watch version?**
Yes, a separate free App Store download: [VoxFlow on the App Store](https://apps.apple.com/app/id6760209368). That is the version Apple reviews.

**Where do I report a bug or ask a question?**
Open an [issue](https://github.com/pittner/voxflow-mac/issues) in this repository, or use the [support page](https://bemooore.com/voxflow/support/?utm_source=github&utm_medium=referral&utm_campaign=voxflow_mac_repo&utm_content=readme_faq).

## Links

- Official download page: https://bemooore.com/voxflow/mac/
- VoxFlow overview: https://bemooore.com/voxflow/
- [Privacy Policy](https://bemooore.com/voxflow/privacy/) · [Terms of Service](https://bemooore.com/voxflow/terms/)

VoxFlow is made by BIT Technology s.r.o.
