# Visual Studio Code Setup Guide

## Installation

### Windows
1. Download VS Code from [https://code.visualstudio.com/](https://code.visualstudio.com/)
2. Run the installer
3. Check "Add to PATH" during installation
4. Launch VS Code

### macOS
1. Download VS Code from [https://code.visualstudio.com/](https://code.visualstudio.com/)
2. Open the downloaded .zip file
3. Drag Visual Studio Code to Applications folder
4. Launch from Applications

### Linux (Ubuntu/Debian)
```bash
sudo apt update
sudo apt install software-properties-common apt-transport-https wget
wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
sudo apt update
sudo apt install code
```

## Essential Extensions

### General Development
1. **Live Server** (ritwickdey.LiveServer)
   - Launch development local server with live reload

2. **Prettier - Code Formatter** (esbenp.prettier-vscode)
   - Automatic code formatting

3. **ESLint** (dbaeumer.vscode-eslint)
   - JavaScript linting

4. **Path Intellisense** (christian-kohler.path-intellisense)
   - Autocomplete file paths

5. **Auto Rename Tag** (formulahendry.auto-rename-tag)
   - Auto rename paired HTML tags

### Frontend Development
6. **ES7+ React/Redux/React-Native snippets** (dsznajder.es7-react-js-snippets)
   - React code snippets

7. **CSS Peek** (pranaygp.vscode-css-peek)
   - Jump to CSS definitions

8. **HTML CSS Support** (ecmel.vscode-html-css)
   - CSS class completion

### Backend Development
9. **REST Client** (humao.rest-client)
   - Test API endpoints directly in VS Code

10. **Thunder Client** (rangav.vscode-thunder-client)
    - Alternative API testing tool

### Version Control
11. **GitLens** (eamodio.gitlens)
    - Enhanced Git capabilities

12. **Git History** (donjayamanne.githistory)
    - View git log and file history

### Productivity
13. **TODO Highlight** (wayou.vscode-todo-highlight)
    - Highlight TODO comments

14. **Bracket Pair Colorizer 2** (CoenraadS.bracket-pair-colorizer-2)
    - Colorize matching brackets

15. **indent-rainbow** (oderwat.indent-rainbow)
    - Colorize indentation

## Configuration

### Settings (File > Preferences > Settings)

```json
{
  "editor.fontSize": 14,
  "editor.tabSize": 2,
  "editor.wordWrap": "on",
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
  "files.autoSave": "onFocusChange",
  "emmet.includeLanguages": {
    "javascript": "javascriptreact"
  },
  "liveServer.settings.donotShowInfoMsg": true
}
```

### Keyboard Shortcuts

| Action | Windows/Linux | macOS |
|--------|--------------|-------|
| Command Palette | Ctrl+Shift+P | Cmd+Shift+P |
| Quick Open File | Ctrl+P | Cmd+P |
| Toggle Terminal | Ctrl+` | Ctrl+` |
| Split Editor | Ctrl+\ | Cmd+\ |
| Format Document | Shift+Alt+F | Shift+Option+F |
| Go to Line | Ctrl+G | Cmd+G |
| Find in Files | Ctrl+Shift+F | Cmd+Shift+F |
| Multi-cursor | Alt+Click | Option+Click |

## Recommended Theme

- **One Dark Pro** (zhuangtongfa.Material-theme)
- **Material Icon Theme** (PKief.material-icon-theme)

## Terminal Integration

1. Open integrated terminal: Ctrl+` or View > Terminal
2. Select default shell:
   - Windows: Git Bash (recommended)
   - macOS/Linux: zsh or bash

## Tips & Tricks

### Emmet Abbreviations
```html
div.container>ul>li*5
```
Expands to:
```html
<div class="container">
  <ul>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
  </ul>
</div>
```

### Multiple Cursors
- Hold Alt (Option on Mac) and click to add cursors
- Ctrl+D (Cmd+D) to select next occurrence
- Ctrl+Shift+L (Cmd+Shift+L) to select all occurrences

### Quick File Navigation
- Ctrl+P (Cmd+P) and type filename
- Ctrl+Tab to switch between open files
- Ctrl+Shift+E to focus file explorer

## Troubleshooting

### Extensions Not Working
1. Restart VS Code
2. Check extension is enabled
3. Update VS Code to latest version

### Live Server Not Starting
1. Check no other server is running on same port
2. Right-click HTML file and select "Open with Live Server"

### Terminal Not Opening
1. Check terminal shell path in settings
2. Try resetting terminal: Ctrl+Shift+P > "Terminal: Kill All Terminals"

## Resources

- [VS Code Documentation](https://code.visualstudio.com/docs)
- [VS Code Tips & Tricks](https://code.visualstudio.com/docs/getstarted/tips-and-tricks)
- [Keyboard Shortcuts Reference](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)

---

*Last updated: January 2025*
