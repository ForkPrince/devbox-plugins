# Devbox Plugins

This repository includes plugins for configuring packages using Devbox.

## Available Plugins

* CouchDB

## How to Use

Each subfolder contains a plugin for a specific package. To use a plugin, add the following reference to the `include` section of your `devbox.json` file.

```json
"include": [
    "github:forkprince/devbox-plugins?dir=<plugin-name>"
],
```
