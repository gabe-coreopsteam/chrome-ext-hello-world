# Hello World Chrome Extension

A simple "Hello World" Chrome extension built to understand the fundamentals of Chrome extension development. This project serves as a learning foundation for building more complex extensions.

## 🎯 Learning Objectives

This project demonstrates:
- Chrome Extension Manifest V3 structure
- Basic popup functionality
- Modern UI design principles for extensions
- Proper Chrome extension development workflow

## 📁 Project Structure

```
hello_world_chrome_ext/
├── manifest.json    # Extension configuration and metadata
├── popup.html       # Popup UI with styling
├── README.md        # This documentation
└── LICENSE          # MIT License
```

## 🚀 Getting Started

### Prerequisites
- Google Chrome browser
- Basic understanding of HTML/CSS
- Text editor or IDE

### Installation Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/gabe-coreopsteam/chrome-ext-hello-world.git
   cd chrome-ext-hello-world
   ```

2. **Load the extension in Chrome:**
   - Open Chrome and navigate to `chrome://extensions/`
   - Enable "Developer mode" (toggle in the top right corner)
   - Click "Load unpacked" button
   - Select the `hello_world_chrome_ext` folder
   - The extension should now appear in your extensions list

3. **Test the extension:**
   - Look for the extension icon in your Chrome toolbar
   - Click the icon to see the "Hello World" popup
   - The popup should display with a gradient background and welcome message

## 📋 Files Explained

### manifest.json
The extension's configuration file using Manifest V3:

```json
{
    "manifest_version": 3,
    "name": "Hello World Extension",
    "version": "1.0",
    "description": "A simple Hello World Chrome extension",
    "action": {
      "default_popup": "popup.html"
    },
    "permissions": []
}
```

**Key Points:**
- `manifest_version: 3` - Uses the latest Chrome extension format
- `action` - Defines the popup behavior (replaces `browser_action` from V2)
- `permissions: []` - No special permissions needed for this basic extension

### popup.html
The UI that appears when clicking the extension icon:

- **Responsive Design**: Fixed 300px width for consistent appearance
- **Modern Styling**: Gradient background with clean typography
- **User Feedback**: Clear confirmation that the extension is working

## 🔄 Manifest V2 vs V3 Migration

This project was initially built with Manifest V2 but updated to V3. Key changes made:

| Manifest V2 | Manifest V3 | Reason |
|-------------|-------------|---------|
| `"manifest_version": 2` | `"manifest_version": 3` | V2 is deprecated |
| `"browser_action"` | `"action"` | API consolidation |
| Background pages | Service workers | Better performance |

## 🛠️ Troubleshooting

### Common Issues:

1. **"Unsupported manifest version" error**
   - Ensure `manifest_version` is set to `3`
   - Check that `browser_action` is changed to `action`

2. **Extension not loading**
   - Verify all file paths are correct
   - Check Chrome Developer Console for errors
   - Ensure Developer mode is enabled

3. **Popup not displaying**
   - Confirm `popup.html` exists in the root directory
   - Check for HTML syntax errors
   - Verify the popup dimensions in CSS

## 📚 Next Steps for Learning

After mastering this basic extension, consider exploring:

1. **Content Scripts**: Interact with web pages
   ```json
   "content_scripts": [{
     "matches": ["<all_urls>"],
     "js": ["content.js"]
   }]
   ```

2. **Background Service Workers**: Handle events and maintain state
   ```json
   "background": {
     "service_worker": "background.js"
   }
   ```

3. **Storage API**: Persist user data
   ```json
   "permissions": ["storage"]
   ```

4. **Host Permissions**: Access specific websites
   ```json
   "host_permissions": ["https://example.com/*"]
   ```

## 🤝 Contributing

This is an educational project! Feel free to:
- Fork and experiment
- Submit improvements via pull requests
- Report issues or suggest enhancements
- Use as a template for your own learning projects

## 📖 Additional Resources

- [Chrome Extension Developer Guide](https://developer.chrome.com/docs/extensions/)
- [Manifest V3 Migration Guide](https://developer.chrome.com/docs/extensions/migrating/)
- [Chrome Extension Samples](https://github.com/GoogleChrome/chrome-extensions-samples)
- [Extension API Reference](https://developer.chrome.com/docs/extensions/reference/)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙋‍♂️ Questions?

If you're learning Chrome extension development and have questions about this project, feel free to open an issue in the repository!

---

**Happy Extension Building! 🚀**
