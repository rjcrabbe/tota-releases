# Tota Releases

## v3.9.1 (2026-09-05)

- Fixed: entering a wrong or seat-limited license key no longer removes your existing activation — the new key is checked first and your current license stays put if it fails
- Fixed: if Tota loses its license record and can't reach the license server (offline, DNS), licensed users keep working for 7 days with a "couldn't verify" notice and a Retry button instead of a "trial ended" lock-out
- License status is re-checked when you bring Tota to the front, so a yearly expiry is noticed without a relaunch
- Your dictionary, snippets, glossaries, voice commands, macros, filler words and clipboard history are written atomically, and a file that fails to load is set aside as a .corrupt backup instead of being silently replaced with defaults
- Dictionary corrections now apply next to line breaks (lists, paragraphs) and keep the capitalisation of the word you said
- Correction-pair logging (Settings → Corrections → "Keep a record of your corrections") is now off by default, never stores the words seen on your screen, and its file is readable only by your user account
- Smart Formatting: if the formatter hits an error, you see the "ran into an error" notice instead of silently getting the raw transcript
- Fixed: pressing the hotkey moments after launch no longer races the model's warm-up
- Fixed: two dictations in quick succession with an empty clipboard now leave the clipboard empty
- Fixed: editing a secure snippet's secret can no longer leave the snippet locked with no secret behind it
- Settings → Support: the support docs link now points to heytota.com/docs/troubleshooting
- Context spelling: ordinary plurals and inflections ("reports", "settings", "files") and UK spellings ("colours") are no longer rewritten toward a similar-sounding on-screen name
- Context spelling: multi-word on-screen names must match every word, and window titles with a spaced hyphen ("App - Section") are treated as separate names
- Reverting a screen spelling from the corrections card now stops that correction for the rest of the session; the card also has a close button and lingers less after the pointer leaves
- Onboarding: the "Sharper transcription" step now offers the Medium (English) model as a background download — the built-in model keeps working while it fetches, and nothing switches until you press "Use Medium"
- If a data file can't be read or backed up, Tota keeps it read-only for the session rather than writing defaults over it


## v3.9 (2026-08-30)

- New: Spell what's on your screen — when you start dictating, Tota glances at the window you're dictating into and spells the names and labels you're looking at correctly. It happens entirely on your Mac and nothing is stored or sent anywhere. On by default; turn it off in Settings → Corrections
- When a context correction fires, it shows in the corrections card with one-click Revert and "don't correct again"
- New notch indicator: on Macs with a notch, recording status hugs the notch with a live waveform and a transcribing animation — the floating pill remains on screens without one
- Say your formatting: spoken brackets and casing commands — "open bracket … close bracket", "all caps", "camel case", "snake case" — with a new onboarding step to learn them
- "Hey Tota" hears you more reliably, with better recognition biasing and fuzzy matching for close pronunciations
- Fixed: quiet trailing speech at the end of a dictation is no longer cut off
- Fewer wrong autocorrections: everyday modern words are never rewritten, and low-confidence transcriptions no longer trigger biased rewrites
- Glossaries now live behind a single switch at the top of the Glossaries page, off by default — flip it on if you use them
- Smart Formatting: question marks no longer split a clause from its sentence, and the first format after your Mac wakes is much faster
- Fixed: stray leading space when pasting into Gmail in Chrome, and mirrored error-banner text after wake


## v3.5 (2026-07-15)

- New Analytics tab: words-per-minute, a daily activity heatmap, and your dictation streak — also a click away from the stats at the top of Home
- Analytics rebuilds your full history from your archives, so the heatmap and streaks reach back to your first dictation
- See which apps you dictate into most (counting starts with this update)
- Fun all-time milestones: books and pages written, time saved vs typing, weeks with Tota — and a naughty word counter


## v3.4 (2026-07-14)

- Secure snippets: store passwords and other secrets encrypted in your Mac's keychain — say the trigger, confirm with Touch ID, and Tota pastes it. Never shown again after saving, never in history or logs
- Snippets can now be command-only: say the trigger on its own to insert, without it firing mid-dictation (the new default for new snippets)
- Duplicate-trigger warning when a snippet clashes with another snippet, voice command, or macro
- New built-in commands: "clear" (clears the current line), "new" (⌘N), and "next field" / "tab"
- Clearer guidance when macOS secure keyboard entry pauses dictation shortcuts, with a wake-word tip


## v3.3 (2026-07-12)

- Macros can now take dictation: say a macro trigger and keep talking — your words fill {dictation} slots, with "next field" jumping between them
- Reorder macro steps by dragging; adjacent dictated-text steps get a Tab inserted between them automatically
- New spoken layout commands: "new paragraph", "new line", and "new list" — say them mid-dictation or on their own
- Fixed: dictating at the start of a line no longer inserts a stray leading space


## v3.2 (2026-07-11)

- Settings reorganised into five clear tabs so every option is easier to find
- Learned corrections now appear in a card in the lower part of the screen, with a bigger Undo button — multiple corrections from one dictation are shown together with Undo All
- Fixed: dictating into a terminal (e.g. Claude Code) could teach the dictionary screen junk, which then corrupted future dictations or added words to them
- Glossary biasing is now off by default — switch a glossary on in Settings → Vocabulary when you want it; turning it off now sticks across restarts


## v3.1 (2026-07-10)

- Redesigned onboarding tour: brand-new visuals, a privacy-first welcome, and live demos throughout
- Smart Formatting can now be switched on during onboarding — the model download starts right away with progress shown
- Onboarding now previews the correction Undo pill and the transcription models, and credits WhisperKit
- Fixed: recording could fail with an "Audio device unavailable" error right after switching microphones (e.g. after picking a mic during onboarding)
- Fixed: adding a custom voice command could duplicate built-in commands; custom commands are now labelled and apps categorised correctly


## v3.0 (2026-07-10)

- Dictation now keeps recording when you switch apps mid-sentence (⌘Tab) — previously the recording was cut off or lost at the switch
- Dictation is no longer interrupted by automation tools (e.g. AI agents) typing or switching apps in the background
- If you've moved to a different app by the time transcription finishes, Tota no longer pastes into the wrong window — the text is copied to your clipboard with an on-screen "Press ⌘V to paste" prompt
- New English Spelling setting (US/UK): UK keeps British spellings (colour, realise, centre) in transcriptions and Smart Formatting
- A large on-screen alert now appears when your microphone changes (e.g. plugging into a display or unplugging headphones), and your next dictation shows which microphone it's using
- Fixed: unplugging your selected microphone could silently record from the wrong device — or nothing at all; dictation now verifiably switches to the built-in mic (never a nearby iPhone)
- Audio Input settings now always show the microphone actually in use, and your preferred mic is picked up again automatically when reconnected
- Smart Formatting now lays out messages and letters properly — greeting, body, and sign-off on their own lines
- Smart Formatting tells you when a dictation couldn't be formatted (model still loading, or the cleanup was skipped) instead of failing silently
- "Open URL" voice commands now work without typing the https:// prefix


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

