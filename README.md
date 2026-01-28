# Claude Code Agent Framework

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Streamline your development workflow by leveraging Claude Code's intelligent code generation capabilities to rapidly prototype, test, and compare implementations across multiple programming languages and frameworks.

## 📖 Overview

Claude Code is an agentic coding tool that lives in your terminal, understands your codebase, and helps you code faster by executing routine tasks, explaining complex code, and handling git workflows - all through natural language commands. It embeds Claude Opus 4—the same model our researchers and engineers use—right in your terminal with deep codebase awareness and the ability to edit files and run commands directly in your environment.

## 📄 What Claude Code Can Do

- **Build features from descriptions**: Tell Claude what you want to build in plain English. It will make a plan, write the code, and ensure it works
- **Debug and fix issues**: Describe a bug or paste an error message. Claude Code will analyze your codebase, identify the problem, and implement a fix
- **Navigate any codebase**: Ask anything about your team's codebase, and get thoughtful answers back
- **Make coordinated changes**: Makes coordinated changes across multiple files
- **Automate tedious tasks**: Fix lint issues, resolve merge conflicts, and write release notes

## ⚠️ Prerequisites

Before installing Claude Code, ensure you have:

- **[Node.js](https://nodejs.org/en/download/) 18 or newer**
- **VS Code** installed on your system
- A **Claude subscription** (Pro, Max) or **Anthropic API key**
- **Git** installed and configured
- A stable internet connection

## 💾 Installation

### Step 1: Install Claude Code CLI

Open your terminal and run:

```bash
npm install -g @anthropic-ai/claude-code
```

### Step 2: Initial Authentication

Navigate to any project directory and run Claude Code for the first time:

```bash
cd your-project-directory
claude
```

You'll complete a one-time OAuth process with your Claude Max or Anthropic Console account. Follow the prompts to authenticate with your Anthropic account.

### Step 3: VS Code Extension Setup

Open VS Code, open the integrated terminal, and run `claude` - the extension will auto-install.

Alternatively, you can manually install the extension:

1. Open VS Code
2. Go to Extensions (Ctrl+Shift+X / Cmd+Shift+X)
3. Search for "Claude Code for VSCode" by Anthropic
4. Click Install
5. Restart VS Code

## 🔗 VS Code Integration Features

Once installed, you'll have access to these powerful features:

### Quick Launch

- **Keyboard shortcut**: Use `Cmd+Esc` (Mac) or `Ctrl+Esc` (Windows/Linux) to open Claude Code directly from your editor
- **UI button**: Click the Claude Code button in the VS Code interface

### Smart Context Sharing

- **Selection context**: The current selection/tab in the IDE is automatically shared with Claude Code
- **Diagnostic sharing**: Diagnostic errors (lint, syntax, etc.) from the IDE are automatically shared with Claude as you work
- **File reference shortcuts**: Use `Cmd+Option+K` (Mac) or `Alt+Ctrl+K` (Linux/Windows) to insert file references (e.g., @File#L1-99)

### Diff Viewing

- Code changes can be displayed directly in the IDE diff viewer instead of the terminal
- Configure this in `/config` within Claude Code

## 🔧 Configuration

### Basic Configuration

1. **Run configuration setup**:

   ```bash
   claude
   /config
   ```

2. **Set diff tool to auto** for automatic IDE detection:

   ```bash
   Set diff tool to: auto
   ```

### Project-Specific Setup

Create a `CLAUDE.md` file in your project root to provide Claude with example project context:

```markdown
# Project Setup for Claude Code

## Branch Naming Convention
- Use `feature/` prefix for new features
- Use `bugfix/` prefix for bug fixes
- Use `hotfix/` prefix for urgent fixes

## Environment Setup
- Node.js version: 18+
- Package manager: npm/yarn
- Testing framework: Jest

## Code Standards
- ESLint configuration in `.eslintrc.js`
- Prettier formatting enabled
- TypeScript strict mode enabled

## Known Issues
- Database connection requires VPN
- Tests require environment variables in `.env.test`
```

### Advanced Terminal Setup

Since it's a terminal interface, there are some non-obvious behaviors: Shift+Enter doesn't work by default for new lines. Just tell Claude to set up your terminal with `/terminal-setup` and it'll fix it for you.

Run this command in Claude Code:

```bash
/terminal-setup
```

## 🚀 Getting Started

Once everything is set up:

1. Open your project in VS Code
2. Open the integrated terminal
3. Run `claude`
4. Try a simple command like: "Explain the structure of this project"
5. Use `Cmd+Esc` / `Ctrl+Esc` for quick access going forward

For detailed usage examples and workflows, check the [official Claude Code documentation](https://docs.anthropic.com/en/docs/claude-code/quickstart).

## ⚡ Basic Usage

### Starting Claude Code

1. **From VS Code integrated terminal**:

   ```bash
   cd your-project
   claude
   ```

2. **From external terminal** (then connect to VS Code):

   ```bash
   cd your-project
   claude
   /ide
   ```

### Essential Commands

- `/help` - Show available commands
- `/ide` - Connect to your IDE from external terminal
- `/config` - Configure Claude Code settings
- `/terminal-setup` - Set up terminal for better experience
- `/bug` - Report issues directly to Anthropic
- `/install-github-app` - Set up automatic PR reviews

### Example Prompting

**Analyze your Codebase**:

```bash
Explain the architecture of this React app
```

**Build a New Feature**:

```bash
Create a user authentication component with login and signup forms using React hooks
```

**Debug an Issue**:

```bash
I'm getting a "Cannot read property 'map' of undefined" error in UserList.jsx. Can you find and fix it?
```

**Refactor Code**:

```bash
Refactor the authentication logic to use a custom hook
```

## 📦 License

- See MIT [LICENSE](LICENSE) for details.

## 👏 Acknowledgments

- [Anthropic](https://anthropic.com) team for the Model Context Protocol

## 🔍 Resources

- [Claude-Desktop n8n-MCP Tutorial](https://www.youtube.com/watch?v=5CccjiLLyaY&t=343s) walkthrough using the n8n-MCP through Claude Desktop
- [Claude-Code n8n-MCP Tutorial](https://www.youtube.com/watch?v=7LlQZKPBKgs) walkthrough using the n8n-MCP through Claude-Code in VSCode

## 💻 Support

**Need help?** Visit [support.anthropic.com](https://support.anthropic.com) for additional assistance or check the [Claude Code documentation](https://docs.anthropic.com/en/docs/claude-code) for the most up-to-date information.
