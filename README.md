# YouTube Cookie Exporter

A Chrome/Edge browser extension to export YouTube cookies in Netscape format for yt-dlp.

## Why?

yt-dlp requires YouTube cookies to access age-restricted or members-only content. This extension exports them in the format yt-dlp expects.

## Installation

### Chrome/Edge
1. Download the latest release from the [Releases page](https://github.com/YOUR_USERNAME/yt-cookie-extension/releases)
2. Unpack the `.zip` file
3. Go to `chrome://extensions/`
4. Enable "Developer mode" (toggle in top right)
5. Click "Load unpacked"
6. Select the unpacked folder

### Firefox
Coming soon.

## Usage

1. Open YouTube and sign in to your account
2. Navigate to any YouTube video
3. Click the extension icon
4. Click "Export Cookies.txt"
5. Save the `youtube_cookies.txt` file

## Using with yt-dlp

Upload the cookies file to your server and run:

```bash
yt-dlp --cookies /path/to/youtube_cookies.txt "https://www.youtube.com/watch?v=VIDEO_ID"
```

## Security Warning

- Cookies are session tokens - **don't share them publicly**
- Delete the cookies file after use
- Cookies typically expire within days to weeks

## Format

The exported file is in Netscape format:

```
# Netscape HTTP Cookie File
.youtube.com	TRUE	/	TRUE	1780000000	SID	...
```

## License

MIT