# Torrent Downloaders for Google Colab

Two versions of torrent downloaders for Google Colab with different storage approaches.

## ⚠️ Important Disclaimer

**These tools are for research and educational purposes only.** 

- Use only for legal content and respect copyright laws
- The authors are not responsible for any misuse of these tools
- Users are solely responsible for ensuring compliance with their local laws
- These tools should not be used for downloading copyrighted material without permission

## 📁 Available Versions

### 1. Google Drive Version (`gdrive_torrent_downloader.ipynb`)
- **Storage**: Google Drive (15GB free)
- **Access**: Files saved permanently to your Google Drive
- **Best for**: Smaller files, permanent storage
- **Requires**: Google Drive mounting and authorization

### 2. Session Temporary Version (`session_temporary_torrent_downloader.ipynb`)
- **Storage**: Session temporary storage (~70GB)
- **Access**: Auto-archive into 700MB volumes for download
- **Best for**: Larger files, temporary processing
- **Requires**: No additional authorization

## 🚀 Quick Start

### Google Drive Version
1. Upload `gdrive_torrent_downloader.ipynb` to Google Colab
2. Mount Google Drive when prompted
3. Download torrents directly to Drive
4. Files permanently saved to `/MyDrive/Torrents/`

### Session Temporary Version
1. Upload `session_temporary_torrent_downloader.ipynb` to Google Colab
2. Download torrents to session temporary storage (~70GB)
3. Files auto-archived into 700MB volumes
4. Download archive volumes to your computer

## 📊 Comparison

| Feature | Google Drive Version | Session Temporary Version |
|---------|---------------------|----------------------|
| Storage Size | 15GB | ~70GB |
| File Access | Permanent (Google Drive) | Temporary (download archives) |
| Authorization | Google Drive required | None |
| Large Files | Limited by Drive space | Up to 70GB |
| Archive Support | No | Auto 700MB volumes |
| Speed | Slower (cloud storage) | Faster (session storage) |

## 🛠️ Installation & Usage

### Requirements
- Google Colab (free tier supported)
- Internet connection
- For Google Drive version: Google account with Drive access

## 🔧 Technical Details

### Dependencies
- `libtorrent-rasterbar-dev` (system package)
- `libtorrent` (Python package)
- `p7zip-full` (for Session Temporary version)
- Google Colab environment

### Supported Formats
- Magnet links (`magnet:?xt=urn:btih:...`)
- .torrent files

### Storage Details

#### Google Drive Version
- Files saved directly to Google Drive
- Organized in `/MyDrive/Torrents/` folder
- Automatic folder creation
- 15GB storage limit

#### Session Temporary Version
- Files downloaded to `/content/torrents/`
- Auto-archived to `/content/archives/`
- 700MB archive volumes (.7z format)
- ~70GB session temporary storage available

### Code Structure

```python
# Google Drive Version
class TorrentDownloader:
    def __init__(self, download_path)
    def download_torrent(self, source)
    def list_files(self)

# Session Temporary Version  
class LocalTorrentDownloader:
    def __init__(self, download_path, archive_path)
    def download_torrent(self, source, auto_archive=True)
    def create_archives(self, torrent_name)
    def download_archives(self, archive_name=None)
    def cleanup(self, keep_archives=True)
```

## ⚠️ Limitations

### Both Versions
- Google Colab session timeout (12 hours)
- Network connectivity dependencies
- LibTorrent performance constraints

### Google Drive Version
- 15GB storage limit
- Slower upload speeds to Drive
- Requires Google authorization

### Session Temporary Version
- Files lost when session restarts
- Must download archives before restart
- 2GB individual file download limit

## 🔧 Troubleshooting

### Common Issues
1. **Installation errors**: Restart runtime and re-run installation cell
2. **Drive mount issues** (Google Drive version): Re-authorize Google Drive access
3. **Download stalling**: Check network connection and torrent health
4. **Storage errors**: Verify available space (15GB Drive / 70GB local)
5. **Archive errors** (Session Temporary version): Check 7zip installation

### Performance Tips
- Use healthy torrents with many seeders
- Monitor download progress regularly
- For large files: Use Session Temporary version
- For permanent storage: Use Google Drive version
- Download archives immediately (Session Temporary version)

## Legal Notice

This software is provided "as is" without warranty of any kind. Users must:
- Comply with all applicable laws and regulations
- Respect intellectual property rights
- Use only for legitimate research and educational purposes
- Not use for downloading copyrighted material without permission

## Contributing

This is a research tool. If you find issues or have improvements:
1. Test thoroughly in a research context
2. Ensure compliance with educational use guidelines
3. Document any changes clearly

## License

For educational and research use only. Commercial use prohibited.

---

**Remember**: Always verify that your use case is legal and ethical in your jurisdiction before using this tool.