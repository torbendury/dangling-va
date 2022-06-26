# kubectl plugin: dangling-va

A simple and fast plugin (written in `bash`) to get a list of dangling `VolumeAttachment` resources that refer to nodes which do not (longer) exist.

This plugin was written by my own demand and is always subject to change.

## Installation

To install the project, either download the repository as a ZIP file or clone it. Afterwards, you can use the `install` script (might need root to move the plugin to the right directory) or just move the `kubectl-dangling_va` script to the kubectl plugin directory.

```bash
git clone git@github.com:torbendury/dangling-va.git
cd dangling-va
./install # or sudo ./install, depending on your user permissions
```

## Use Cases and basic usage

The plugin is mostly used for debugging faulty CSI drivers that are not capable of cleanly dismounting volumes e.g. after node deletion.

The plugin offers a `help` subcommand which shows the implemented functionality.

To get a list of all available commands, take a look at the help:

```bash
$ kubectl dangling-va help

Usage: kubectl dangling-va <command>

Available commands:

list            List all dangling VolumeAttachments that refer to a node which does not exist.
delete          Delete all dangling VolumeAttachments that refer to a node which does not exist.
help            Print this help
version         Print the current installed plugin version
```

## Features

- List dangling `VolumeAttachment` resources
- _TO BE DONE: delete dangling_`VolumeAttachments`

## Feedback

If you have any feedback, please reach out to me at [torben@torbendury.de](mailto:torben@torbendury.de).

## Contributing

Contributions are always welcome!

See [`CONTRIBUTING.md`](CONTRIBUTING.md) (to be done) for ways to get started.
