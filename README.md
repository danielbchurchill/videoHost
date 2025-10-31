# Video Host

A minimal video hosting site that displays videos in fullscreen with autoplay functionality. Perfect for QR code sharing and instant video playback.

## Features

- 🎥 **Fullscreen Video Player**: Automatically fills the entire viewport
- ▶️ **Autoplay**: Video starts playing immediately on load  
- 📱 **Mobile Optimized**: Works perfectly on all devices
- 🚀 **Ultra Minimal**: Only 13 lines of HTML/CSS code
- ⚡ **Fast Loading**: No dependencies, pure HTML

## Setup

1. **Add your video file** to `src/videos/` directory
2. **Update the video path** in `index.html` to match your video file name
3. **Start a local server**:
   ```bash
   python3 -m http.server 8080
   ```
4. **Access your video** at `http://localhost:8080`

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

## Supported Video Formats

- MP4 (recommended)
- WebM
- MOV
- OGV

## Note on Large Files

Video files are excluded from git commits due to GitHub's file size limits. For production deployment, consider using:

- YouTube (embed)
- Vimeo (embed) 
- AWS S3
- Google Cloud Storage
- Any CDN service

## Browser Support

✅ All modern browsers including mobile Safari, Chrome, Firefox, and Edge.

## License

MIT License - Use freely for any purpose.