# CSV ⇄ SQLite Converter

A powerful, privacy-focused web application for converting between CSV files and SQLite databases. All processing happens locally in your browser - no data is ever sent to external servers.

![CSV SQLite Converter](https://img.shields.io/badge/Privacy-100%25%20Local-green) ![License](https://img.shields.io/badge/License-Open%20Source-blue) ![Browser](https://img.shields.io/badge/Browser-Compatible-orange)

## 🚀 Features

### CSV to SQLite
- **Drag & Drop Interface**: Simply drag your CSV files onto the upload area
- **Flexible Parsing**: Support for various delimiters (comma, semicolon, tab, pipe)
- **Smart Type Detection**: Automatically infer column data types
- **Custom Table Names**: Specify your preferred table name
- **Header Detection**: Automatically detect if first row contains headers
- **Live Preview**: See your data before downloading
- **Progress Tracking**: Real-time conversion progress

### SQLite to CSV
- **Database Analysis**: Automatically detect and list all tables in your SQLite file
- **Table Selection**: Choose which table to export
- **Custom Delimiters**: Export with your preferred CSV delimiter
- **Header Options**: Include or exclude column headers
- **Data Preview**: Preview converted data before download
- **Multiple Formats**: Support for .sqlite, .sqlite3, and .db files

## 🔒 Privacy & Security

- **100% Local Processing**: All conversions happen in your browser using WebAssembly
- **No Server Communication**: Your data never leaves your device
- **No Data Storage**: No temporary files or data retention
- **Client-Side Only**: Pure JavaScript/HTML implementation
- **Open Source**: Fully transparent codebase

## 🛠️ Usage

### Converting CSV to SQLite

1. **Upload your CSV file**:
   - Drag and drop your CSV file onto the upload area, or
   - Click "Choose CSV File" to browse and select

2. **Configure options** (optional):
   - Set table name (default: "data")
   - Choose CSV delimiter
   - Toggle header detection
   - Enable/disable automatic type inference

3. **Convert**: The conversion starts automatically after file upload

4. **Preview & Download**: Review your data and download the SQLite database

### Converting SQLite to CSV

1. **Upload your SQLite file**:
   - Drag and drop your .sqlite/.sqlite3/.db file, or
   - Click "Choose SQLite File" to browse

2. **Select table**: Choose which table to export from the dropdown

3. **Configure options**:
   - Choose output CSV delimiter
   - Include/exclude headers

4. **Convert**: Click "Convert to CSV"

5. **Download**: Preview and download your CSV file

## 🏗️ Technical Details

### Dependencies
- **SQL.js**: WebAssembly port of SQLite for browser usage
- **Font Awesome**: Icons for the user interface
- **Google Fonts (Inter)**: Modern typography

### Browser Compatibility
- Chrome 57+
- Firefox 52+
- Safari 11+
- Edge 16+

### File Size Limits
- Recommended: Files under 100MB for optimal performance
- Maximum: Limited by browser memory (typically 1-2GB)

## 📁 Project Structure

```
csv-sqlite-html/
├── CSVtoSQLiteDB.html    # Main application file
└── README.md             # This documentation
```

## 🚀 Getting Started

### Local Development

1. **Clone the repository**:
   ```bash
   git clone https://github.com/npcraig/csv-sqlite-html.git
   ```

2. **Open in browser**:
   - Simply open `CSVtoSQLiteDB.html` in your web browser
   - No build process or server required!

### Deployment

The application is a single HTML file that can be:
- Hosted on any web server
- Opened directly from filesystem
- Deployed to static hosting services (GitHub Pages, Netlify, etc.)

## 🎨 Features in Detail

### User Interface
- **Responsive Design**: Works on desktop, tablet, and mobile
- **Modern Styling**: Clean, professional interface with smooth animations
- **Intuitive Navigation**: Clear visual feedback and progress indicators
- **Accessibility**: Proper ARIA labels and keyboard navigation

### Data Processing
- **Robust CSV Parsing**: Handles quoted fields, escaped characters, and edge cases
- **Type Inference**: Automatically detects numbers, dates, and text
- **Error Handling**: Comprehensive error messages and recovery
- **Memory Efficient**: Streaming processing for large files

### Export Options
- **SQLite Compatibility**: Standard SQLite format compatible with all SQLite tools
- **CSV Standards**: RFC 4180 compliant CSV output
- **Custom Naming**: User-defined table and file names
- **Format Preservation**: Maintains data integrity during conversion

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Report Issues**: Found a bug? [Open an issue](https://github.com/npcraig/csv-sqlite-html/issues)
2. **Feature Requests**: Have an idea? Let us know!
3. **Pull Requests**: Submit improvements or fixes
4. **Documentation**: Help improve this README or add examples

### Development Guidelines
- Maintain the single-file architecture
- Ensure all processing remains client-side
- Test with various CSV formats and SQLite databases
- Follow existing code style and conventions

## 📝 License

This project is open source. See the repository for license details.

## 🙏 Acknowledgments

- **SQL.js Team**: For the amazing WebAssembly SQLite port
- **SQLite**: For the robust database engine
- **Font Awesome**: For the beautiful icons
- **Community**: For feedback and contributions

## 📊 Use Cases

- **Data Analysis**: Convert CSV data to SQLite for SQL queries
- **Data Migration**: Move between different data formats
- **Database Development**: Create test databases from CSV data
- **Data Archival**: Convert CSVs to compact SQLite format
- **Report Generation**: Extract specific tables from databases
- **Data Sharing**: Convert databases to universally readable CSV

## 🔧 Troubleshooting

### Common Issues

**File not uploading?**
- Check file extension (.csv for CSV, .sqlite/.sqlite3/.db for SQLite)
- Ensure file is not corrupted
- Try with a smaller file first

**Conversion failing?**
- Verify CSV format is valid
- Check for unusual characters or encoding issues
- Try different delimiter settings

**Large file performance?**
- Use modern browser with sufficient RAM
- Close other browser tabs
- Consider splitting very large files

**Download not working?**
- Check browser download settings
- Ensure pop-ups are not blocked
- Try right-clicking and "Save As"

## 📈 Performance Tips

- **Large Files**: Process files under 100MB for best performance
- **Memory Usage**: Close other applications when processing large datasets
- **Browser Choice**: Chrome and Firefox generally offer best performance
- **File Format**: SQLite files are typically much smaller than equivalent CSVs

---

**Made with ❤️ for data enthusiasts who value privacy and simplicity.** 