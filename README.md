# Unfuck Email - Filters

Email filters for popular email providers to help organize and clean up your inbox.

## Filters Available

- **Gmail Filters** (`gmailFilters.xml`) - Import-ready XML file for Gmail
- **Fastmail Filters** (`fastmailFilters.xml`) - Import-ready XML file for Fastmail
- **YAML Configuration** (`filters.yml`) - Source configuration for generating filters
- **Light Filters** (`filters_light.yml`) - Minimal filter set
- **Test Filters** (`filters_test.xml`) - Test configuration

## Dependencies

* gmail-yaml-filters

To build the YML file use [gmail-yaml-filters](https://github.com/mesozoic/gmail-yaml-filters)

### Installation

For MacOS:

```bash
brew install pipx
pipx install gmail-yaml-filters
```

## Build the filters.xml file for Gmail / Fastmail

First clone this project or download the filters.yml file.

```bash
gmail-yaml-filters --dry-run filters.yml > filters.xml
```

## Apply filters

### Option 1

gmail-yaml-filters can be used to install the filters directly, just follow the [instructions](https://github.com/mesozoic/gmail-yaml-filters?tab=readme-ov-file#synchronization-via-gmail-api).

### Option 2

Go to your settings page and import the filters manually.

#### Gmail
1. Go to [Gmail Settings Page](https://mail.google.com/mail/u/0/#settings/filters) 
2. Click "Import filters"
3. Upload `gmailFilters.xml`

#### Fastmail
1. Go to [Fastmail Settings Page](https://app.fastmail.com/settings/filters)
2. Click "Import"
3. Upload `fastmailFilters.xml`

## Notes

It's recommended to apply these filters to all new incoming mail.

A label is created for all filtered emails. To change just find and replace `_Archive` with the desired label name.

## Contributing

This project is part of the larger [UnfuckEmail](https://github.com/stevenirby/unfuckemail) ecosystem.
