# Video Host

A minimal video hosting site that displays YouTube videos in fullscreen with autoplay functionality. Perfect for QR code sharing and instant video playback.

## Features

- 🎥 **Fullscreen YouTube Player**: Automatically fills the entire viewport
- ▶️ **Autoplay**: Video starts playing immediately on load (muted for browser compliance)
- 📱 **Mobile Optimized**: Works perfectly on all devices
- 🚀 **Ultra Minimal**: Only 11 lines of HTML/CSS code
- ⚡ **Fast Loading**: Uses YouTube's CDN for optimal performance
- 🌐 **No File Size Limits**: Host any length video via YouTube

## Setup

1. **Upload your video to YouTube**
2. **Get the video ID** from the YouTube URL (e.g., `36jV4vA3QwQ` from `https://www.youtube.com/watch?v=36jV4vA3QwQ`)
3. **Update the video ID** in `index.html` in the iframe src
4. **Start a local server**:
   ```bash
   python3 -m http.server 8080
   ```
5. **Access your video** at `http://localhost:8080`

## For QR Code Sharing

1. Find your local IP address:
   ```bash
   ifconfig | grep "inet " | grep -v 127.0.0.1
   ```
2. Share the URL: `http://[your-ip]:8080`
3. Generate a QR code pointing to this URL
4. Anyone scanning the QR code will instantly see your video

## Deployment

### GitHub Pages (Free)
1. Push your code to GitHub (excluding video files)
2. Upload your video to a cloud storage service
3. Update the video `src` path in `index.html`
4. Enable GitHub Pages in repository settings

### Netlify/Vercel (Free)
1. Connect your GitHub repository
2. Upload video files to cloud storage
3. Update video paths accordingly
4. Deploy automatically

## File Structure

```
videoHost/
├── index.html          # Minimal video player
├── .gitignore         # Excludes large video files
└── src/
    └── videos/
        └── your-video.mp4  # Your video file (not in git)
```

## Supported Video Sources

- ✅ **YouTube** (current implementation)
- ✅ **Vimeo** (change embed URL)
- ✅ **Any video hosting service with embed support**

## YouTube Embed Parameters

The current setup includes these YouTube parameters for optimal experience:
- `autoplay=1` - Starts playing automatically
- `mute=1` - Required for autoplay in most browsers
- `controls=1` - Shows video controls
- `rel=0` - Reduces related video suggestions
- `modestbranding=1` - Minimal YouTube branding

## Note on Autoplay

Due to browser policies, videos with sound cannot autoplay. The video starts muted and users can unmute manually. This ensures compatibility across all browsers and devices.

## Browser Support

✅ All modern browsers including mobile Safari, Chrome, Firefox, and Edge.

## License

MIT License - Use freely for any purpose.