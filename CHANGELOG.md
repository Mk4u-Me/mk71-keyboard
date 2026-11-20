# Changelog

## 1.0.7 — 2026-11-20

### Fixed
- পুরো শব্দ লেখার আগে, এমনিকি **একটি অক্ষর** লেখার পরেও এখন সাজেশন আসে। আগে
  শব্দের দ্বিতীয় কী চাপার আগ পর্যন্ত তালিকাটি তৈরি হত না, তাই এক অক্ষরে কিছুই
  দেখা যেত না।
- বাংলা অভিধানের তালিকা বর্ণানুক্রমিক হওয়ায় এক অক্ষরের প্রস্তাবে “অংক, অংকিত…”
  জাতীয় শব্দ আগে আসত; এখন ছোট ও নিত্যদিনের শব্দ আগে আসে (ক → কই, কংশ; কা → কা,
  কাঁচ)।

## 1.0.6 — 2026-11-20

### Added
- নতুন রিলিজ এলে অ্যাপ নিজেই জানায়: টপ বারের অ্যাপ মেনুতে **Update Available**
  (হলুদ ডটসহ) আসে আর ⚙ গিয়ার আইকনে ছোট হলুদ ডট বসে — চাপলে GitHub-এর ডাউনলোড
  পেজ খোলে।
- চেক হয় চালু হওয়ার কিছুক্ষণ পরে, তারপর প্রতি ৬ ঘণ্টায়; ইন্টারনেট না থাকলে বা
  GitHub-এ পৌঁছানো না গেলে কিছুই দেখায় না।

### Changed
- **Check for Update** আর “আপডেট সার্ভার নেই” বার্তা দেখায় না — এখন সত্যিই GitHub
  দেখে: নতুন কিছু না থাকলে জানায় আপনি সর্বশেষ ভার্সনেই আছেন, নতুন থাকলে
  Download / Later জিজ্ঞেস করে।
- বাংলা ইউজার গাইডে টপ বারের টেবিলে আপডেট নোটিসের কথা যোগ করা হয়েছে।

## 1.0.5 — 2026-11-19

### Changed
- নতুন ইনস্টল বা পোর্টেবল কপি প্রথমবার খুললে এখন **White** থিম ডিফল্ট — আগে Dark
  খুলত। পুরোনো ব্যবহারকারীর বেছে নেওয়া থিম আগের মতোই মনে থাকে।

## 1.0.4 — 2026-11-19

### Changed
- Appearance পেজ এখন সংক্ষিপ্ত: **Colour theme** ও **Window opacity** ছাড়া বাকি সব সারি
  (Font, Font size, Key height এবং নিচের বাংলা ব্যাখ্যা বক্স) সরানো হয়েছে।
- ফন্ট, ফন্ট সাইজ ও কী-এর উচ্চতা অ্যাপের নির্ধারিত মানেই থাকে, তাই ভুল সেটিংসে
  কিবোর্ড এলোমেলো হওয়ার সুযোগ নেই।

## 1.0.3 — 2026-11-18

### Changed
- **AI tools** এখন Settings → AI পেজের ভেতরে **“Open AI tools…”** বাটনে — endpoint আর key যেখানে দেওয়া হয়, প্রুফরিড/সমার্থক/অনুবাদও সেখান থেকেই খোলা যায়।
- টপ-বারের মেনু থেকে আলাদা “AI tools…” এন্ট্রি সরানো হয়েছে; ট্রে মেনু ও **Ctrl+Alt+A** আগের মতোই কাজ করে।

## 1.0.2 — 2026-11-18

### Fixed
- Appearance-এ **Colour theme** (Dark / White) ড্রপডাউন ফিরে এসেছে। 1.0.1-এ নতুন বাংলা লেবেল যোগ করার সময় সারিটি ভুলে পেজে যোগ হয়নি।
- সেটিংসের স্মোক টেস্ট হালনাগাদ (পুরোনো `QuickTipDialog` ইমপোর্ট সরানো হয়েছে)।

## 1.0.1 — 2026-11-18

### Appearance
- Window opacity, Font, Font size and Key height now carry a plain Bangla line beside them, so what each one changes is readable without a tooltip.
- Window opacity shows its exact percentage next to the slider and explains what raising or lowering it does.

### Speech and AI
- New **How to set API key** button in Speech to Text: written steps and clickable site links for Google Cloud, Groq, OpenAI, Deepgram, Sarvam AI and Gemini.

### Look and feel
- The white theme now paints the same 84% glass panels as the dark one; key caps stay solid.
- The top bar opens at 61% transparency by default.

### Documentation
- A 20-page Bangla user guide ships next to the executable in every build.

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
