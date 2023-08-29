# Obsidian-Auto-Release

This repository is to automatically release a new obsidian plugin or a new version of it, just by typing the following in your terminal:
````
$ make release
````

## Usage
To use this, you need to copy the ``release.yml`` into your actions folder: ``.github/workflows``. Also copy the scripts, makefile, eslint config files and ``version-bump.mjs`` into your project. Also the scripts inside this ``package.json`` are required.

## Features
- Automatically fetched the last release tag, increases it. \ 
- Updates the version in ``package.json``, ``manifest.json`` and ``version.json``. \ 
- Checks if ``package.json`` and ``manifest.json`` have the same name and description and those are not empty. Also the description need to end with ``'.'`` and does not contain the words ``obsidian`` and ``plugin``.
- Use linter to fix style issues and commit those.
- Create new tag and push changes to new version and style issue fixes with tag
- In the github action creates the new release so you just need to click on the newest tag and release it. The required files are already inserted.