# yt-cookie-extension

See `README.md` for what the extension does and how to use it.

## Operational notes

- Chrome/Edge extension that exports YouTube cookies in Netscape format for yt-dlp. Companion of `/root/yt-transcript`.
- Working branch: `main`. Private repo `jokaperes/yt-cookie-extension`. Always commit AND push.
- `/root/yt-cookie-extension-pack/` is a mirror used only as release-zip staging — do not develop there; replicate changes from here.
- yt-dlp (yt-transcript engine >= 2.3.3) rotates the cookies and writes them back to the file. When cookies burn out, the fix is re-exporting from an incognito window with a spare account using extension v1.1.
