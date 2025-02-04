# Cursor Configuration Repository

This repository contains a `.cursorrules` file that helps enforce consistent development practices and structured debugging workflows when using Cursor.

## Features
- Enforces concise but maintainable code.
- Encourages structured debugging with reasoning paragraphs.
- Promotes unbiased decision-making and thorough comparisons.
- Ensures clear documentation of changes.
- Guides effective search queries and problem-solving techniques.

## Installation & Usage

### Option 1: Clone and Symlink (Recommended)
To ensure `.cursorrules` is used across multiple projects, you can clone this repository and create a symbolic link:

```bash
# Clone the repository
git clone git@github.com:yourname/cursor-config.git ~/.cursor-config

# Create a symlink in your project directory
ln -s ~/.cursor-config/.cursorrules /your/project/.cursorrules
```

### Option 2: Use a Dotfiles Manager
If you manage configurations with `stow` or `chezmoi`, you can integrate `.cursorrules` seamlessly:

#### **Using Stow:**
```bash
# Install Stow if not installed
sudo apt install stow  # Linux
brew install stow      # macOS

# Move .cursorrules to dotfiles directory
mkdir -p ~/dotfiles/cursor
mv ~/.cursorrules ~/dotfiles/cursor/

# Stow the file into place
cd ~/dotfiles
stow cursor
```

### Option 3: Cloud Sync (Google Drive/Dropbox)
If you prefer a non-Git solution, store `.cursorrules` in a cloud folder and symlink it:

```bash
mv ~/.cursorrules ~/Dropbox/CursorSync/.cursorrules
ln -s ~/Dropbox/CursorSync/.cursorrules ~/.cursorrules
```

## Updating the Rules
To update `.cursorrules`, modify the file and commit the changes:

```bash
cd ~/.cursor-config
nano .cursorrules  # Make changes

git add .cursorrules
git commit -m "Updated cursorrules"
git push origin main
```

On other systems/projects, pull the latest version:
```bash
cd ~/.cursor-config
git pull origin main
```

## License
This repository is open-source and free to use under the MIT License.

## Contributions
Feel free to submit pull requests or issues to improve the configuration rules!