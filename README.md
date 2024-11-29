# ChromeAI-Assistant
**Powered by Chrome's Built-in AI Gemini Nano (No Internet Required)**

This project offers an offline AI assistant using Chrome's Built-in AI APIs and Gemini Nano, enabling features like summarization, text improvement, translation, and more—without the need for an internet connection.

## Prerequisites

1. **Download Chrome Dev Channel (or Canary Channel)**  
   Ensure that your version is **equal to or newer than 128.0.6545.0**.  
   - Download the Chrome Dev or Canary channel from the [Chrome Dev](https://www.google.com/intl/en_in/chrome/dev/) / [Chrome Canary](https://www.google.com/intl/en_in/chrome/canary/).

2. **Check Device Requirements**  
   Confirm that your device meets the following requirements:  
   - **At least 22 GB of free storage space**.  
   - Ensure that your device does not drop below 10 GB of available storage after the download, as the model will be deleted again if it does.

3. **Note on Free Disk Space Reporting**  
   - Some operating systems may report free disk space differently, e.g., by including or excluding disk space occupied by the trash bin.
   - On macOS, use **Disk Utility** to get a more accurate representation of free disk space.

4. **Enable Gemini Nano and the Prompt API**  
   Follow these steps to enable Gemini Nano and the Prompt API flags for local experimentation:

   1. Open a new tab in Chrome and go to:  
      `chrome://flags/#optimization-guide-on-device-model`  
      - Select **Enabled** for **BypassPerfRequirement**.  
      - This bypasses performance checks that might prevent Gemini Nano from downloading to your device.

   2. Go to:  
      `chrome://flags/#prompt-api-for-gemini-nano`  
      - Select **Enabled**.

   3. Relaunch Chrome to apply changes.

5. **Confirm Availability of Gemini Nano**  
   - Open Chrome DevTools and send the following in the console:
     ```javascript
     await ai.languageModel.capabilities().available;
     ```
   - If this returns **“readily”**, you are all set.
   - If this fails, first **try running Chrome as an administrator** and then test again.
   - If the issue persists, refer to this troubleshooting guide for further assistance: [Built-in AI Early Preview Program](https://docs.google.com/document/d/1VG8HIyz361zGduWgNG7R_R8Xkv0OOJ8b5C9QKeCjU0c/edit?tab=t.0)

## Tested on:
- **Chrome Dev Version**: 133.0.6847.2 (Official Build, 64-bit, cohort: Dev)

## Features
- **Summarize**: Condense lengthy content into key points.
- **Shorten**: Reduce text while retaining the core message.
- **Improve**: Enhance the quality of written content.
- **Translate**: Convert text from multiple languages to English.
- **Clear**: Reset the interface for a fresh start.
- **Voice**: Speak and receive AI-generated responses.

## Usage
Type or speak your message, and use the following hotkeys for actions:

- **Ctrl+Enter**: Generate output
- **Ctrl+Spacebar**: Voice input
- **Ctrl+S**: Summarize text
- **Ctrl+X**: Shorten text
- **Ctrl+I**: Improve text
- **Ctrl+L**: Translate text to English
- **Ctrl+E**: Clear text
- **Ctrl+R**: Clear memory
- **Esc**: Stop current operation

## Development
Built for the Google Chrome Built-in AI Challenge.

## License
© 2024 Abhiram Thimmaraju. All rights reserved.
