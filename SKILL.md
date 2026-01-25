---
name: elevenlabs-voices
description: High-quality voice personas for text-to-speech using ElevenLabs API. 18 voices, presets, and Python script included.
version: 1.1.1
---

# ElevenLabs Voice Personas

High-quality voice personas for text-to-speech using ElevenLabs API.

## ✨ Features

- **18 Voice Personas** - Carefully curated voices for different use cases
- **Voice Presets** - Quick access: narrator, professional, warm, energetic, etc.
- **Python TTS Script** - Generate audio files directly
- **Multi-accent support** - American, British, Australian voices
- **Neutral/inclusive voice** - River for gender-neutral content

## 🎙️ Available Voices

| Voice | Accent | Gender | Persona | Best For |
|-------|--------|--------|---------|----------|
| rachel | 🇺🇸 US | female | warm | Conversations, tutorials |
| adam | 🇺🇸 US | male | narrator | Documentaries, audiobooks |
| bella | 🇺🇸 US | female | professional | Business, presentations |
| brian | 🇺🇸 US | male | comforting | Meditation, calm content |
| george | 🇬🇧 UK | male | storyteller | Audiobooks, storytelling |
| alice | 🇬🇧 UK | female | educator | Tutorials, explanations |
| callum | 🇺🇸 US | male | trickster | Playful, gaming |
| charlie | 🇦🇺 AU | male | energetic | Sports, motivation |
| jessica | 🇺🇸 US | female | playful | Social media, casual |
| lily | 🇬🇧 UK | female | actress | Drama, elegant content |
| matilda | 🇺🇸 US | female | professional | Corporate, news |
| river | 🇺🇸 US | neutral | neutral | Inclusive, informative |
| roger | 🇺🇸 US | male | casual | Podcasts, relaxed |
| daniel | 🇬🇧 UK | male | broadcaster | News, announcements |
| eric | 🇺🇸 US | male | trustworthy | Business, corporate |
| chris | 🇺🇸 US | male | friendly | Tutorials, approachable |
| will | 🇺🇸 US | male | optimist | Motivation, uplifting |
| liam | 🇺🇸 US | male | social | YouTube, social media |

## 🎯 Quick Presets

Use these shorthand names for common use cases:

- `default` → rachel (warm, friendly)
- `narrator` → adam (documentaries)
- `professional` → matilda (corporate)
- `storyteller` → george (audiobooks)
- `educator` → alice (tutorials)
- `calm` → brian (meditation)
- `energetic` → liam (social media)
- `trustworthy` → eric (business)
- `neutral` → river (inclusive)
- `british` → george
- `australian` → charlie
- `broadcaster` → daniel (news)

## 💻 CLI Usage

```bash
# List all voices
python3 scripts/tts.py --list

# Generate speech
python3 scripts/tts.py --text "Hello world" --voice rachel --output hello.mp3

# Use a preset
python3 scripts/tts.py --text "Breaking news..." --voice broadcaster --output news.mp3

# Test all voices (generates samples/)
python3 scripts/tts.py --test
```

## ⚙️ Configuration

The script looks for API key in this order:
1. `ELEVEN_API_KEY` environment variable
2. Clawdbot config (`~/.clawdbot/clawdbot.json` → tts.elevenlabs.apiKey)
3. Skill-local `.env` file

## 🎛️ Voice Settings

Each voice has tuned settings for optimal output:

- **stability** (0.0-1.0): Higher = more consistent, lower = more expressive
- **similarity_boost** (0.0-1.0): How closely to match the original voice
- **style** (0.0-1.0): Exaggeration of the speaking style

## 📝 Triggers

- "use {voice_name} voice"
- "speak as {persona}"
- "list voices"
- "voice settings"

## 📁 Files

```
elevenlabs-voices/
├── SKILL.md          # This file
├── voices.json       # Voice definitions & settings
├── examples.md       # Usage examples
├── scripts/
│   └── tts.py        # Python TTS script
└── references/
    └── voice-guide.md
```

## 🔗 Links

- [ElevenLabs](https://elevenlabs.io)
- [API Docs](https://docs.elevenlabs.io)
