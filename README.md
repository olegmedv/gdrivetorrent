# Universal Torrent Downloader for Google Colab

Fully automated torrent downloader with universal archive system for Google Colab.

## ⚠️ Important Disclaimer

**These tools are for research and educational purposes only.** 

- Use only for legal content and respect copyright laws
- The authors are not responsible for any misuse of these tools
- Users are solely responsible for ensuring compliance with their local laws
- These tools should not be used for downloading copyrighted material without permission

## 🎯 Universal System Features

- **🔄 Fully Automated**: Download → Archive → Download to computer
- **📁 Universal Folder**: All downloads go to `/content/downloads_torrent/`
- **📦 Auto-Archiving**: Creates 700MB volumes with timestamps
- **⬇️ Auto-Download**: Archives download to your computer automatically
- **🚀 70GB Storage**: Session temporary storage (~70GB available)
- **🔧 No Dependencies**: No Google Drive authorization needed

## 🚀 Quick Start

### Universal System (`session_temporary_torrent_downloader.ipynb`)
1. Upload `session_temporary_torrent_downloader.ipynb` to Google Colab
2. Run setup cells (install dependencies, create folders)
3. Upload torrent file in Section 4
4. **Everything happens automatically**:
   - Downloads to `/content/downloads_torrent/`
   - Archives into 700MB volumes
   - Downloads archives to your computer

### Legacy Google Drive Version (`gdrive_torrent_downloader.ipynb`)
- **Deprecated**: Use universal system instead
- Limited to 15GB storage
- Requires Google Drive authorization

## 🎯 Universal System Workflow

```
1. Upload torrent file
   ↓
2. Auto-download to /content/downloads_torrent/
   ↓
3. Auto-archive into 700MB volumes (torrent_archive_TIMESTAMP.7z.001, .002, etc.)
   ↓
4. Auto-download all volumes to your computer
   ↓
5. Extract with 7zip/WinRAR
```

### Advantages
- **Fully automated**: No manual steps needed
- **Universal**: Works with any torrent, no name dependencies  
- **Large capacity**: 70GB vs 15GB Google Drive
- **Fast**: Local storage performance
- **Simple**: One workflow for everything

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

#### Universal System
- **Download folder**: `/content/downloads_torrent/` (all torrents go here)
- **Archive folder**: `/content/archives/` (700MB volumes created here)
- **Archive format**: `torrent_archive_TIMESTAMP.7z.001`, `.002`, etc.
- **Storage capacity**: ~70GB session temporary storage
- **Auto-cleanup**: Files lost when session restarts (archives downloaded first)

### Code Structure

```python
# Universal System
class UniversalTorrentDownloader:
    def __init__(self, downloads_path, archive_path)
    def download_torrent(self, source, auto_archive=True, auto_download=True)
    def create_archives_from_downloads(self)  # Archives everything in downloads folder
    def download_all_archives(self)           # Downloads all archive volumes
    def list_downloads(self)                  # Shows files in downloads folder
    def list_archives(self)                   # Shows created archives
    def cleanup(self, keep_archives=True)
```

## ⚠️ Limitations

### Universal System
- **Session timeout**: 12 hours maximum (Google Colab limitation)
- **File loss**: Files lost when session restarts (archives downloaded automatically)
- **Download limit**: 2GB per individual archive volume via Colab
- **Network dependency**: Requires stable internet connection
- **LibTorrent constraints**: Performance depends on torrent health/seeders

### Legacy Google Drive Version (Deprecated)
- 15GB storage limit
- Slower performance
- Requires Google authorization

## 🔧 Troubleshooting

### Common Issues
1. **Installation errors**: Restart runtime and re-run installation cell
2. **Drive mount issues** (Google Drive version): Re-authorize Google Drive access
3. **Download stalling**: Check network connection and torrent health
4. **Storage errors**: Verify available space (15GB Drive / 70GB local)
5. **Archive errors** (Session Temporary version): Check 7zip installation

### Performance Tips
- **Use healthy torrents**: Choose torrents with many seeders
- **Monitor progress**: Check download status regularly  
- **Large files**: Universal system handles up to 70GB
- **Session management**: Archives download automatically, no manual intervention needed
- **Network stability**: Ensure stable internet for best performance

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