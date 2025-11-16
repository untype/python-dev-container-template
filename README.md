```
╔═══════════════════════════════════════════════════════════════════════════╗
║                                                                           ║
║   ██████╗ ██╗   ██╗████████╗██╗  ██╗ ██████╗ ███╗   ██╗                ║
║   ██╔══██╗╚██╗ ██╔╝╚══██╔══╝██║  ██║██╔═══██╗████╗  ██║                ║
║   ██████╔╝ ╚████╔╝    ██║   ███████║██║   ██║██╔██╗ ██║                ║
║   ██╔═══╝   ╚██╔╝     ██║   ██╔══██║██║   ██║██║╚██╗██║                ║
║   ██║        ██║      ██║   ██║  ██║╚██████╔╝██║ ╚████║                ║
║   ╚═╝        ╚═╝      ╚═╝   ╚═╝  ╚═╝ ╚═════╝ ╚═╝  ╚═══╝                ║
║                                                                           ║
║              ╔╦╗╔═╗╦  ╦  ╔═╗╔═╗╔╗╔╔╦╗╔═╗╦╔╗╔╔═╗╦═╗                      ║
║               ║║║╣ ╚╗╔╝  ║  ║ ║║║║ ║ ╠═╣║║║║║╣ ╠╦╝                      ║
║              ═╩╝╚═╝ ╚╝   ╚═╝╚═╝╝╚╝ ╩ ╩ ╩╩╝╚╝╚═╝╩╚═                      ║
║                                                                           ║
║          > PYTHON 3.12 + UV + RUFF + PRE-COMMIT HOOKS <                  ║
║          > FULLY DOCKERIZED DEVELOPMENT ENVIRONMENT <                    ║
║                                                                           ║
╚═══════════════════════════════════════════════════════════════════════════╝
```

## >> SYSTEM_SPECS

```
[CORE_ENGINE]
├─ Python 3.12        │ Latest runtime environment
├─ UV Package Manager │ Hyper-speed dependency resolution
├─ Ruff Linter        │ Lightning-fast code analysis
├─ Docker Container   │ Isolated development sandbox

[QUALITY_PROTOCOLS]
├─ Pre-commit Hooks   │ Automated quality gates
├─ Mypy Type Checker  │ Strict type enforcement
├─ Pytest Framework   │ Test-driven development
└─ Code Coverage      │ Quality metrics tracking

[INTERFACE_LAYER]
├─ VS Code Extensions │ Optimized IDE configuration
├─ Catppuccin Theme   │ Cyberpunk-aesthetic workspace
├─ Python Language    │ Full IntelliSense support
└─ Git Integration    │ Version control automation
```

---

## >> PREREQUISITES

```
┌─────────────────────────────────────────────────────────────┐
│  REQUIRED SOFTWARE STACK                                    │
├─────────────────────────────────────────────────────────────┤
│  [ ] Docker/Podman       :: Container runtime engine       │
│  [ ] VS Code             :: Primary development interface   │
│  [ ] Dev Containers Ext  :: Remote container connector      │
└─────────────────────────────────────────────────────────────┘
```

**INSTALLATION LINKS:**
- Docker Desktop: `https://docker.com/products/docker-desktop`
- Podman Desktop: `https://podman-desktop.io`
- VS Code: `https://code.visualstudio.com`
- Dev Containers: `ms-vscode-remote.remote-containers`

---

## >> QUICK_START_PROTOCOL

### PHASE 1: TEMPLATE INITIALIZATION

```
┌──────────────────────────────────────────────────┐
│ [1] Navigate to repository homepage             │
│ [2] Click "Use this template" button            │
│ [3] Select "Create a new repository"            │
│ [4] Enter project name (e.g., scraper-alpha-01) │
│ [5] Choose visibility: [PUBLIC] / [PRIVATE]     │
│ [6] Execute: "Create repository"                │
└──────────────────────────────────────────────────┘
```

### PHASE 2: LOCAL DEPLOYMENT

**MACOS / LINUX:**
```bash
# Clone repository to local filesystem
$ git clone https://github.com/YOUR-USERNAME/YOUR-PROJECT-NAME.git
$ cd YOUR-PROJECT-NAME

# Launch VS Code interface
$ code .
```

**WINDOWS:**
```cmd
# Clone repository to local filesystem
> git clone https://github.com/YOUR-USERNAME/YOUR-PROJECT-NAME.git
> cd YOUR-PROJECT-NAME

# Launch VS Code interface
> code .
```

### PHASE 3: CONTAINER ACTIVATION

```
┌─────────────────────────────────────────────────────────┐
│  NOTIFICATION DETECTED:                                 │
│  "Dev Container configuration found. Reopen in          │
│   container to activate development environment?"       │
│                                                          │
│  ACTION: Click [Reopen in Container]                    │
└─────────────────────────────────────────────────────────┘

 ALTERNATIVE METHOD:
 > Press: [CMD/CTRL + SHIFT + P]
 > Type: "Dev Containers: Reopen in Container"
 > Execute: [ENTER]
```

### PHASE 4: SYSTEM INITIALIZATION

```
[████████████████████████████████████] 100%

CONTAINER BUILD SEQUENCE:
├─ [OK] Docker/Podman image construction
├─ [OK] UV package manager installation
├─ [OK] Python 3.12 environment setup
├─ [OK] Directory structure generation
├─ [OK] Dependency resolution & install
├─ [OK] Pre-commit hooks configuration
└─ [OK] VS Code extensions deployment

>> SYSTEM READY FOR OPERATION <<
```

### PHASE 5: PROJECT STRUCTURE

```
YOUR-PROJECT/
│
├── .devcontainer/
│   ├── devcontainer.json     # Container configuration matrix
│   └── Dockerfile             # Image build specifications
│
├── .vscode/
│   └── settings.json          # Workspace preferences
│
├── src/                       # >> PRIMARY CODE DIRECTORY
│   ├── __init__.py
│   └── main.py
│
├── tests/                     # >> TEST SUITE DIRECTORY
│   └── test_main.py
│
├── pyproject.toml             # Dependency manifest
├── .pre-commit-config.yaml    # Quality gate definitions
└── .gitignore                 # VCS exclusion rules
```

---

## >> DEPENDENCY_MANAGEMENT

### RUNTIME PACKAGES

Edit `pyproject.toml`:
```toml
dependencies = [
    "rich>=13.7.0",              # Terminal enhancement
    "python-dotenv>=1.0.0",      # Environment variables
    "requests>=2.31.0",          # HTTP client
    "beautifulsoup4>=4.12.0",    # HTML parsing
]
```

Apply changes:
```bash
$ uv sync --all-extras --dev
```

### DEVELOPMENT PACKAGES

```toml
[project.optional-dependencies]
dev = [
    "pytest>=7.4.0",
    "pytest-cov>=4.1.0",
    "mypy>=1.7.0",
    "ruff>=0.1.0",
    "pre-commit>=3.5.0",
    "ipython>=8.18.0",
]
```

---

## >> TESTING_SUITE

```bash
# Execute full test battery
$ pytest

# Generate coverage report
$ pytest --cov=src

# Target specific test module
$ pytest tests/test_main.py
```

---

## >> CODE_QUALITY_GATES

Pre-commit hooks execute automatically on `git commit`:

```bash
# Manual execution on all files
$ pre-commit run --all-files

# Execute specific quality check
$ pre-commit run ruff --all-files
```

**AUTOMATED CHECKS:**
```
┌─────────────────────────────────────────────┐
│ [RUN] Trailing whitespace removal          │
│ [RUN] End-of-file fixer                     │
│ [RUN] YAML syntax validation                │
│ [RUN] Large file detection                  │
│ [RUN] Ruff linter                           │
│ [RUN] Ruff formatter                        │
│ [RUN] Mypy type checker                     │
└─────────────────────────────────────────────┘
```

---

## >> TOOLCHAIN_INVENTORY

```
╔══════════════════════════════════════════════════════════╗
║ TOOL            │ FUNCTION                               ║
╠══════════════════════════════════════════════════════════╣
║ UV              │ Hyper-fast package management          ║
║ Ruff            │ Code linting & formatting              ║
║ Mypy            │ Static type analysis                   ║
║ Pytest          │ Test execution framework               ║
║ Pre-commit      │ Git hook automation                    ║
║ Rich            │ Enhanced terminal output               ║
║ Python-dotenv   │ Environment configuration              ║
╚══════════════════════════════════════════════════════════╝
```

---

## >> INSTALLED_EXTENSIONS

```
[LANGUAGE_SUPPORT]
├─ Python              :: Core language support
├─ Pylance             :: Advanced IntelliSense
└─ Python Debugger     :: Debugging interface

[CODE_QUALITY]
├─ Ruff                :: Linting & formatting
├─ Mypy Type Checker   :: Type validation
└─ Even Better TOML    :: Config file support

[PRODUCTIVITY]
├─ GitHub Copilot      :: AI-powered coding
├─ GitLens             :: Enhanced Git integration
├─ Markdown Mermaid    :: Diagram rendering
└─ Catppuccin Theme    :: Aesthetic interface
```

---

## >> CUSTOMIZATION_MATRIX

### CHANGE PYTHON VERSION

```toml
# .devcontainer/Dockerfile
FROM python:3.12-slim-bookworm  # <- Modify version here

# pyproject.toml
requires-python = ">=3.12"      # <- Update requirement
```

### ADD EXTENSIONS

```json
// .devcontainer/devcontainer.json
"extensions": [
  "your.extension.id"
]
```

### MODIFY THEME

```json
// .devcontainer/devcontainer.json
"workbench.colorTheme": "Your Theme Name"
```

---

## >> TROUBLESHOOTING_PROTOCOLS

```
ERROR: Container build failure
├─ DIAGNOSIS: Docker/Podman not running
└─ SOLUTION: Launch Docker Desktop or Podman Desktop, retry build

ERROR: Dependency installation failure
├─ DIAGNOSIS: Invalid pyproject.toml syntax
└─ SOLUTION: Validate TOML, run 'uv sync --all-extras --dev'

ERROR: Pre-commit hooks not executing
├─ DIAGNOSIS: Hooks not installed
└─ SOLUTION: Execute 'pre-commit install'
```

---

## >> DEPLOYMENT_WORKFLOW

```
┌───────────────────────────────────────────────────┐
│  FOR EACH NEW PROJECT:                            │
├───────────────────────────────────────────────────┤
│  [1] Use template → Create new repository         │
│  [2] Clone to local machine                       │
│  [3] Open in VS Code                              │
│  [4] Reopen in container                          │
│  [5] Write code                                   │
│  [6] Commit & push                                │
│                                                    │
│  >> Each project = Isolated container instance    │
│  >> Zero dependency conflicts                     │
│  >> Complete environment reproducibility          │
└───────────────────────────────────────────────────┘
```

---

## >> DOCUMENTATION_LINKS

```
[REFERENCE_MATERIALS]
├─ UV Documentation        :: https://docs.astral.sh/uv/
├─ Ruff Documentation      :: https://docs.astral.sh/ruff/
├─ Dev Containers Guide    :: https://code.visualstudio.com/docs/devcontainers/containers
└─ Pre-commit Handbook     :: https://pre-commit.com/
```

---

## >> LICENSE_DECLARATION

```
┌─────────────────────────────────────────────────────────┐
│  MIT License                                            │
│                                                          │
│  Copyright (c) 2025 untype                              │
│                                                          │
│  Permission is hereby granted, free of charge, to any   │
│  person obtaining a copy of this software and           │
│  associated documentation files (the "Software"), to    │
│  deal in the Software without restriction, including    │
│  without limitation the rights to use, copy, modify,    │
│  merge, publish, distribute, sublicense, and/or sell    │
│  copies of the Software, and to permit persons to whom  │
│  the Software is furnished to do so, subject to the     │
│  following conditions:                                  │
│                                                          │
│  The above copyright notice and this permission notice  │
│  shall be included in all copies or substantial         │
│  portions of the Software.                              │
│                                                          │
│  THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF  │
│  ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT        │
│  LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS  │
│  FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO    │
│  EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE │
│  FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN  │
│  AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING      │
│  FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE │
│  USE OR OTHER DEALINGS IN THE SOFTWARE.                 │
└─────────────────────────────────────────────────────────┘
```

---

```
╔═══════════════════════════════════════════════════════════════════════════╗
║                                                                           ║
║                    >> HAPPY CODING, DEVELOPER <<                          ║
║                                                                           ║
║                  [PYTHON 3.12 + UV + RUFF + DOCKER/PODMAN]               ║
║                                                                           ║
╚═══════════════════════════════════════════════════════════════════════════╝
```
