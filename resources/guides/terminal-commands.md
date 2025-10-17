# Terminal Commands Guide

## What is a Terminal?

A terminal (or command line interface) allows you to interact with your computer using text commands instead of clicking through graphical interfaces.

### Terminal Names by OS
- **Windows**: Command Prompt (cmd), PowerShell, Git Bash
- **macOS**: Terminal, iTerm2
- **Linux**: Terminal, Bash, Zsh

## Opening the Terminal

- **Windows**:
  - Press `Win + R`, type `cmd` or `powershell`
  - Search for "Terminal" or "Command Prompt"
  - In VS Code: Press `Ctrl + \``

- **macOS**:
  - Press `Cmd + Space`, type "Terminal"
  - Or Applications > Utilities > Terminal
  - In VS Code: Press `Ctrl + \``

- **Linux**:
  - Press `Ctrl + Alt + T`
  - Or search for "Terminal" in applications
  - In VS Code: Press `Ctrl + \``

## Basic Navigation

### Current Directory
```bash
# Show current directory (Print Working Directory)
pwd
```

### List Files
```bash
# List files in current directory
ls                  # macOS/Linux
dir                 # Windows

# List with details
ls -l               # macOS/Linux
ls -la              # Include hidden files
dir /w              # Windows wide format

# List all files including hidden
ls -a               # macOS/Linux
dir /a              # Windows
```

### Change Directory
```bash
# Move to a directory
cd folder-name

# Move up one level
cd ..

# Move to home directory
cd ~                # macOS/Linux
cd %USERPROFILE%    # Windows

# Move to specific path
cd /path/to/folder              # macOS/Linux
cd C:\path\to\folder            # Windows

# Go back to previous directory
cd -                # macOS/Linux only
```

## File Operations

### Creating Files
```bash
# Create empty file
touch filename.txt          # macOS/Linux
echo. > filename.txt        # Windows

# Create file with content
echo "Hello" > filename.txt
```

### Creating Directories
```bash
# Create directory
mkdir folder-name

# Create nested directories
mkdir -p parent/child/grandchild    # macOS/Linux
mkdir parent\child\grandchild       # Windows

# Create multiple directories
mkdir folder1 folder2 folder3
```

### Copying Files
```bash
# Copy file
cp source.txt destination.txt       # macOS/Linux
copy source.txt destination.txt     # Windows

# Copy directory
cp -r source-folder dest-folder     # macOS/Linux
xcopy source-folder dest-folder /E  # Windows
```

### Moving/Renaming Files
```bash
# Move or rename file
mv old-name.txt new-name.txt        # macOS/Linux
move old-name.txt new-name.txt      # Windows

# Move to different directory
mv file.txt /path/to/destination/   # macOS/Linux
move file.txt C:\path\to\dest\      # Windows
```

### Deleting Files
```bash
# Delete file
rm filename.txt             # macOS/Linux
del filename.txt            # Windows

# Delete directory
rm -r folder-name           # macOS/Linux
rmdir /s folder-name        # Windows

# Force delete (be careful!)
rm -rf folder-name          # macOS/Linux
```

### Viewing File Contents
```bash
# Display entire file
cat filename.txt            # macOS/Linux
type filename.txt           # Windows

# Display first few lines
head filename.txt           # macOS/Linux
head -n 10 filename.txt     # First 10 lines

# Display last few lines
tail filename.txt           # macOS/Linux
tail -n 10 filename.txt     # Last 10 lines

# View file page by page
less filename.txt           # macOS/Linux (q to quit)
more filename.txt           # Windows
```

## Searching

### Find Files
```bash
# Find files by name (macOS/Linux)
find . -name "*.txt"
find /path -name "filename.txt"

# Find files by name (Windows)
dir /s /b *.txt
where /r . *.txt
```

### Search Within Files
```bash
# Search for text in files (macOS/Linux)
grep "search-term" filename.txt
grep -r "search-term" .             # Recursive search

# Search for text in files (Windows)
findstr "search-term" filename.txt
findstr /s "search-term" *.*        # Recursive search
```

## System Information

### Check System Info
```bash
# System information
uname -a                    # macOS/Linux
systeminfo                  # Windows

# Current user
whoami

# Disk usage
df -h                       # macOS/Linux
wmic logicaldisk get size,freespace,caption  # Windows
```

### Process Management
```bash
# List running processes
ps aux                      # macOS/Linux
tasklist                    # Windows

# Kill process
kill PID                    # macOS/Linux
taskkill /PID pid /F        # Windows
```

## Network Commands

```bash
# Check network connectivity
ping google.com

# Show IP address
ipconfig                    # Windows
ifconfig                    # macOS/Linux (older)
ip addr                     # Linux (newer)

# Show network connections
netstat -an
```

## Permissions (macOS/Linux)

```bash
# Change file permissions
chmod 755 file.txt
chmod +x script.sh          # Make executable

# Change ownership
chown user:group file.txt

# Run with sudo (superuser)
sudo command
```

## Environment Variables

```bash
# View all environment variables
printenv                    # macOS/Linux
set                         # Windows

# View specific variable
echo $PATH                  # macOS/Linux
echo %PATH%                 # Windows

# Set temporary variable
export VAR_NAME="value"     # macOS/Linux
set VAR_NAME=value          # Windows
```

## Command History

```bash
# View command history
history                     # macOS/Linux
doskey /history            # Windows

# Repeat last command
!!                          # macOS/Linux
# Use Up Arrow key on Windows

# Search history
Ctrl + R (then type)        # macOS/Linux
```

## Pipes and Redirection

```bash
# Redirect output to file
command > output.txt        # Overwrite
command >> output.txt       # Append

# Pipe output to another command
ls -l | grep ".txt"         # macOS/Linux
dir | findstr ".txt"        # Windows

# Redirect errors
command 2> errors.txt       # Error output only
command &> all.txt          # Both output and errors
```

## Package Managers

### Node.js (npm/yarn)
```bash
# Check version
npm --version
node --version

# Install package
npm install package-name
npm install -g package-name  # Global install

# Install dependencies
npm install

# Run scripts
npm start
npm run build
npm test
```

### Python (pip)
```bash
# Check version
python --version
pip --version

# Install package
pip install package-name

# Install from requirements
pip install -r requirements.txt

# List installed packages
pip list
```

## Useful Shortcuts

### Universal Shortcuts
- `Tab` - Autocomplete file/folder names
- `Ctrl + C` - Cancel current command
- `Ctrl + L` or `clear` - Clear screen
- `Ctrl + D` - Exit terminal
- `Up/Down Arrows` - Navigate command history

### macOS/Linux Specific
- `Ctrl + A` - Move to beginning of line
- `Ctrl + E` - Move to end of line
- `Ctrl + U` - Clear line before cursor
- `Ctrl + K` - Clear line after cursor
- `Ctrl + W` - Delete word before cursor

## Developer Commands

### Git (Version Control)
```bash
git status
git add .
git commit -m "message"
git push
git pull
git clone <url>
```

### Create React App
```bash
npx create-react-app my-app
cd my-app
npm start
```

### Express Server
```bash
mkdir my-server
cd my-server
npm init -y
npm install express
```

### Common Development Commands
```bash
# Run development server
npm run dev
npm start

# Build for production
npm run build

# Run tests
npm test
npm run test

# Lint code
npm run lint
```

## Common Scenarios

### Starting a New Project
```bash
# Create project folder
mkdir my-project
cd my-project

# Initialize Git
git init

# Initialize npm
npm init -y

# Install dependencies
npm install express react dotenv

# Create files
touch index.js .env .gitignore

# Open in VS Code
code .
```

### Deploying a Project
```bash
# Build project
npm run build

# Check git status
git status

# Commit changes
git add .
git commit -m "Prepare for deployment"
git push

# Deploy (example with Vercel)
vercel deploy
```

## Troubleshooting

### Command Not Found
```bash
# Check if installed
which command-name          # macOS/Linux
where command-name          # Windows

# Add to PATH if needed
export PATH=$PATH:/new/path # macOS/Linux
```

### Permission Denied
```bash
# Run with elevated permissions
sudo command                # macOS/Linux
# Right-click > Run as Administrator (Windows)
```

### Port Already in Use
```bash
# Find process using port
lsof -i :3000              # macOS/Linux
netstat -ano | findstr :3000  # Windows

# Kill process
kill -9 PID                # macOS/Linux
taskkill /PID pid /F       # Windows
```

## Best Practices

1. **Use Tab completion** - Save time and avoid typos
2. **Read error messages carefully** - They often tell you exactly what's wrong
3. **Be careful with delete commands** - There's no recycle bin
4. **Use version control** - Commit often
5. **Document your commands** - Keep notes of complex commands
6. **Use relative paths when possible** - Makes projects portable

## Resources

- [Command Line Crash Course](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Understanding_client-side_tools/Command_line)
- [Linux Command Line Basics](https://ubuntu.com/tutorials/command-line-for-beginners)
- [Windows Command Line Reference](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/windows-commands)
- [Explainshell](https://explainshell.com/) - Explains shell commands

## Quick Reference Card

| Task | macOS/Linux | Windows |
|------|-------------|---------|
| List files | `ls` | `dir` |
| Change directory | `cd` | `cd` |
| Copy file | `cp` | `copy` |
| Move file | `mv` | `move` |
| Delete file | `rm` | `del` |
| Create directory | `mkdir` | `mkdir` |
| View file | `cat` | `type` |
| Clear screen | `clear` | `cls` |
| Find text | `grep` | `findstr` |
| Current directory | `pwd` | `cd` |

---

*Last updated: January 2025*
