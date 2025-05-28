# CSV ⇄ SQLite Converter

A powerful, privacy-focused web application for converting between CSV files and SQLite databases. All processing happens locally in your browser - no data is ever sent to external servers.

![CSV SQLite Converter](https://img.shields.io/badge/Privacy-100%25%20Local-green) ![License](https://img.shields.io/badge/License-Open%20Source-blue) ![Browser](https://img.shields.io/badge/Browser-Compatible-orange)

## 🚀 Features

### CSV to SQLite
- **Multi-File Support**: Upload and process multiple CSV files individually
- **Individual File Management**: Preview, select, and manage each processed file separately
- **Selective Combination**: Choose which processed files to combine into your SQLite database
- **Drag & Drop Interface**: Simply drag your CSV files onto the upload area
- **Flexible Parsing**: Support for various delimiters (comma, semicolon, tab, pipe)
- **Smart Type Detection**: Automatically infer column data types
- **Auto Table Naming**: Tables are automatically named based on CSV filenames
- **Header Detection**: Automatically detect if first row contains headers
- **Individual Previews**: Preview each processed file's data independently
- **Progress Tracking**: Real-time processing progress for each file
- **File Replacement**: Re-upload files with the same name to replace previous versions

### SQLite to CSV
- **Database Analysis**: Automatically detect and list all tables in your SQLite file
- **Table Selection**: Choose which table to export
- **Custom Delimiters**: Export with your preferred CSV delimiter
- **Header Options**: Include or exclude column headers
- **Data Preview**: Preview converted data before download
- **Multiple Formats**: Support for .sqlite, .sqlite3, and .db files

## 🔄 Workflow Advantages

### **Individual File Processing**
- Each CSV file is processed and stored independently
- No risk of losing work when adding new files
- Preview and validate each file before including it in your database

### **Selective Combination**
- Choose exactly which files to include in your final database
- Mix and match data sources for different projects
- Create multiple databases from the same collection of processed files

### **Iterative Workflow**
- Upload files as they become available
- Build your database incrementally over time
- Replace outdated files without starting over

### **Quality Control**
- Preview each file's data structure and content
- Remove problematic files without affecting others
- Ensure data quality before creating your final database

## 🔒 Privacy & Security

- **100% Local Processing**: All conversions happen in your browser using WebAssembly
- **No Server Communication**: Your data never leaves your device
- **No Data Storage**: No temporary files or data retention
- **Client-Side Only**: Pure JavaScript/HTML implementation
- **Open Source**: Fully transparent codebase

## 🛠️ Usage

### Converting CSV to SQLite

1. **Upload your CSV files**:
   - Drag and drop one or more CSV files onto the upload area, or
   - Click "Choose CSV Files" to browse and select multiple files

2. **Configure parsing options** (applied to all files):
   - Choose CSV delimiter (comma, semicolon, tab, pipe)
   - Toggle header detection
   - Enable/disable automatic type inference

3. **Individual file processing**:
   - Each CSV file is processed independently and appears in the "Processed CSV Files" list
   - Files are automatically selected for combination by default
   - Monitor processing progress for each file

4. **Manage processed files**:
   - **Preview**: Click the eye icon to view sample data from any processed file
   - **Select/Deselect**: Use checkboxes to choose which files to include in your database
   - **Remove**: Click the trash icon to delete files you no longer need
   - **Replace**: Upload a file with the same name to replace an existing processed file

5. **Combine selected files**:
   - Review which files are selected (checkboxes checked)
   - Click "Combine Selected (X) into SQLite DB" to create your database
   - Each selected CSV becomes a separate table named after its filename

6. **Preview & Download**: 
   - Review the combined database with all selected tables
   - Download the single SQLite database file containing your chosen tables

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
csv-sqlite-html-converter/
├── CSVtoSQLiteDB.html    # Main application file
└── README.md             # This documentation
```

## 🚀 Getting Started

### Local Development

1. **Clone the repository**:
   ```bash
   git clone https://github.com/npcraig/csv-sqlite-html-converter.git
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
- **File Management**: Individual file controls with preview, selection, and deletion
- **Accessibility**: Proper ARIA labels and keyboard navigation

### Data Processing
- **Individual File Processing**: Each CSV is parsed and stored independently
- **Robust CSV Parsing**: Handles quoted fields, escaped characters, and edge cases
- **Type Inference**: Automatically detects numbers, dates, and text
- **Error Handling**: Comprehensive error messages and recovery per file
- **Memory Efficient**: Streaming processing for large files
- **File Replacement**: Smart handling of duplicate filenames

### Export Options
- **Selective Combination**: Choose which processed files to include in the final database
- **SQLite Compatibility**: Standard SQLite format compatible with all SQLite tools
- **CSV Standards**: RFC 4180 compliant CSV output
- **Auto Table Naming**: Tables named based on source filenames with sanitization
- **Format Preservation**: Maintains data integrity during conversion
- **Multiple Outputs**: Create different databases from the same processed files

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Report Issues**: Found a bug? [Open an issue](https://github.com/npcraig/csv-sqlite-html-converter/issues)
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

- **Data Analysis**: Process multiple CSV datasets and selectively combine relevant ones for SQL queries
- **Data Curation**: Upload various CSV files, preview each one, and choose only the ones you need
- **Iterative Database Building**: Add CSV files over time and combine them when your dataset is complete
- **Data Quality Control**: Preview individual files before including them in your final database
- **Selective Data Migration**: Choose specific data sources from a collection of CSV files
- **Project-Based Organization**: Process files individually, then create project-specific databases
- **Database Development**: Create test databases from curated CSV data sources
- **Data Archival**: Convert selected CSVs to compact SQLite format for long-term storage
- **Report Generation**: Extract specific tables from databases back to CSV
- **Multi-Source Integration**: Combine data from different sources with full control over inclusion

## 🔧 Troubleshooting

### Common Issues

**Files not appearing in the processed list?**
- Check that files have .csv extension
- Ensure files are not empty or corrupted
- Try uploading files one at a time to identify problematic ones

**Can't see individual file preview?**
- Click the eye icon next to the file name
- Check that the file processed successfully (no error status)
- Try refreshing the page if previews aren't loading

**Combine button disabled?**
- Ensure at least one file is selected (checkbox checked)
- Check that files have been processed successfully
- Verify files appear in the processed files list

**File replacement not working?**
- Make sure the new file has exactly the same name as the original
- Check that the file is a valid CSV format
- The old file should be automatically replaced in the list

**Conversion failing?**
- Verify CSV format is valid for each file
- Check for unusual characters or encoding issues in individual files
- Try different delimiter settings
- Use individual file previews to identify problematic data

**Large file performance?**
- Process files individually to identify performance bottlenecks
- Use modern browser with sufficient RAM
- Close other browser tabs
- Consider splitting very large files

**Download not working?**
- Ensure at least one file is selected for combination
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