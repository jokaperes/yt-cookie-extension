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

## Usage (recommended: incognito, so cookies don't keep expiring)

YouTube rotates the cookies of any session that stays open in a browser, which is
why exported cookies often stop working within hours. The fix is to export from a
throwaway session that you close immediately and never touch again:

1. Go to `chrome://extensions`, open this extension's details and enable **Allow in Incognito**
2. Open an incognito window and sign in with a **spare YouTube account** (not your main one)
3. Navigate to `https://www.youtube.com/robots.txt`
4. Click the extension icon and click "Export Cookies.txt" — when an incognito window is open, the extension exports its cookies automatically
5. Save `youtube_cookies.txt`, then **close the incognito window**
6. Never log in with that account in a browser again — yt-dlp can keep using the cookies for months

### Quick export (normal profile)

You can also just sign in to YouTube normally and click "Export Cookies.txt", but
expect the cookies to be rotated quickly while you keep using YouTube in that browser.

## Using with yt-dlp

Upload the cookies file to your server and run:

```bash
yt-dlp --cookies /path/to/youtube_cookies.txt "https://www.youtube.com/watch?v=VIDEO_ID"
```

## Security Warning

- Cookies are session tokens - **don't share them publicly**
- Delete the cookies file after use
- Cookies exported from an active browser session are rotated quickly; cookies exported from a closed incognito session of a spare account last much longer

## Format

The exported file is in Netscape format:

```
# Netscape HTTP Cookie File
.youtube.com	TRUE	/	TRUE	1780000000	SID	...
```

## License

MIT