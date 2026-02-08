---
title: "How to Localize HoneyBear-Folio"
description: "Guide for contributing translations and adding new languages."
weight: 20
---

# Localizing HoneyBear-Folio

HoneyBear-Folio supports multiple languages for its user interface. You can help make the app accessible to more users by contributing translations or adding support for new languages.

## How Localization Works

- The app uses JSON files for each supported language (e.g., `en.json`, `es.json`).
- All UI text is referenced by keys and translated using these files.
- The language selector in Settings allows users to switch languages instantly.

## Steps to Add a New Language

1. **Create a Translation File**
   - Copy `en.json` from `app/src/i18n/`.
   - Rename it to your language code (e.g., `fr.json` for French).
   - Translate all values, keeping the keys unchanged.

2. **Register the Language**
   - Edit `AVAILABLE_LANGUAGES` in `app/src/i18n/i18n.js` to add your language:
     ```js
     export const AVAILABLE_LANGUAGES = [
       { code: "en", label: "English" },
       { code: "es", label: "Español" },
       { code: "fr", label: "Français" }, // Add your language here
     ];
     ```

3. **Test Your Translation**
   - Start the app and select your language in Settings.
   - Check that all UI elements are translated.

4. **Submit Your Contribution**
   - Open a pull request with your new translation file and updated language list.
   - Mention any untranslated keys or issues.

## Tips for Translators
- Keep translations concise and clear.
- Use consistent terminology.
- If a key is unclear, check the UI or ask in the project discussions.

## Improving Existing Translations
- You can also help by correcting or improving current translations.
- Edit the relevant JSON file and submit a pull request.

## Need Help?
- Ask questions or get support in the [GitHub Discussions](https://github.com/HoneyBearFolio/HoneyBear-Folio/discussions).

Thank you for helping make HoneyBear-Folio accessible to everyone!