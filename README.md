# LinkedIn Reaction Deleter

A browser-based script to automatically remove your LinkedIn reactions (likes, celebrates, supports, etc.) with customizable speed settings. This script helps you clean up your LinkedIn activity history efficiently.

## Features

- Automatically finds and removes your reactions on LinkedIn posts
- Two speed modes: Human Speed 🚶 and Toyota Supra Speed 🏎️
- Handles pagination by clicking "Show more results"
- Automatically scrolls to load more content
- Provides detailed console logging
- Can be stopped at any time
- Error handling and retry mechanisms

## Prerequisites

Before you begin, ensure you have:
- A modern web browser (Chrome, Firefox, Edge, etc.)
- Access to your browser's developer console
- Logged into LinkedIn in your browser

## Installation

1. Copy the entire content of `reaction-deleter.js`
2. Navigate to your LinkedIn reactions page:
   - Go to your LinkedIn profile
   - Click on "Activity"
   - Click on "All activity" dropdown
   - Select "Reactions"

## Usage

1. Open your browser's developer console:
   - Chrome/Edge: Press `F12` or `Ctrl + Shift + J` (Windows/Linux) or `Cmd + Option + J` (Mac)
   - Firefox: Press `F12` or `Ctrl + Shift + K` (Windows/Linux) or `Cmd + Option + K` (Mac)

2. Paste the script into the console and press Enter

3. Choose a speed mode by typing one of these commands:
```javascript
setDeleteSpeed('HUMAN')   // Normal speed with safe delays
setDeleteSpeed('SUPRA')   // Super fast mode
```

4. To stop the script at any time, type:
```javascript
stopReactionDeletion()
```

## Speed Modes

### Human Speed 🚶
- Scroll delay: 2 seconds
- Click delay: 1.5 seconds
- Load delay: 3 seconds
- Base delay: 1 second
- Best for: Avoiding rate limits and detection
- Use when: You want to play it safe

### Toyota Supra Speed 🏎️
- Scroll delay: 200ms
- Click delay: 200ms
- Load delay: 500ms
- Base delay: 200ms
- Best for: Quick cleanup when you have many reactions
- Warning: May trigger rate limits

You can switch speeds at any time by running the `setDeleteSpeed()` command again.

## How It Works

The script will:
1. Find all visible reaction buttons on the page
2. Click each reaction to remove it
3. Scroll down to load more content
4. Click "Show more results" when available
5. Repeat until all reactions are processed or you stop it

## Console Output

You'll see progress updates in the console:
```
*** Starting reaction removal process with Human Speed 🚶 ***
Scanning for reaction buttons...
Found 10 reaction buttons
Successfully removed reaction
...
```

## Troubleshooting

1. **Script not finding reactions:**
   - Make sure you're on your activity page filtered by reactions
   - Try scrolling manually to load some reactions before running
   - Check if your LinkedIn UI is up to date

2. **Rate limiting:**
   - Switch to Human Speed mode
   - Wait a few minutes and try again
   - Try running the script in shorter sessions

3. **Script seems stuck:**
   - Use `stopReactionDeletion()`
   - Refresh the page and try again
   - Make sure your internet connection is stable

## Known Limitations

- Only works on reactions visible in your activity feed
- LinkedIn's UI updates may require script updates
- Rate limiting may occur in Supra mode
- Very large numbers of reactions may require multiple runs

## Safety Features

- Configurable speeds to avoid rate limiting
- Proper delays between actions
- Error handling for each reaction removal
- Ability to stop at any time
- Progress logging in console
- Confirmation of completion

## Disclaimer

This script is provided as-is without any guarantees. Always review the code before running scripts in your browser console. Use at your own risk and ensure you want to remove the reactions before running the script.

## License

This project is licensed under a Personal Use License - see the LICENSE file for details. Commercial use is strictly prohibited.
