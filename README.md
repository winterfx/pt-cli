# pt-cli

CLI tool for audio transcription with AI summary powered by OpenAI Whisper.

## Prerequisites

- [FFmpeg](https://ffmpeg.org/) must be installed on your system

```bash
# macOS
brew install ffmpeg

# Ubuntu/Debian
sudo apt install ffmpeg

# Windows
choco install ffmpeg
```

## Install

```bash
npm install -g @winterfx/pt-cli
```

## Configuration

Create `.env` file in `~/.pt/` or current directory:

```env
API_KEY=your_openai_api_key
BASE_URL=https://api.openai.com/v1
```

## Usage

```bash
pt <audio-file-or-url> [options]
```

### Options

| Option | Description |
|--------|-------------|
| `-s, --summary` | Generate AI summary |
| `-l, --language <lang>` | Language code (auto, en, zh, etc.) |
| `-o, --output <file>` | Output file path |
| `--output-format <format>` | text, json, markdown, srt |
| `-q, --quiet` | Suppress progress output |

### Examples

```bash
# Transcribe local file
pt audio.mp3

# Transcribe with summary
pt audio.mp3 -s

# Output as SRT subtitles
pt audio.mp3 --output-format srt -o subtitles.srt

# Transcribe from URL
pt https://example.com/podcast.mp3
```

## License

MIT
