# Universal Social Media Downloader

A Flask-based web application to download videos, reels, stories, posts, and more from popular social media platforms like YouTube, Instagram, TikTok, Twitter/X, Facebook, Reddit, and others.

## Features

- **Auto platform detection** from URL
- Download from:
  - YouTube (videos, shorts, playlists)
  - Instagram (posts, reels, stories, IGTV)
  - TikTok
  - Twitter/X
  - Facebook
  - Reddit
  - Many other platforms supported via [yt-dlp](https://github.com/yt-dlp/yt-dlp)
- **Bulk download** support
- Download folders as ZIP files
- List and clear downloaded files
- Subtitle and metadata download (where available)

## Requirements

- Python 3.8+
- [yt-dlp](https://github.com/yt-dlp/yt-dlp)
- [instaloader](https://github.com/instaloader/instaloader)
- Flask
- requests

Install dependencies:
```sh
pip install flask yt-dlp instaloader requests
```

## Usage

1. **Clone the repository:**
    ```sh
    git clone https://github.com/BorudePiyush/LINK-to-video-Downloader.git
    cd LINK-to-video-Downloader
    ```

2. **Run the app:**
    ```sh
    python app.py
    ```

3. **Open your browser and go to:**
    ```
    http://localhost:5000
    ```

4. **Paste a social media URL and download!**

## API Endpoints

- `POST /download`  
  Download a single URL.  
  **Body:** `{ "url": "<media-url>" }`

- `POST /bulk-download`  
  Download multiple URLs.  
  **Body:** `{ "urls": ["<url1>", "<url2>", ...] }`

- `GET /downloads`  
  List downloaded files and folders.

- `GET /download-file/<filename>`  
  Download a specific file.

- `GET /download-folder/<foldername>`  
  Download a folder as a ZIP file.

- `POST /clear-downloads`  
  Delete all downloaded files.

- `GET /supported-platforms`  
  List supported platforms and features.

## Notes

- Downloaded files are saved in the `downloads/` directory.
- For Instagram downloads, you may need to log in or provide credentials for private content.
- This tool is for educational and personal use only. Please respect the terms of service of each platform.

## License

MIT License

---

**Author:**
