# Linode CLI Snap Package [![CircleCI Build Status](https://circleci.com/gh/felicianotech/linode-cli-snap.svg?style=shield)](https://circleci.com/gh/felicianotech/linode-cli-snap) [![GitHub License](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/felicianotech/linode-cli-snap/master/LICENSE)

`linode-cli` allows you to manage your Linode account from your terminal.
Create, manage, and delete Linode VPSs, domain names, and more.

This repository provides the source code for the `linode-cli` snap which is available in the [Snapcraft Store](https://snapcraft.io/linode-cli).
The snap is maintained by [@FelicianoTech](https://twitter.com/FelicianoTech) meanwhile the code for `linode-cli` itself is maintained by [Linode](https://www.linode.com/).
The upstream repository can be found [here](https://github.com/linode/linode-cli).


## Installation

`linode-cli` can be installed via snap on Ubuntu 16.04, Ubuntu 18.04+, elementary OS 5, and many Linux distros with `snapd` installed  by running:

```
sudo snap install linode-cli
```

If you don't have the `snap` command available, you might be able to find instructions for your distro [here](https://docs.snapcraft.io/core/install).
`linode-cli` is normally available via `pip` if you don't want to use Snap.


## Usage

```
linode-cli <command> <action>
```

*command* is the part of the CLI you are interacting with, for example "linodes".
You can see a list of all available commands by using `--help`:

```
linode-cli --help
```

*action* is the action you want to perform on a given command, for example "list".
You can see a list of all available actions for a command with the `--help` for
that command:

```
linode-cli linodes --help
```

Some actions don't require any parameters, but many do.  To see details on how
to invoke a specific action, use `--help` for that action:

```
linode-cli linodes create --help
```

The first time you invoke the CLI, you will be asked to configure it with a token, and optionally select some default values for "region," "image," and "type".
If you configure these defaults, you may omit them as parameters to actions and the default value will be used.


## Development

This snap can be built with Snapcraft.
On Ubuntu:

```
sudo snap install --classic snapcraft
snapcraft snap
```


## License

The code for this snap is licensed under the MIT license.
The code for `linode-cli` itself is licensed under the BSD 3-Clause "New" or "Revised" License.
This repo's license can be found [here](./LICENSE) while the license for `linode-cli` can be found [here](https://github.com/linode/linode-cli/blob/master/LICENSE).
