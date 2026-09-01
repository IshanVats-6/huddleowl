# HuddleOwl downloads

Installers for [HuddleOwl](https://huddleowl.com), the AI meeting coach that runs
on your own machine.

**There is no source code in this repository.** It exists so the download buttons
on the website have a public place to point at while the application's own
repository stays private. Every file here is attached to a
[release](../../releases).

## Get the app

Use the buttons on the website rather than these files directly. They always
point at the current build:

| | |
|---|---|
| Apple Silicon Mac | <https://huddleowl.com/download/mac> |
| Intel Mac | <https://huddleowl.com/download/mac-intel> |
| Windows | <https://huddleowl.com/download/windows> |

Free for individuals. No account, no card, no sign up.

## Verifying a download

Every release carries `SHA256SUMS.txt`. On macOS or Linux:

```
shasum -a 256 -c SHA256SUMS.txt --ignore-missing
```

On Windows:

```
certutil -hashfile HuddleOwl-0.1.9-win-x64.exe SHA256
```

## First launch on macOS

HuddleOwl is not notarised with Apple yet, which is a signing formality rather
than anything about the build. macOS will say the app is damaged. Run this once,
then open it again:

```
xattr -cr /Applications/HuddleOwl.app
```

## Windows SmartScreen

The build is unsigned, so SmartScreen asks once. Choose **More info**, then
**Run anyway**.
