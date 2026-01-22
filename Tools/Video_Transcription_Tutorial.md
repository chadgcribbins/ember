# Video Transcription Tutorial
## How to Download and Transcribe Videos from Any Website

This tutorial shows you how to download videos from 1000+ websites and automatically transcribe them using AI.

---

## What You'll Need

- **yt-dlp**: Universal video downloader (supports YouTube, Twitter/X, TikTok, Facebook, Instagram, Vimeo, Reddit, LinkedIn, and 1000+ more sites)
- **ffmpeg**: Video processing library (required by yt-dlp)
- **OpenAI Whisper**: AI-powered transcription tool (supports 99 languages)

---

## One-Time Setup

### Install the Tools (macOS)

```bash
# Install yt-dlp and ffmpeg
brew install yt-dlp ffmpeg

# Install Whisper
python3 -m pip install --break-system-packages openai-whisper
```

### Install the Tools (Linux/WSL)

```bash
# Install yt-dlp and ffmpeg
sudo apt update
sudo apt install yt-dlp ffmpeg

# Install Whisper
pip3 install openai-whisper
```

### Install the Tools (Windows)

```bash
# Install using pip
pip install yt-dlp
# Download ffmpeg from https://ffmpeg.org/download.html

# Install Whisper
pip install openai-whisper
```

---

## How to Use

### Step 1: Download the Video

```bash
# Basic download
yt-dlp "VIDEO_URL"

# Download to a specific filename
yt-dlp -o "my_video.%(ext)s" "VIDEO_URL"

# Download to a specific folder
cd /path/to/your/folder
yt-dlp -o "video_name.%(ext)s" "VIDEO_URL"
```

**Examples:**
```bash
# YouTube video
yt-dlp "https://youtube.com/watch?v=dQw4w9WgxcQ"

# Twitter/X video
yt-dlp "https://x.com/i/status/1999531989469397437"

# TikTok video
yt-dlp "https://www.tiktok.com/@user/video/1234567890"

# Instagram video
yt-dlp "https://www.instagram.com/p/ABC123/"
```

### Step 2: Transcribe the Video

```bash
# Basic transcription (auto-detects language)
whisper video_name.mp4

# Specify language (faster, more accurate)
whisper video_name.mp4 --language English

# Choose model size (tiny, base, small, medium, large)
whisper video_name.mp4 --model base  # Good balance of speed/accuracy
whisper video_name.mp4 --model small  # More accurate, slower
whisper video_name.mp4 --model large  # Best accuracy, slowest
```

### Step 3: Get Your Transcript

Whisper creates a `.txt` file with the same name as your video:
- Input: `video_name.mp4`
- Output: `video_name.txt`

---

## Output Formats

Whisper supports multiple output formats:

```bash
# Plain text (default)
whisper video.mp4 --output_format txt

# Subtitles (SRT format)
whisper video.mp4 --output_format srt

# WebVTT subtitles
whisper video.mp4 --output_format vtt

# JSON with word-level timestamps
whisper video.mp4 --output_format json

# All formats at once
whisper video.mp4 --output_format txt,srt,vtt,json
```

---

## Complete Workflow Example

```bash
# 1. Navigate to your folder
cd ~/Documents/transcripts

# 2. Download video with a descriptive name
yt-dlp -o "ai_university_talk.%(ext)s" "https://x.com/i/status/1999531989469397437"

# 3. Transcribe it
whisper ai_university_talk.mp4 --model base --output_format txt

# 4. Rename transcript with a meaningful name
mv ai_university_talk.txt "AI_Native_University_2026_Transcript.txt"

# 5. Clean up video file (optional)
rm ai_university_talk.mp4
```

---

## Supported Websites

yt-dlp supports **1000+ websites** including:

**Social Media:**
- YouTube, YouTube Music, YouTube Shorts
- Twitter/X (videos and spaces)
- TikTok
- Instagram (posts, reels, stories)
- Facebook (videos, live streams)
- LinkedIn
- Reddit

**Video Platforms:**
- Vimeo
- Dailymotion
- Twitch
- Rumble
- Odysee

**Educational:**
- Coursera
- Khan Academy
- Udemy
- edX

**News & Media:**
- CNN, BBC, NBC
- ESPN, Fox Sports
- NPR, PBS

**And many more!** See full list: https://github.com/yt-dlp/yt-dlp/blob/master/supportedsites.md

---

## Whisper Language Support

Whisper supports **99 languages** including:
- English, Spanish, French, German, Italian, Portuguese
- Chinese (Mandarin), Japanese, Korean
- Arabic, Hindi, Russian, Turkish
- And 87 more languages!

```bash
# Specify language for better accuracy
whisper video.mp4 --language Spanish
whisper video.mp4 --language Japanese
whisper video.mp4 --language Arabic
```

---

## Troubleshooting

### "yt-dlp: command not found"
- Reinstall: `brew install yt-dlp` (macOS) or `pip install yt-dlp`

### "whisper: command not found"
- Reinstall: `python3 -m pip install --break-system-packages openai-whisper`

### Video won't download
- Some sites require authentication or block downloads
- Try: `yt-dlp -F "URL"` to list available formats
- Try: `yt-dlp --cookies-from-browser chrome "URL"` to use browser cookies

### Transcription is inaccurate
- Use a larger model: `--model small` or `--model medium`
- Specify language: `--language English`
- Ensure audio quality is good

### "FP16 is not supported on CPU" warning
- This is normal on non-GPU systems, can be ignored
- Whisper will automatically use FP32 instead

---

## Pro Tips

### 1. Download Audio Only (Faster)
```bash
yt-dlp -x --audio-format mp3 "VIDEO_URL"
whisper audio.mp3  # Whisper works with audio files too!
```

### 2. Batch Process Multiple Videos
```bash
# Create a file with URLs (one per line)
cat > videos.txt << EOF
https://youtube.com/watch?v=VIDEO1
https://x.com/i/status/12345
https://vimeo.com/12345678
EOF

# Download all
yt-dlp -a videos.txt

# Transcribe all
for file in *.mp4; do
  whisper "$file" --model base
done
```

### 3. Get Timestamps
```bash
# Output includes timestamps by default in SRT/VTT
whisper video.mp4 --output_format srt

# Example output (in .srt file):
# [00:00.000 --> 00:07.200]
# In 2026, we'll see the birth of the first AI Native University...
```

### 4. Transcribe Live Streams
```bash
# Download live stream
yt-dlp "LIVE_STREAM_URL"

# Or download and transcribe in one go
yt-dlp "STREAM_URL" -o stream.mp4 && whisper stream.mp4
```

---

## Cost

- **yt-dlp**: Free and open source
- **ffmpeg**: Free and open source
- **Whisper**: Free and open source (runs locally on your computer)
- **No API costs**, **No subscriptions**, **No limits**

---

## Privacy

All processing happens **locally on your computer**:
- Videos are downloaded directly to your machine
- Transcription runs on your CPU/GPU
- No data is sent to external servers (except the original download)
- You have complete control over your files

---

## References

- **yt-dlp GitHub**: https://github.com/yt-dlp/yt-dlp
- **Supported Sites**: https://github.com/yt-dlp/yt-dlp/blob/master/supportedsites.md
- **Whisper GitHub**: https://github.com/openai/whisper
- **Whisper Model Comparison**: https://github.com/openai/whisper#available-models-and-languages

---

## Quick Reference

```bash
# Download video
yt-dlp -o "filename.%(ext)s" "URL"

# Transcribe (basic)
whisper filename.mp4

# Transcribe (optimized)
whisper filename.mp4 --model base --language English --output_format txt,srt

# Clean up
rm filename.mp4
```

---

*Last updated: December 2025*
