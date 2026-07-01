# Tota Releases

## v2.8 (2026-07-01)

- Audio Drop (new): drop in a recording and get a full transcript with automatic speaker labels — who said what, start to finish. Rename speakers to real names, and export to plain text, Markdown, subtitles (SRT), JSON, or CSV. Everything runs on your Mac.
- Timestamps, your way: show them once per speaker turn, on every sentence, or turn them off entirely.
- Cleaner transcripts: removed stray caption markers and formatting artifacts that could appear at the start of lines.
- A progress bar now shows how far along a transcription is.


## v2.7 (2026-06-30)

- Vocabulary & Glossaries (new): teach Tota the names, jargon, and acronyms you use — it biases transcription toward your terms, corrects common mishears, and can automatically pick the right glossary based on the app you're dictating into
- Smart Formatting stays in its lane: fixed cases where it would answer or act on your dictation instead of just cleaning it up, and hardened it against text that tries to hijack the formatter
- Faster Smart Formatting: the system prompt is now cached, so each cleanup runs quicker
- Fixed a bug that could occasionally produce an empty transcription


## v2.6 (2026-06-29)

- Smart Formatting (new): an optional on-device AI model cleans up your dictation — fixing typos and misheard words and formatting lists — all processed locally on your Mac
- Faster first transcription: the speech model now warms up in the background at launch, so your first dictation no longer stalls
- Accurate download progress and speed when fetching the Smart Formatting model


## v2.5 (2026-03-20)

- Added multilingual transcription: choose Transcribe or Translate to English for non-English speech
- Added language selection: Auto-detect plus 11 languages (Spanish, French, German, Italian, Portuguese, Japanese, Chinese, Korean, Russian, Arabic, Hindi, Dutch)
- Fixed selected Whisper model not persisting across app launches, which caused language settings to reset
- Fixed recording overlay intermittently disappearing during transcription when dictionary polling was active


## v2.4 (2026-03-14)

- Added "Hey Tota" wake word for hands-free activation using Apple's on-device speech recognition
- Added auto-stop recording on silence with configurable delay
- Fixed voice command shortcut display (e.g. "Cmd+G" instead of "Cmd+Key(5)")
- Fixed checkbox hit-testing in command modifier key selection
- Moved Cancel button to left side of forms for consistency
- Forms scroll into view when adding new commands, snippets, or filler words


## v2.3 (2026-03-13)

- Added fn (🌐) key as a hold-to-talk option
- Added ⌘, keyboard shortcut to open Settings
- Whisper non-speech tags like [BLANK_AUDIO] and [MUSIC] are now automatically filtered out


## v2.2 (2026-03-11)

- Voice commands now sorted alphabetically across all tabs
- Website commands renamed from "open" to "visit"
- Added Claude desktop app command
- Added Protonmail website command
- Added "chat" as alias for ChatGPT command
- Custom commands now appear within category tabs with blue outline
- Cleaner action descriptions
- Built-in dictionary corrections for automatic transcription fixes


## v2.1 (2026-03-10)

Added option to hide Tota from Cmd+Tab app switcher (Settings > General > Behavior)


## v2.0 (2026-03-09)

Fixed a crash when audio device becomes unavailable (Bluetooth disconnect, sleep/wake)


## v1.9 (2026-03-08)

Fixed a crash when audio device becomes unavailable (Bluetooth disconnect, sleep/wake)


## v1.8 (2026-03-08)

Fixed a crash when audio device becomes unavailable (Bluetooth disconnect, sleep/wake)


## v1.7 (2026-03-04)

UI improvements


## v1.6 (2026-03-04)

UI improvements

