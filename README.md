<h1>QuickShelf 📋</h1>
<p><em>A fast and intuitive Python CLI clipboard/snippet manager that helps you organize and retrieve your copied text snippets.</em></p>

<hr>

<h2>✨ Features</h2>
<ul>
  <li>🚀 <b>Quick Storage</b> — Automatically save clipboard content or manual input</li>
  <li>🔍 <b>Smart Search</b> — Find snippets by keyword in content or tags</li>
  <li>🏷️ <b>Tagging System</b> — Organize snippets with custom tags</li>
  <li>📊 <b>Usage Tracking</b> — Monitor access patterns and statistics</li>
  <li>💾 <b>Local SQLite</b> — All data stored locally in an SQLite database</li>
  <li>🎨 <b>Rich Interface</b> — Beautiful terminal UI with colored output</li>
</ul>

<hr>

<h2>📦 Installation</h2>

<h3>From Source</h3>
<pre><code>git clone https://github.com/Subhayu004/quickshelf.git
cd quickshelf
pip install -r requirements.txt
pip install -e .
</code></pre>

<h3>Quick Install</h3>
<pre><code>pip install -r requirements.txt
python -m quickshelf.main --help
</code></pre>

<hr>

<h2>🚀 Usage</h2>

<h3>Adding Snippets</h3>
<pre><code># Add current clipboard content
quickshelf add

# Add specific text
quickshelf add "Your text here"

# Add with tags
quickshelf add "git clone https://github.com/user/repo.git" --tags "git,commands"

# Force use clipboard content
quickshelf add --clipboard
</code></pre>

<h3>Listing Snippets</h3>
<pre><code># List recent snippets
quickshelf list

# Search for specific content
quickshelf list --search "git"

# Limit number of results
quickshelf list --limit 10
</code></pre>

<h3>Retrieving Snippets</h3>
<pre><code># Get a snippet by ID
quickshelf get 5

# Get and copy to clipboard
quickshelf get 5 --copy
</code></pre>

<h3>Statistics</h3>
<pre><code># View database statistics
quickshelf stats
</code></pre>

<hr>

<h2>📂 Database Location</h2>
<ul>
  <li><b>Linux/macOS:</b> ~/.quickshelf/snippets.db</li>
  <li><b>Windows:</b> %USERPROFILE%\.quickshelf\snippets.db</li>
</ul>

<hr>

<h2>🧭 Commands Reference</h2>
<table>
  <thead>
    <tr>
      <th>Command</th>
      <th>Description</th>
      <th>Options</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>add</code></td>
      <td>Add a new snippet</td>
      <td><code>--tags</code>, <code>--clipboard</code></td>
    </tr>
    <tr>
      <td><code>list</code></td>
      <td>List snippets</td>
      <td><code>--limit</code>, <code>--search</code></td>
    </tr>
    <tr>
      <td><code>get</code></td>
      <td>Retrieve specific snippet</td>
      <td><code>--copy</code></td>
    </tr>
    <tr>
      <td><code>stats</code></td>
      <td>Show database statistics</td>
      <td>-</td>
    </tr>
  </tbody>
</table>

<hr>

<h2>💡 Examples</h2>
<pre><code># Add clipboard content with tags
quickshelf add --tags "python,snippet"

# Search for Python-related snippets
quickshelf list --search "python"

# Get snippet #3 and copy to clipboard
quickshelf get 3 --copy

# View your most used snippets
quickshelf stats
</code></pre>

<hr>

<h2>🛠️ Requirements</h2>
<ul>
  <li>Python 3.8+</li>
  <li><a href="https://typer.tiangolo.com/">typer</a></li>
  <li><a href="https://pypi.org/project/pyperclip/">pyperclip</a></li>
  <li><a href="https://github.com/Textualize/rich">rich</a></li>
</ul>

<hr>

<h2>🧑‍💻 Development</h2>
<h3>Project Structure</h3>
<pre><code>quickshelf/
├── quickshelf/
│   ├── __init__.py
│   └── main.py          # Main CLI application
├── requirements.txt     # Python dependencies
├── setup.py             # Package configuration
└── README.md            # This file
</code></pre>

<hr>

<h2>🤝 Contributing</h2>
<ol>
  <li>Fork the repository</li>
  <li>Create a feature branch</li>
  <li>Make your changes</li>
  <li>Add tests if applicable</li>
  <li>Submit a pull request</li>
</ol>

<hr>

<h2>📜 License</h2>
<p>MIT License — see <a href="LICENSE">LICENSE</a> for details.</p>

<hr>

<h2>🗺️ Roadmap</h2>
<ul>
  <li>📥 Import/export functionality</li>
  <li>🗂️ Snippet categories beyond tags</li>
  <li>🔎 Advanced search with regex support</li>
  <li>🔄 Sync between devices</li>
  <li>🖥️ GUI interface</li>
  <li>🧩 Plugin system for custom integrations</li>
</ul>
