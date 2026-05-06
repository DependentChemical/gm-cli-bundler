# GM-CLI Standalone Builder (2026 GMRT Edition)

A lightweight, zero-dependency automation suite designed to build and maintain a standalone, portable version of the official **GameMaker CLI**.

## 🚀 Why This Exists

As of the **Spring 2026 GameMaker Update**, the shift to the **GMRT (GameMaker Runtime)** and plain-text project files opened the door for "Vibe Coding" and AI-assisted development. However, the official `gm-cli` toolchain typically requires a full Node.js installation—adding unnecessary bloat to development systems.

This repository was created to:

1. **Eliminate Bloat:** No Node.js, npm, or system-wide installers required.
2. **Enable Portability:** Compiles the CLI into a single, standalone `.exe` using the **Bun** runtime.
3. **Automate Updates:** A GitHub Action monitors the official [YoYoGames/gm-cli](https://github.com/YoYoGames/gm-cli "null") repository and builds a new executable whenever a new version is released.
4. **AI-First Workflow:** Optimized for use with agentic IDEs like **Google Antigravity**, allowing Gemini or Claude to manage builds and code checks via a single binary.

## 🛠 Features

- **Automated Sync:** Checks for upstream updates every 12 hours.
- **Native Performance:** Builds for the **GMRT** architecture (LLVM-based native compilation).
- **Minified Build:** Optimized for speed and lower memory footprint.
- **Zero Trace:** The local system stays clean; all building happens in GitHub Actions.

## 📂 Project Structure

- `.github/workflows/auto-build.yml`: The logic that clones, builds, and releases the standalone binary.
- `.gitignore`: Prevents local build artifacts from cluttering the repo.

## 📖 How to Use

1. **Download:** Go to the **Releases** tab of this repository and download the latest `gm-cli.exe`.
2. **Deploy:** Drop the `.exe` into your GameMaker project root or add it to your system PATH.
3. **Run:** Open your terminal (PowerShell or Antigravity) and use:

        .\gm-cli.exe run --runtime=gmrt

## 🤖 Vibe Coding with AI

To use this with an AI agent (like Gemini in Antigravity), simply point the agent to the standalone binary. You can use missions such as:

> 
> *"Use the standalone gm-cli.exe to perform a code check on all modified GML files before committing."*

*Created for high-performance GameMaker development without the motherfucking overhead.*


As you can clearly see this README too was fucking AI generated, boy are we lazy as fuck.