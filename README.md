# Sh-Lab

![License](https://img.shields.io/github/license/theahmadrezza/Sh-Lab?style=flat-square)
![ShellCheck](https://img.shields.io/badge/linted%20with-ShellCheck-brightgreen?style=flat-square)
![shfmt](https://img.shields.io/badge/formatted%20with-shfmt-blue?style=flat-square)
![Bash](https://img.shields.io/badge/Bash-5.0%2B-lightgrey?style=flat-square)

> ***Where curiosity turns into craft.***

A local sandbox for developing **Bash** scripts using professional practices — strict mode, **ShellCheck** linting, **shfmt** formatting, and a clean modular structure.

![Sh-Lab banner](assets/banner.webp "I really love GNU/Linux.")

## About

**Sh-Lab** is a personal sandbox for practicing reliable Bash scripting: strict error handling, static analysis, consistent formatting, and clean modular structure. Every script follows the same conventions, even when it only prints `Hello, world!`.

## Prerequisites

| Tool | Recommended Version | Purpose |
| --- | --- | --- |
| ShellCheck | 0.9+ | Static analysis |
| shfmt | 3.7+ | Consistent formatting |
| Bash | 5.0+ | Runtime for all scripts |

Install on Debian/Ubuntu

1. **Install ShellCheck**

    Follow the instructions on the official [GitHub page](https://github.com/koalaman/shellcheck "ShellCheck official GitHub page"), or run

    ```bash
    sudo apt install shellcheck
    ```

2. **Install shfmt**

    Follow the instructions on the official [GitHub page](https://github.com/mvdan/sh "shfmt official GitHub page"), or run

    ```bash
    sudo apt install shfmt
    ```

3. **Verify the installed versions**

    ```bash
    shellcheck --version
    shfmt --version
    bash --version
    ```

## Project Structure

```text
Sh-Lab/
├── .vscode
│   └── settings.json
├── assets
│   └── banner.webp
├── bin
│   ├── shellcheck-v0.11.0
│   └── shfmt-v3.14.1
├── docs
│   └── BashReferenceManual.pdf
├── scripts
│   └── git_squash_all_history.sh
├── src
│   └── main.sh
├── .editorconfig
├── .gitignore
├── .shellcheckrc
├── LICENSE
└── README.md
```

| Path | Description |
| --- | --- |
| `src/main.sh` | Entry point. Runs under strict mode (`set -euo pipefail`) and prints a greeting to `stdout`. |
| `.shellcheckrc` | ShellCheck configuration shared by the editor and local runs. |
| `.editorconfig` | Whitespace and indentation rules enforced across editors. |
| `.vscode/settings.json` | Workspace settings wiring ShellCheck and shfmt into VS Code. |

## Getting Started

1. **Clone the repository**

    ```bash
    git clone https://github.com/theahmadrezza/Sh-Lab.git
    ```

2. **Navigate to the project**

    ```bash
    cd Sh-Lab
    ```

3. **Make the entry point executable**

    ```bash
    chmod +x src/main.sh
    ```

4. **Run the entry point**

    ```bash
    ./src/main.sh
    ```

Expected output

```text
Hello, world!
```

## Contributing

This is a personal learning repository, but suggestions and corrections are
welcome. Before opening a pull request

1. **Run ShellCheck on every changed script**

    ```bash
    shellcheck src/*.sh
    ```

2. **Format with shfmt**

    ```bash
    shfmt -w -i 4 -ci src/
    ```

Keep scripts under strict mode (`set -euo pipefail`) and one concern per script. Open an [issue](https://github.com/theahmadrezza/Sh-Lab/issues) first for larger changes.

## License

Released under the MIT License — see [LICENSE](LICENSE) for details.
