# MC-CMS Marketplace

Official marketplace repository for MC-CMS plugins, themes, and games.

## 🏪 About

This repository hosts the community marketplace for MC-CMS. The marketplace uses a simple GitHub-based system where all packages are listed in `registry.json`.

## 📦 Structure

```
MCCMS-marketplace/
├── README.md
├── registry.json          # Main registry file
├── plugins/               # Plugin packages
│   └── example-plugin/
│       ├── plugin.json
│       └── download.zip
├── themes/                # Theme packages
│   └── example-theme/
│       ├── theme.json
│       └── download.zip
└── games/                 # Game integration packages
```

## 🔗 Registry URL

The marketplace is accessed via:
```
https://raw.githubusercontent.com/Exilon-Studios/MCCMS-marketplace/main/registry.json
```

## 📝 Registry Format

```json
{
  "update": {
    "version": "1.0.0",
    "file": "mccms-1.0.0.zip",
    "url": "https://github.com/Exilon-Studios/MCCMS/releases/download/v1.0.0/mccms-1.0.0.zip",
    "hash": "sha256_hash"
  },
  "plugins": [
    {
      "id": "plugin-id",
      "name": "Plugin Name",
      "description": "Plugin description",
      "version": "1.0.0",
      "author": "Author Name",
      "url": "https://raw.githubusercontent.com/Exilon-Studios/MCCMS-marketplace/main/plugins/plugin-id/download.zip",
      "hash": "sha256_hash",
      "mccms_api": "1.0.0"
    }
  ],
  "themes": [
    {
      "id": "theme-id",
      "name": "Theme Name",
      "description": "Theme description",
      "version": "1.0.0",
      "author": "Author Name",
      "url": "https://raw.githubusercontent.com/Exilon-Studios/MCCMS-marketplace/main/themes/theme-id/download.zip",
      "hash": "sha256_hash",
      "mccms_api": "1.0.0"
    }
  ],
  "games": [],
  "alerts": []
}
```

## 🚀 How to Submit Your Package

### For Plugins

1. **Prepare your plugin**:
   - Create a plugin using `php artisan plugin:create "Your Plugin"`
   - Ensure it follows MC-CMS plugin structure
   - Test thoroughly

2. **Create plugin.json**:
```json
{
  "id": "your-plugin",
  "name": "Your Plugin",
  "description": "Plugin description",
  "version": "1.0.0",
  "author": "Your Name",
  "mccms_api": "1.0.0"
}
```

3. **Create download.zip**:
   - Zip your plugin directory
   - Include only necessary files (no node_modules, .git, etc.)

4. **Fork this repository**

5. **Add your plugin**:
   - Create `plugins/your-plugin/` directory
   - Add `plugin.json` and `download.zip`
   - Calculate SHA256 hash: `sha256sum download.zip`

6. **Update registry.json**:
   - Add your plugin entry to the `plugins` array
   - Include the correct URL and hash

7. **Submit Pull Request**:
   - Title: "Add plugin: Your Plugin Name"
   - Description: Brief description of your plugin

### For Themes

Same process as plugins, but in the `themes/` directory.

## 📋 Package Requirements

### Plugins
- Must follow MC-CMS plugin structure
- Must include `plugin.json`
- Must be compatible with MC-CMS 1.0.0+
- Must not contain malicious code
- Must be tested and functional

### Themes
- Must follow MC-CMS theme structure
- Must include `theme.json`
- Must be compatible with MC-CMS 1.0.0+
- Must be responsive
- Must not break core functionality

## ✅ Review Process

1. **Automated Checks**:
   - Package structure validation
   - JSON syntax validation
   - Hash verification

2. **Manual Review**:
   - Code quality review
   - Security audit
   - Functionality testing

3. **Approval**:
   - Packages are approved by Exilon Studios team
   - Updates to existing packages are auto-approved if from original author

## 🔒 Security

If you discover a security vulnerability in any package, please email **security@exilon-studios.com**.

## 📄 License

All packages in this marketplace must specify their license. Recommended licenses:
- GPL-3.0 (for open source)
- MIT (for permissive open source)
- Proprietary (for commercial packages)

## 💡 Support

- **Documentation**: https://github.com/Exilon-Studios/MCCMS
- **Issues**: https://github.com/Exilon-Studios/MCCMS-marketplace/issues
- **Discussions**: https://github.com/Exilon-Studios/MCCMS/discussions

---

**Made with ❤️ by Exilon Studios**
