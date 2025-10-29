# Windows MCP - Gemini CLI Extension

This is an integration of [Windows-MCP](https://github.com/CursorTouch/Windows-MCP) as a Gemini CLI built-in extension.

## Features

The Windows MCP Server provides comprehensive Windows operating system integration:

- **Seamless Windows Integration**: Interacts natively with Windows UI elements, opens apps, controls windows
- **UI Automation**: Rich toolset for keyboard, mouse operations and capturing window/UI state
- **Application Control**: Launch, switch between, and control Windows applications
- **File Navigation**: Navigate and interact with Windows file system
- **Desktop Interaction**: Simulate user input, capture screenshots, interact with UI elements
- **QA Testing**: Automated testing capabilities for Windows applications
- **Real-Time Interaction**: Fast response times for automation tasks (0.7-2.5 seconds typical latency)

## How It Works

This extension integrates the Python-based Windows MCP Server into Gemini CLI:

1. **Automatic Installation**: When you run `npm install`, the `postinstall` script automatically installs all Python dependencies using the embedded Python 3.13.7
2. **Zero Configuration**: The extension is automatically loaded by Gemini CLI's extension system
3. **MCP Server**: Runs as an MCP server using stdio transport for Windows automation

## File Structure

```
windows-mcp/
├── main.py                    # Main server entry point
├── src/
│   ├── desktop/              # Desktop interaction services
│   └── tree/                 # File tree utilities
├── gemini-extension.json     # Extension configuration
├── package.json              # NPM package configuration
├── install-deps.js           # Automatic dependency installer
└── EXTENSION.md             # This file
```

## Usage

Once installed, you can use Windows automation tools through Gemini CLI:

### Example Commands (via LLM)

- "Open Notepad"
- "Take a screenshot of the current window"
- "Click on the Start menu"
- "Type 'Hello World' in the active window"
- "List all running applications"
- "Navigate to C:\Users\Documents"
- "Close the active window"

## Platform Requirements

- **Platform**: Windows only (Windows 7, 8, 8.1, 10, 11)
- **Language**: English as default Windows language highly preferred
- **Python**: 3.13+

## Key Capabilities

- **Window Management**: Open, close, minimize, maximize, switch between windows
- **Mouse & Keyboard**: Simulate mouse clicks, movements, keyboard input
- **UI Element Interaction**: Interact with buttons, text fields, menus, and other UI elements
- **Screen Capture**: Take screenshots of desktop, windows, or specific regions
- **Application Launching**: Start any Windows application by name or path
- **Process Management**: Query and manage running processes
- **File System Operations**: Navigate directories, read file contents

## Dependencies

Python dependencies (automatically installed):
- click >= 8.2.1
- fastmcp >= 2.8.1
- fuzzywuzzy >= 0.18.0
- humancursor >= 1.1.5
- ipykernel >= 6.30.0
- live-inspect >= 0.1.1
- markdownify >= 1.1.0
- pdfplumber >= 0.11.7
- pillow >= 11.2.1
- psutil >= 7.0.0
- pyautogui >= 0.9.54
- pygetwindow >= 0.0.9
- python-levenshtein >= 0.27.1
- pywinauto >= 0.6.9
- requests >= 2.32.3
- tabulate >= 0.9.0
- uiautomation >= 2.0.24

## Platform Support

- ✅ Windows 7, 8, 8.1, 10, 11
- ❌ macOS (not supported)
- ❌ Linux (not supported)

## License

This extension integrates the original Windows-MCP which is licensed under MIT License.
