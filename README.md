# Unfuck Email - Filters

🧹 **Clean up your inbox automatically!** These email filters help organize promotional emails, newsletters, and spam by automatically archiving emails that contain unsubscribe links and promotional language.

---

## 🚀 Quick Start (Recommended)

### Download Pre-built Filters

The easiest way to use these filters is to download the pre-built XML files from our [latest release](https://github.com/stevenirby/unfuckemail/releases/latest):

1. **For Gmail users**: Download [`gmailFilters.xml`](https://github.com/stevenirby/unfuckemail/releases/latest/download/gmailFilters.xml)
2. **For Fastmail users**: Download [`fastmailFilters.xml`](https://github.com/stevenirby/unfuckemail/releases/latest/download/fastmailFilters.xml)

### Import the Filters

#### Gmail
1. Open [Gmail Settings > Filters and Blocked Addresses](https://mail.google.com/mail/u/0/#settings/filters)
2. Click "Import filters"
3. Upload the `gmailFilters.xml` file you downloaded
4. Review and apply the filters

#### Fastmail
1. Open [Fastmail Settings > Rules](https://app.fastmail.com/settings/filters)
2. Click "Import"
3. Upload the `fastmailFilters.xml` file you downloaded
4. Review and apply the rules

## 🎯 What These Filters Do

These filters automatically **archive** emails that contain common promotional and unsubscribe language, including:

- "Unsubscribe" links and text
- "Email Preferences" and "Manage Subscriptions"
- "This is a promotional email"
- "Opt out" language
- And many more patterns

All filtered emails are labeled as `_Archive` (Gmail) or `Archive` (Fastmail) so you can still find them if needed.

## 🛠️ Advanced Usage

### For Developers: Building From Source

If you want to modify the filters or build them yourself:

#### Prerequisites
```bash
# macOS
brew install pipx
pipx install gmail-yaml-filters

# Or using pip
pip install gmail-yaml-filters
```

#### Build Custom Filters
1. Clone this repository or download `filters.yml`
2. Modify `filters.yml` to add/remove filter rules
3. Generate the XML files:

```bash
# For Gmail
gmail-yaml-filters --dry-run filters.yml > gmailFilters.xml

# For Fastmail (replaces _Archive with Archive)
sed 's/_Archive/Archive/g' filters.yml | gmail-yaml-filters --dry-run - > fastmailFilters.xml
```

### Direct API Installation (Gmail only)

For advanced users, you can install filters directly via Gmail API using gmail-yaml-filters. Follow the [official instructions](https://github.com/mesozoic/gmail-yaml-filters?tab=readme-ov-file#synchronization-via-gmail-api).

## 📋 Available Files

- **`filters.yml`** - Source configuration file (human-readable)
- **`gmailFilters.xml`** - Pre-built Gmail import file (generated automatically)
- **`fastmailFilters.xml`** - Pre-built Fastmail import file (generated automatically)

## ⚙️ Customization

To change the archive label name:
1. Edit `filters.yml`
2. Find and replace `_Archive` with your preferred label name
3. Rebuild the XML files using the commands above

## 💡 Tips

- **Apply to existing emails**: When importing, choose to apply filters to existing conversations for immediate cleanup
- **Test first**: Start with a few filters to see how they work with your email patterns
- **Regular updates**: Check back for filter updates as new promotional patterns emerge

## 🤝 Contributing

Found a promotional email that isn't being caught? Please contribute!

1. Fork this repository
2. Add the new pattern to [`filters.yml`](https://github.com/stevenirby/unfuckemail/blob/master/filters.yml)
3. Submit a pull request

## 📄 License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International License**.

- ✅ **Free for personal use** - Use these filters in your personal email setup
- ✅ **Open source** - Modify, improve, and share with attribution
- ❌ **Commercial use requires permission** - Contact us for commercial licensing

For commercial use, please reach out to discuss licensing options.

[![CC BY-NC 4.0](https://licensebuttons.net/l/by-nc/4.0/88x31.png)](https://creativecommons.org/licenses/by-nc/4.0/)

---

## 🎲 Discover More

This project is brought to you by [Random Daily URLs](https://randomdailyurls.com) - a newsletter that delivers one absolutely random website to your inbox every weekday.

**No algorithms. No corporate bullshit. Just pure, curated randomness.**

[Subscribe to Random Daily URLs →](https://randomdailyurls.com)

Made with ❤️ and 🔥 by [@StevenIrby](https://randomdailyurls.com)
