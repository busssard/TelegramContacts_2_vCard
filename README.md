# TelegramContacts_2_vCard# 📱 Telegram to vCard Converter

A simple, single-file web application that converts Telegram contact exports to vCard format (.vcf) for easy import into any contact management system.

## 🚀 Usage

1. **Export your Telegram contacts**
   - Open Telegram Desktop
   - Go to Settings → Advanced → Export Telegram Data
   - Select "Contact list" and export as JSON

2. **Convert to vCard**
   - Open `telegram-vcard-converter.html` in your browser
   - Drop the JSON file or paste its contents
   - Click "Convert to vCard"
   - Review the contacts
   - Click "Download vCard File"

3. **Import contacts**
   - Import the downloaded `.vcf` file into yourr contact management app

## 📋 Expected JSON Format

The converter expects Telegram's standard export format:

```json
{
  "about": "...",
  "contacts": {
    "about": "...",
    "list": [
      {
        "first_name": "John",
        "last_name": "Doe",
        "phone_number": "+1234567890",
        "date": "2023-01-15T10:30:00"
      }
    ]
  }
}
```

## 🔧 Technical Details

**Generated vCard Format:**
- Version: vCard 3.0
- Fields included: Name (FN, N), Phone (TEL), Notes (with original date)
- Character encoding: UTF-8
- Line breaks: CRLF (standard vCard format)

**Browser Compatibility:**
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Any modern browser with ES6 support

## 📦 Installation

No installation or internet needed!
Its completely local, just using the browser as User INterface
Just download or save the HTML file and open it in your browser.

## 🛡️ Privacy & Security

- **100% Client-Side** - No data is sent to any server
- **No Tracking** - No analytics or external scripts
- **Offline Capable** - Works without internet connection
- **Open Source** - Review the code yourself

## 🤝 Contributing

Since this is a single-file application, improvements are welcome:

1. Suggest features via issues
2. Submit pull requests with enhancements
3. Report bugs or edge cases

## 📝 License

This project is provided as-is for non-commercial personal use.

## 🔍 Troubleshooting

**"Invalid JSON format" error:**
- Ensure you've exported the complete Telegram data
- Check that the JSON structure matches the expected format
- Verify the file isn't corrupted

**Contacts not appearing:**
- Make sure contacts have phone numbers
- Check that the `contacts.list` array exists
- Verify the JSON is properly formatted

**Download not working:**
- Check your browser's download settings
- Ensure pop-ups aren't blocked
- Try a different browser

## 🌟 Use Cases

- Switching from Telegram to a different messaging app
- Backing up Telegram contacts
- Syncing Telegram contacts with your phone's contact list
- Migrating contacts to a new device
- Creating a backup of important contact information

## 💡 Tips

- The app preserves the original date when the contact was added (stored in the Notes field)
- Contacts without phone numbers are automatically skipped
- The generated vCard file can contain hundreds of contacts in a single file
- You can edit the generated vCard with any text editor before importing

## 📧 Contact & Support

For questions, issues, or suggestions, please open an issue on the project repository.

---

Made with ❤️ for the Telegram community
