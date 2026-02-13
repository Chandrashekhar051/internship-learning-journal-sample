#  Development Environment Setup on macOS

## Overview

In this session, I set up a complete CLI-based development environment on macOS. The focus was on creating a clean, reproducible workflow using Homebrew for package management, UV for Python project handling, GitHub CLI for repository management, and the LLM command-line tool for interacting with AI models directly from the terminal.

This setup emphasizes working efficiently from the terminal instead of relying only on GUI tools.

---

## 1.Homebrew Installation

Homebrew acts as a package manager for macOS. It simplifies installing developer tools and managing dependencies.

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

After installation, Homebrew manages system-level developer tools.

---

## 2.GitHub CLI Installation

Instead of creating repositories manually in the browser, GitHub CLI allows managing GitHub directly from the terminal.

```bash
brew install gh
```

This enables authentication, repository creation, pull requests, and other GitHub operations via command line.

---

## 3.Managing Python Dependencies with UV

UV is a fast Python package and environment manager. It improves dependency resolution and virtual environment management.

Example command demonstrated:

```bash
uv remove flask
```

This shows how packages can be removed efficiently from a project environment.

---

## 4.Installing LLM Command-Line Tool

The LLM CLI tool allows interaction with large language models directly from the terminal.

Installed using:

```bash
brew install llm
```

---

## 4.Configuring API Access

To use the LLM tool, an API key must be configured.

```bash
llm keys set openai
```

After entering the key, a custom base URL was configured:

```bash
export OPENAI_BASE_URL=https://aipipe.org/openai/v1
```

This connects the CLI tool to the appropriate API endpoint.

---

## 5.Running Prompts from Terminal

Once configured, prompts can be executed directly:

```bash
llm "what is 2+2?"
llm "what do you think of chennai?"
```

This demonstrates how AI responses can be generated without leaving the terminal.

---

## Key Learnings

- Homebrew simplifies developer tool installation.
- GitHub CLI enables full GitHub workflow from terminal.
- UV improves Python dependency management.
- LLM CLI integrates AI capabilities into development workflow.
- API configuration is essential for secure model access.
