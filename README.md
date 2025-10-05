For starting the MCP server in Linux:

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

, or in Windows:

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
$env:PATH += ";C:\Users\ferfd\.local\bin"
```

Then, for creating the MCP server, execute:

```bash
# Create a new directory for our project
uv init mcp
cd mcp

# Create virtual environment and activate it
uv venv
source .venv/bin/activate

# Install dependencies
uv add "mcp[cli]" httpx

# Create our server file
touch mcp.py
```

Or in windows:
```powershell
# Create a new directory for our project
uv init mcp-server
cd mcp-server

# Create virtual environment and activate it
uv venv
.venv\Scripts\activate

# Install dependencies
uv add mcp[cli] httpx

# Create our server file
new-item mcp-server.py
```

Finally, remove boilerplate files:

```bash
# Remove boilerplate files
# On Windows:
del main.py
# On Unix or macOS:
rm main.py
```