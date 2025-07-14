# Google Drive Torrent Downloader

A Google Colab notebook for downloading torrents directly to Google Drive using LibTorrent.

## ⚠️ Important Disclaimer

**This tool is for research and educational purposes only.** 

- Use only for legal content and respect copyright laws
- The authors are not responsible for any misuse of this tool
- Users are solely responsible for ensuring compliance with their local laws
- This tool should not be used for downloading copyrighted material without permission

## Features

- Download torrents directly to Google Drive
- Support for both magnet links and .torrent files
- Real-time progress monitoring
- File listing and organization
- Automatic Google Drive integration
- Easy-to-use interface in Google Colab

## Requirements

- Google account with Google Drive access
- Google Colab (free tier supported)
- Internet connection

## Installation & Usage

1. **Open the notebook**: Upload `gdrive_torrent_downloader.ipynb` to Google Colab
2. **Run installation cell**: Install LibTorrent dependencies
3. **Mount Google Drive**: Authorize access to your Google Drive
4. **Use the downloader**: 
   - For magnet links: Paste the magnet URL
   - For .torrent files: Upload the file to Colab
5. **Monitor progress**: Watch real-time download status
6. **Access files**: Files are saved to `/content/drive/MyDrive/Torrents/`

## Technical Details

### Dependencies
- `libtorrent-rasterbar-dev` (system package)
- `libtorrent` (Python package)
- Google Colab environment

### Supported Formats
- Magnet links (`magnet:?xt=urn:btih:...`)
- .torrent files

### Storage
- Files are saved directly to Google Drive
- Organized in `/MyDrive/Torrents/` folder
- Automatic folder creation

## Code Structure

```python
class TorrentDownloader:
    def __init__(self, download_path)     # Initialize with download path
    def download_torrent(self, source)    # Download from magnet/file
    def list_files(self)                  # List downloaded files
```

## Limitations

- Google Colab session timeout (12 hours)
- Google Drive storage limits
- Network connectivity dependencies
- LibTorrent performance constraints

## Troubleshooting

### Common Issues
1. **Installation errors**: Restart runtime and re-run installation cell
2. **Drive mount issues**: Re-authorize Google Drive access
3. **Download stalling**: Check network connection and torrent health
4. **Storage errors**: Verify available Google Drive space

### Performance Tips
- Use healthy torrents with many seeders
- Monitor download progress regularly
- Consider splitting large downloads across sessions

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