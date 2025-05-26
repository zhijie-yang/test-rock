# Rocks template repo

This repository template provides a basic setup to help you get started quickly with developing your own rock(s).

## Table of Contents
- [Setup Instructions](#setup-instructions)
- [Directory Structure](#directory-structure)
- [Building the Rock](#building-the-rock)

## Setup Instructions

### 1. Start a new repository from this template

Check GitHub's documentation on [creating a repository from a template](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template)

### 2. Customize the Template

This template comes with a basic setup to get you started. Here's what you need to customize:

- **`rockcraft.yaml`**: This is your rock's [recipe](https://documentation.ubuntu.com/rockcraft/en/stable/reference/rockcraft.yaml/)! Adjust its contents, as well as its parent directories' names according to your rock's name and version.
- **`SECURITY.md.template`**: Edit the template with your repo's details and set the security policy by renaming this file to `SECURITY.md`.
- **`CODEOWNERS`**: Optional, but recommended. Read more about [CODEOWNERS](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners).

## Directory Structure

Here's an overview of the directory structure of the repository:

```
rocks/                        # Directory containing all rocks and their versions
  └─ my-rock/                 # Directory containing all versions of a single rock
     └─ 0.1                   # Directory containing the rock project file for a specific version
        └─ rockcraft.yaml     # Rock project file
.gitignore
CODEOWNERS                    
README.md                     # Top level document containing this specification
SECURITY.md.template          # Security policy template
```

## Building, testing and uploading the Rock

To build, test and upload the rock to GHCR, simply commit your `rockcraft.yaml`
file and check the GitHub actions.

> [!NOTE]
> Before committing your `rockcraft.yaml`, it is recommended that you `pack` it
> with [Rockcraft](https://snapcraft.io/rockcraft) run a smoke test locally.
> Check the [Rockcraft documentation](https://documentation.ubuntu.com/rockcraft) to learn more.

## Sync with template

A `Makefile` is provided to sync the repository with the latest template changes. To do so, simply run:

```bash
make sync-with-template
```
