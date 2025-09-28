# CSV Transaction Sanitizer

A simple, elegant web application that sanitizes CSV files by converting transaction names from ALL CAPS to proper sentence case. Perfect for cleaning up financial transaction data exported from banks and financial institutions.

## 🚀 Features

- **Drag & Drop Interface**: Simply drag your CSV file onto the upload area
- **Smart Sanitization**: Converts ALL CAPS transaction names to proper sentence case
- **Real-time Processing**: See progress as your file is processed
- **Instant Download**: Get your sanitized CSV file immediately
- **Mobile Responsive**: Works perfectly on desktop and mobile devices
- **No Data Upload**: All processing happens in your browser - your data never leaves your device

## 📋 How It Works

The application specifically targets the **first column** of your CSV file (typically the transaction description) and:

1. Converts ALL CAPS text to sentence case
2. Preserves special characters, numbers, and punctuation
3. Maintains proper formatting for contractions and possessives
4. Keeps all other columns unchanged

### Example Transformations

| Before (ALL CAPS) | After (Sentence Case) |
|------------------|----------------------|
| `WALMART SUPERCENTER` | `Walmart Supercenter` |
| `AMAZON.COM PURCHASE` | `Amazon.com Purchase` |
| `SHELL GAS STATION #123` | `Shell Gas Station #123` |
| `MCDONALD'S #4567` | `Mcdonald's #4567` |
| `ATM WITHDRAWAL FEE` | `Atm Withdrawal Fee` |

## 🖥️ Usage

1. **Open the Application**: Navigate to the GitHub Pages URL
2. **Upload Your CSV**: 
   - Drag and drop your CSV file onto the upload area, OR
   - Click "Choose File" to select your CSV file
3. **Process**: Click the "Sanitize CSV" button
4. **Download**: Once processing is complete, click "Download Sanitized CSV"

## 🚀 Deployment to GitHub Pages

### Method 1: Direct Upload

1. Create a new repository on GitHub
2. Upload the `index.html` file to the repository
3. Go to repository Settings → Pages
4. Select "Deploy from a branch" and choose `main` branch
5. Your site will be available at `https://yourusername.github.io/repository-name`

### Method 2: Git Commands

```bash
# Initialize git repository (if not already done)
git init

# Add your files
git add .

# Commit your changes
git commit -m "Initial commit: CSV Transaction Sanitizer"

# Add your GitHub repository as remote
git remote add origin https://github.com/yourusername/csv-sanitize.git

# Push to GitHub
git branch -M main
git push -u origin main
```

Then enable GitHub Pages in your repository settings.

## 📁 File Structure

```
csv-sanitize/
├── index.html          # Main application file
├── README.md          # This file
└── .cursorindexignore # Editor configuration (optional)
```

## 🛠️ Technical Details

### Technologies Used
- **HTML5**: Modern semantic markup
- **CSS3**: Responsive design with gradients and animations
- **Vanilla JavaScript**: No external dependencies
- **File API**: For reading uploaded files
- **Blob API**: For generating downloadable files

### Browser Support
- Chrome 50+
- Firefox 52+
- Safari 10+
- Edge 79+

### CSV Processing
- Handles quoted fields with commas
- Preserves empty cells
- Maintains row structure
- Processes files of reasonable size (tested up to 10MB)

## 🔒 Privacy & Security

- **Client-Side Only**: All processing happens in your browser
- **No Data Upload**: Your CSV files never leave your device
- **No Tracking**: No analytics or tracking scripts
- **Open Source**: Full source code available for review

## 🐛 Troubleshooting

### Common Issues

**File not processing?**
- Ensure your file has a `.csv` extension
- Check that the file isn't corrupted
- Try refreshing the page and uploading again

**Unexpected results?**
- The tool processes the first column only
- Complex CSV structures with nested quotes may need manual review
- Very large files (>50MB) may cause browser performance issues

**Download not working?**
- Ensure your browser allows file downloads
- Check if popup blockers are interfering
- Try using a different browser

## 📝 Sample CSV Format

Your CSV should look something like this:

```csv
Transaction Description,Date,Amount,Category
WALMART SUPERCENTER,2023-12-01,-45.67,Groceries
AMAZON.COM PURCHASE,2023-12-02,-23.99,Shopping
SHELL GAS STATION #123,2023-12-03,-35.00,Transportation
```

After processing:

```csv
Transaction Description,Date,Amount,Category
Walmart Supercenter,2023-12-01,-45.67,Groceries
Amazon.com Purchase,2023-12-02,-23.99,Shopping
Shell Gas Station #123,2023-12-03,-35.00,Transportation
```

## 🤝 Contributing

Feel free to fork this project and submit pull requests for improvements. Some ideas for enhancements:

- Support for different column selections
- Multiple sanitization rules
- Batch processing of multiple files
- Export to different formats (Excel, etc.)
- Custom transformation rules

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🔗 Links

- **Live Demo**: [Your GitHub Pages URL here]
- **Repository**: [Your GitHub repository URL here]
- **Issues**: Report bugs and request features in the GitHub Issues section

---

Made with ❤️ for cleaner financial data
