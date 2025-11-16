# Python Dev Container Template

A ready-to-use Python development environment template using Docker Dev Containers, UV package manager, and modern tooling.

## 🚀 Features

- **Python 3.12** - Latest Python in a Debian container
- **UV** - Fast Python package installer and resolver
- **Ruff** - Lightning-fast linter and formatter
- **Pre-commit hooks** - Automated code quality checks
- **Type checking** - Mypy with strict mode
- **Testing** - Pytest with coverage
- **VS Code extensions** - Pre-configured development tools
- **Catppuccin Frappé theme** - Beautiful color scheme

## 📋 Prerequisites

### macOS or Windows:
- [Docker Desktop](https://www.docker.com/products/docker-desktop) - Installed and running
- [VS Code](https://code.visualstudio.com/) - Latest version
- [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) - Install in VS Code

## 🎯 Quick Start

### Step 1: Create New Project from Template

1. Click the **"Use this template"** button at the top of this repository
2. Choose **"Create a new repository"**
3. Name your new project (e.g., `my-scraping-project`)
4. Choose public or private
5. Click **"Create repository"**

### Step 2: Clone and Open

**macOS:**
```bash
# Clone your new repository
git clone https://github.com/YOUR-USERNAME/YOUR-PROJECT-NAME.git
cd YOUR-PROJECT-NAME

# Open in VS Code
code .
```

**Windows:**
```bash
# Clone your new repository
git clone https://github.com/YOUR-USERNAME/YOUR-PROJECT-NAME.git
cd YOUR-PROJECT-NAME

# Open in VS Code
code .
```

### Step 3: Open in Dev Container

When VS Code opens, you'll see a notification:

> **"Folder contains a Dev Container configuration file. Reopen folder to develop in a container"**

Click **"Reopen in Container"**

*Alternatively:*
- Press `Cmd+Shift+P` (Mac) or `Ctrl+Shift+P` (Windows)
- Type: **"Dev Containers: Reopen in Container"**
- Press Enter

### Step 4: Wait for Container Build

First time setup takes 2-3 minutes:
- ✅ Docker builds the container
- ✅ Installs UV and Python
- ✅ Creates project directories
- ✅ Installs dependencies
- ✅ Sets up pre-commit hooks
- ✅ Installs VS Code extensions

### Step 5: Start Coding! 🎉

Your development environment is ready with:
```
your-project/
├── .devcontainer/       # Container configuration
├── src/                 # Your Python code goes here
├── tests/               # Your tests go here
├── .vscode/             # VS Code settings
├── pyproject.toml       # Dependencies and configuration
├── .pre-commit-config.yaml  # Code quality hooks
└── .gitignore           # Git ignore rules
```

## 📦 Adding Dependencies

### Runtime Dependencies
Edit `pyproject.toml`:
```toml
dependencies = [
    "rich>=13.7.0",
    "python-dotenv>=1.0.0",
    "requests>=2.31.0",        # Add your packages here
    "beautifulsoup4>=4.12.0",  # Example for web scraping
]
```

Then in the terminal:
```bash
uv sync --all-extras --dev
```

### Development Dependencies
```toml
[project.optional-dependencies]
dev = [
    "pytest>=7.4.0",
    "pytest-cov>=4.1.0",
    "mypy>=1.7.0",
    "ruff>=0.1.0",
    "pre-commit>=3.5.0",
    "ipython>=8.18.0",  # Add dev tools here
]
```

## 🧪 Running Tests

```bash
# Run all tests
pytest

# Run with coverage
pytest --cov=src

# Run specific test file
pytest tests/test_main.py
```

## 🎨 Code Quality

Pre-commit hooks run automatically on `git commit`:

```bash
# Manual run on all files
pre-commit run --all-files

# Run specific hook
pre-commit run ruff --all-files
```

## 🔧 Included Tools

| Tool | Purpose |
|------|---------|
| **UV** | Fast package management |
| **Ruff** | Linting and formatting |
| **Mypy** | Static type checking |
| **Pytest** | Testing framework |
| **Pre-commit** | Git hooks for code quality |
| **Rich** | Beautiful terminal output |
| **Python-dotenv** | Environment variable management |

## 📝 VS Code Extensions Included

- Python & Pylance - Language support
- Ruff - Linting/formatting
- Mypy - Type checking
- GitHub Copilot - AI assistance
- GitLens - Enhanced Git
- Even Better TOML - Config editing
- Markdown Mermaid - Diagrams
- Catppuccin theme pack

## 🗂️ Project Structure

```
.
├── .devcontainer/
│   ├── devcontainer.json    # VS Code dev container config
│   └── Dockerfile            # Container image definition
├── .vscode/                  # VS Code workspace settings
├── src/                      # Your Python source code
│   ├── __init__.py
│   └── main.py
├── tests/                    # Your test files
│   └── test_main.py
├── .gitignore                # Files to ignore in git
├── .pre-commit-config.yaml   # Pre-commit hooks config
├── pyproject.toml            # Project dependencies and settings
└── README.md                 # This file
```

## 💡 Tips

### First Time Using Dev Containers?

1. Make sure Docker Desktop is **running** (check system tray/menu bar)
2. The first build takes a few minutes - subsequent opens are instant
3. All your files are on your local machine (bind mounted)
4. Terminal in VS Code runs inside the container

### Customizing

**Change Python version:**
- Edit `.devcontainer/Dockerfile`: Change `FROM python:3.12-slim-bookworm`
- Edit `pyproject.toml`: Change `requires-python = ">=3.12"`

**Add VS Code extensions:**
- Edit `.devcontainer/devcontainer.json` → `extensions` array

**Change theme:**
- Edit `.devcontainer/devcontainer.json` → `workbench.colorTheme`

### Troubleshooting

**Container won't build:**
- Ensure Docker Desktop is running
- Try: `Cmd/Ctrl+Shift+P` → "Dev Containers: Rebuild Container"

**Dependencies not installing:**
- Check `pyproject.toml` syntax
- Run: `uv sync --all-extras --dev` in terminal

**Pre-commit not working:**
- Run: `pre-commit install` in terminal
- Check hooks: `pre-commit run --all-files`

## 🔄 Reusing This Template

This is designed to be a **disposable environment**. For each new project:

1. Use the template to create a new repository
2. Clone it
3. Open in container
4. Code your project
5. Commit and push

Each project gets its own isolated container - no conflicts between projects!

## 📚 Learn More

- [UV Documentation](https://docs.astral.sh/uv/)
- [Ruff Documentation](https://docs.astral.sh/ruff/)
- [Dev Containers](https://code.visualstudio.com/docs/devcontainers/containers)
- [Pre-commit](https://pre-commit.com/)

## 📄 License
MIT
