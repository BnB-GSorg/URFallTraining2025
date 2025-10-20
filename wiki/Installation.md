# Installation Guide

This guide will help you set up and access the URFallTraining2025 repository on your local machine.

## Prerequisites

Before you begin, ensure you have the following installed:

### Required Software

- **Git**: Version control system
  - Windows: Download from [git-scm.com](https://git-scm.com/)
  - Mac: `brew install git` or download from git-scm.com
  - Linux: `sudo apt-get install git` (Debian/Ubuntu) or `sudo yum install git` (RedHat/CentOS)

### Recommended Software

- **Text Editor or IDE**: For viewing and editing files
  - [Visual Studio Code](https://code.visualstudio.com/)
  - [Sublime Text](https://www.sublimetext.com/)
  - [Atom](https://atom.io/)
  - Any text editor of your choice

- **Markdown Viewer**: For reading documentation
  - Many IDEs include Markdown preview
  - Browser extensions available for Chrome, Firefox, etc.

## Installation Steps

### 1. Verify Git Installation

Open a terminal or command prompt and verify Git is installed:

```bash
git --version
```

You should see output like: `git version 2.x.x`

### 2. Clone the Repository

Choose a directory where you want to store the project and run:

```bash
git clone https://github.com/BnB-GSorg/URFallTraining2025.git
```

This will create a new directory called `URFallTraining2025` with all the repository contents.

### 3. Navigate to the Repository

```bash
cd URFallTraining2025
```

### 4. Verify the Installation

List the contents to ensure everything was cloned correctly:

```bash
# On Windows
dir

# On Mac/Linux
ls -la
```

You should see files including:
- `.gitignore`
- `LICENSE`
- `README.md`
- `wiki/` (directory)

## Configuration

### Set Up Git (First Time Users)

If this is your first time using Git, configure your identity:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### Set Up SSH Keys (Optional but Recommended)

For easier authentication with GitHub:

1. Check for existing SSH keys:
   ```bash
   ls -al ~/.ssh
   ```

2. Generate a new SSH key (if needed):
   ```bash
   ssh-keygen -t ed25519 -C "your.email@example.com"
   ```

3. Add the SSH key to your GitHub account:
   - Copy the public key: `cat ~/.ssh/id_ed25519.pub`
   - Go to GitHub → Settings → SSH and GPG keys → New SSH key
   - Paste your key and save

4. Update the remote URL to use SSH:
   ```bash
   git remote set-url origin git@github.com:BnB-GSorg/URFallTraining2025.git
   ```

## Keeping Your Copy Updated

### Pull Latest Changes

To get the latest updates from the repository:

```bash
git pull origin main
```

### Check Repository Status

To see if there are any local changes:

```bash
git status
```

### View Commit History

To see recent changes:

```bash
git log --oneline -10
```

## Working with the Repository

### Creating a Branch

If you plan to contribute, create a feature branch:

```bash
git checkout -b feature/your-feature-name
```

### Viewing Files

Use your preferred text editor or IDE to open and view files:

```bash
# Using VS Code
code .

# Using Vim
vim README.md

# Using Nano
nano README.md
```

## Troubleshooting

### Problem: "git: command not found"

**Solution**: Git is not installed or not in your PATH. Reinstall Git and ensure it's added to your system PATH.

### Problem: "Permission denied (publickey)"

**Solution**: Your SSH keys are not set up correctly. Use HTTPS instead:
```bash
git clone https://github.com/BnB-GSorg/URFallTraining2025.git
```

Or set up SSH keys following the instructions above.

### Problem: "Repository not found"

**Solution**: 
- Check that you typed the URL correctly
- Ensure you have internet connectivity
- Verify the repository exists and is accessible

### Problem: Conflicts when pulling updates

**Solution**:
```bash
# Save your local changes
git stash

# Pull updates
git pull origin main

# Reapply your changes
git stash pop
```

### Problem: Large files won't clone

**Solution**: If the repository contains large files, ensure you have:
- Sufficient disk space
- Stable internet connection
- Consider using Git LFS if large binary files are involved

## Additional Tools

### For Design Files

Depending on the design files included in the repository, you may need:

- **CAD Software**: SolidWorks, Fusion 360, FreeCAD, etc.
- **3D Modeling**: Blender, Maya, etc.
- **Circuit Design**: KiCad, Eagle, Fritzing, etc.

Check specific project documentation for detailed software requirements.

### For Robot Programming

- **URSim**: Universal Robots simulator (if working with UR robots)
- **RobotStudio**: ABB's simulation software (if applicable)
- **Python**: For scripting and automation
- **MATLAB/Simulink**: For control systems (if applicable)

## Getting Help

If you encounter issues during installation:

1. Check the [FAQ](FAQ.md)
2. Search [GitHub Issues](https://github.com/BnB-GSorg/URFallTraining2025/issues)
3. Create a new issue with:
   - Your operating system and version
   - Git version
   - Complete error message
   - Steps you've already tried

## Next Steps

After installation:

1. Read the [Home](Home.md) page for project overview
2. Explore the [Project Structure](Project-Structure.md)
3. Check the [FAQ](FAQ.md) for common questions
4. Start exploring the training materials!

---

*Last updated: October 2025*
