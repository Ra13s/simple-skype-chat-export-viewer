# Skype Chat Export Viewer

A simple, client-side HTML viewer for Skype `messages.json` export files.

This tool allows you to browse your exported Skype conversations **locally** in your web browser without needing to upload your sensitive chat data anywhere.

## Features

*   **Local Processing:** Your `messages.json` file is processed entirely within your browser using JavaScript. **No data is uploaded or sent anywhere.** This is crucial for protecting the privacy of your chat history.
*   **Conversation List:** Displays all conversations found in the export, sorted by the most recent message.
*   **Message Display:** Shows messages chronologically within a selected conversation.
    *   Distinguishes between your messages and messages from others.
    *   Displays sender names and timestamps.
    *   Renders basic formatting (bold, italic, strikethrough).
    *   Displays links, shared images/videos/files (metadata and thumbnails only), and basic system messages (like topic changes).
*   **Search:** Filter conversations by name.
*   **Simple Interface:** Basic, clean interface focused on readability.

## How to Use

1.  **Download:** Get the `index.html` file (or use the live version via GitHub Pages if available - see below).
2.  **Export Skype Data:** If you haven't already, export your Skype chat history. This process creates a `.tar` file containing `messages.json`. Extract the `messages.json` file from the archive.
3.  **Open:** Open the `index.html` file in your web browser (Firefox, Chrome, Edge, Safari etc.).
4.  **Select File:** Click the "Select messages.json File" button and choose the `messages.json` file you extracted in step 2. **Note:** Your file is processed directly in your browser and is *never* uploaded.
5.  **Browse:** Your conversations will load in the sidebar. Click on a conversation to view its messages.

## GitHub Pages (Live Demo)

You can likely use a live version of this tool hosted directly via GitHub Pages (if the repository owner has enabled it). Check the repository's description or settings for a URL typically in the format: `https://<username>.github.io/<repository-name>/`

Using the live version still processes your file locally in *your* browser – your chat data is not sent to the server hosting the page.

## Privacy

Your privacy is paramount, especially concerning personal chat logs. This tool is designed to work completely offline or with local browser processing only. Your chat data remains on your computer and is **never transmitted over the internet** by this tool. All processing happens locally in your web browser.

## Limitations

*   **Performance:** Very large `messages.json` files (hundreds of MB or more) might cause the browser to become slow or unresponsive during loading and processing.
*   **Formatting:** Does not render all possible Skype formatting, rich content, or complex elements perfectly (e.g., polls, intricate card layouts might show limited info).
*   **Media:** Only displays thumbnails for images/videos if included in the export data. It does not embed the actual media files (as they are usually separate in the export). Links to files are shown, but the files themselves are not accessible directly through this viewer.
*   **Calls:** Call history details (duration, participants beyond basic events) are generally not displayed in detail.
*   **Modern Features:** Features added to Skype after the export format was defined might not be represented.
*   **Error Handling:** Basic error handling is included, but corrupted or unexpected `messages.json` structures might cause issues.

## Development Note

This tool was developed mostly with assistance from the AI model Gemini 2.5 Pro.

## License

This project is licensed under the **MIT License**. See the `LICENSE` file for the full text.