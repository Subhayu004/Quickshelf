QuickShelf 📋
A fast and intuitive Python CLI clipboard/snippet manager that helps you organize and retrieve your copied text snippets.

Features
🚀 Quick Storage: Automatically save clipboard content or manual input
🔍 Smart Search: Find snippets by keyword in content or tags
🏷️ Tagging System: Organize snippets with custom tags
📊 Usage Tracking: Monitor access patterns and statistics
💾 Local SQLite: All data stored locally in an SQLite database
🎨 Rich Interface: Beautiful terminal UI with colored output
Installation
From Source
Clone the repository:
bash
git clone https://github.com/yourusername/quickshelf.git
cd quickshelf
Install dependencies:
bash
pip install -r requirements.txt
Install the package:
bash
pip install -e .
Quick Install
bash
pip install -r requirements.txt
python -m quickshelf.main --help
Usage
Adding Snippets
Add current clipboard content:

bash
quickshelf add
Add specific text:

bash
quickshelf add "Your text here"
Add with tags:

bash
quickshelf add "git clone https://github.com/user/repo.git" --tags "git,commands"
Force use clipboard content:

bash
quickshelf add --clipboard
Listing Snippets
List recent snippets:

bash
quickshelf list
Search for specific content:

bash
quickshelf list --search "git"
Limit number of results:

bash
quickshelf list --limit 10
Retrieving Snippets
Get a snippet by ID:

bash
quickshelf get 5
Get and copy to clipboard:

bash
quickshelf get 5 --copy
Statistics
View database statistics:

bash
quickshelf stats
Database Location
QuickShelf stores its SQLite database at:

Linux/macOS: ~/.quickshelf/snippets.db
Windows: %USERPROFILE%\.quickshelf\snippets.db
Commands Reference
Command	Description	Options
add	Add a new snippet	--tags, --clipboard
list	List snippets	--limit, --search
get	Retrieve specific snippet	--copy
stats	Show database statistics	-
Examples
bash
# Add clipboard content with tags
quickshelf add --tags "python,snippet"

# Search for Python-related snippets
quickshelf list --search "python"

# Get snippet #3 and copy to clipboard
quickshelf get 3 --copy

# View your most used snippets
quickshelf stats
Requirements
Python 3.8+
typer
pyperclip
rich
Development
Project Structure
quickshelf/
├── quickshelf/
│   ├── __init__.py
│   └── main.py          # Main CLI application
├── requirements.txt     # Python dependencies
├── setup.py            # Package configuration
└── README.md           # This file
Contributing
Fork the repository
Create a feature branch
Make your changes
Add tests if applicable
Submit a pull request
License
MIT License - see LICENSE file for details.

Roadmap
 Import/export functionality
 Snippet categories beyond tags
 Advanced search with regex support
 Sync between devices
 GUI interface
 Plugin system for custom integrations
