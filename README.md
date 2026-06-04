# A development container for Haskell

This is an opinionated [Dev Container](https://containers.dev) for Haskell.

## Features

The development container has the following features:

- **Pre-configured Cabal, Stack and HLS:** Cabal, Stack and HLS come pre-installed and pre-configured.
- **Pre-installed development tools:** The development container comes with a number of generic (Git, Neovim, SSH, etc.) and Haskell-specific (ormolu, implicit-hie, retrie, etc.) development tools pre-installed.
- **Integrated GHCi:** The development container comes with an integrated GHCi shell.
- **Offline support:** Hoogle and Hackage are included locally in the container, meaning you do not need an internet connection to find definitions or read documentation.

To open the integrated GHCi shell, press the yellow lambda symbol in the top-right corner. To search Hoogle, press <kbd>Alt</kbd> + <kbd>Shift</kbd> + <kbd>H</kbd>.

## Using with Visual Studio Code

Follow the steps below to use the Dev Container with Visual Studio Code:

1. Follow the [Getting Started](https://code.visualstudio.com/docs/remote/containers#_getting-started) instructions to configure Visual Studio Code and Docker for use with Dev Containers.
2. Clone this repository. You can checkout another branch to use a different version.
3. Open the repository using Visual Studio Code.
4. Click `Reopen in Container` when Visual Studio Code prompts you, or open the command palette (<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd> or <kbd>Cmd</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd>) and execute the command `>Dev Containers: Reopen in Container`.

> [!WARNING]
> Building the image initially may take a **long time** (30 minutes to multiple hours).

## How does it work

Visual Studio Code supports [Dev Containers](https://code.visualstudio.com/docs/remote/containers) (i.e. using a Docker image as a development environment). It automates the hassle of setting up a proper development environment.

## Troubleshooting

This section lists some common problems, and possible ways to fix these problems. If you encounter an issue not listed here, or if the fixes listed do not work for you, please [open an issue](https://github.com/marijnvanwezel/haskell-dev-env/issues/new).

- **Definitions from other files are not found.**
    - Try running `stack install` in the project directory.
- **Definitions from dependencies are not found.**
    - Try restarting Visual Studio Code.
- **Stuck on `Processing ../..`.**
    - Try running `stack build` in the project directory.
- **Code completion and/or checking is not working.**
    - Try restarting Visual Studio Code.
    - Try running `stack install` in the project directory.
- **Something else does not work.**
    - Try restarting Visual Studio Code.
    - [Open an issue](https://github.com/marijnvanwezel/haskell-dev-env/issues/new) on GitHub.

## Installed software

The container comes with the following (relevant) software pre-installed:

- [`debian:bookworm-slim`](https://hub.docker.com/_/debian) as a base image;
- [GNU Bash](https://www.gnu.org/software/bash/);
- [Git](https://git-scm.com/);
- [Neovim](https://neovim.io/);
- [GHCUp](https://www.haskell.org/ghcup/);
- The [Glasgow Haskell Compiler (GHC)](https://www.haskell.org/ghc/);
- The [Haskell Language Server (HLS)](https://github.com/haskell/haskell-language-server);
- [Stack](https://docs.haskellstack.org/en/stable/);
- [Cabal](https://www.haskell.org/cabal/).

Following VSCode extensions are automatically installed after container is started:

- [Haskell](https://marketplace.visualstudio.com/items?itemName=haskell.haskell);
- [Haskell GHCi Debugger Adapter](https://marketplace.visualstudio.com/items?itemName=phoityne.phoityne-vscode);
- [Integrated Haskell Shell](https://marketplace.visualstudio.com/items?itemName=eriksik2.vscode-ghci);
- [Hoogle for VSCode](https://marketplace.visualstudio.com/items?itemName=jcanero.hoogle-vscode);
- [Hackage Theme](https://marketplace.visualstudio.com/items?itemName=dmarticus.hackage-theme);
- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker);
- [VSCode PDF](https://marketplace.visualstudio.com/items?itemName=tomoki1207.pdf);
- [YAML](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml);
- [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one).

The development container also comes pre-installed with a number of useful packages.
