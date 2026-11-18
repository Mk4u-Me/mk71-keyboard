# Changelog

## 1.0.0 — first public build

### Keyboard
- Bangla phonetic (Avro-style, custom) and fixed layouts, English QWERTY, symbols and emoji pages.
- On-screen key grid with Shift, Space, Enter, arrows and backspace.
- Suggestions for the next word, dates, times, numbers (in Bangla digits), emojis, calculator results and spell check.
- Encoding converter: ANSI / Bijoy / Probhat ↔ Unicode.

### Typing into other apps
- Physical keys are transliterated into the focused application; Control/Alt/Windows shortcuts always pass through.
- Paste with focus check, typing fallback, and support for Edit / RichEdit / Chromium and Electron text fields.

### Voice typing
- Google Web Speech (free, no key) plus optional Google Cloud, Groq Whisper, Deepgram (nova-3) and Sarvam AI.
- Automatic fallback to the free service; the paid service returns by itself when its allowance resets.
- Bilingual recognition map, silence detection and microphone device choice.

### AI (optional)
- Proofreading, synonyms, antonyms and translation through any OpenAI-compatible endpoint, or a Gemini key.
- Local rule-based proofreading works with no network or key.

### Window and settings
- Top bar opens at the top centre of the screen every launch, collapses when the pointer leaves, and no longer
  stays open after a missed mouse-leave event.
- Mouse wheel never changes a value in Settings unless its control is being used.
- Keyboard window position is clamped on screen when a monitor is removed or a resolution changes.
- Windows 7–11 manifest (DPI aware, long paths, common controls v6).

### Fixes
- Speech requests carry a proper User-Agent, so Cloudflare no longer blocks Groq with `error code: 1010`.
- API keys with a smart dash, space or line break are reported plainly instead of failing with a codec error.
- Sarvam defaults to `saaras:v4` and falls back to `saarika:v2.5` on older accounts.
- Tooltips no longer log `wrapped C/C++ object has been deleted` after a widget is destroyed.
- AI tools has a menu entry (⚙ → AI tools…) and a shortcut (Ctrl+Alt+A).
