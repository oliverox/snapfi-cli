oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![Downloads/week](https://img.shields.io/npm/dw/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![License](https://img.shields.io/npm/l/oclif-hello-world.svg)](https://github.com/oclif/hello-world/blob/main/package.json)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g snapfi-cli
$ snapfi-cli COMMAND
running command...
$ snapfi-cli (--version)
snapfi-cli/0.0.0 darwin-arm64 node-v16.13.1
$ snapfi-cli --help [COMMAND]
USAGE
  $ snapfi-cli COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`snapfi-cli hello PERSON`](#snapfi-cli-hello-person)
* [`snapfi-cli hello world`](#snapfi-cli-hello-world)
* [`snapfi-cli help [COMMANDS]`](#snapfi-cli-help-commands)
* [`snapfi-cli plugins`](#snapfi-cli-plugins)
* [`snapfi-cli plugins:install PLUGIN...`](#snapfi-cli-pluginsinstall-plugin)
* [`snapfi-cli plugins:inspect PLUGIN...`](#snapfi-cli-pluginsinspect-plugin)
* [`snapfi-cli plugins:install PLUGIN...`](#snapfi-cli-pluginsinstall-plugin-1)
* [`snapfi-cli plugins:link PLUGIN`](#snapfi-cli-pluginslink-plugin)
* [`snapfi-cli plugins:uninstall PLUGIN...`](#snapfi-cli-pluginsuninstall-plugin)
* [`snapfi-cli plugins:uninstall PLUGIN...`](#snapfi-cli-pluginsuninstall-plugin-1)
* [`snapfi-cli plugins:uninstall PLUGIN...`](#snapfi-cli-pluginsuninstall-plugin-2)
* [`snapfi-cli plugins update`](#snapfi-cli-plugins-update)

## `snapfi-cli hello PERSON`

Say hello

```
USAGE
  $ snapfi-cli hello PERSON -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/oliverox/snapfi-cli/blob/v0.0.0/dist/commands/hello/index.ts)_

## `snapfi-cli hello world`

Say hello world

```
USAGE
  $ snapfi-cli hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ snapfi-cli hello world
  hello world! (./src/commands/hello/world.ts)
```

## `snapfi-cli help [COMMANDS]`

Display help for snapfi-cli.

```
USAGE
  $ snapfi-cli help [COMMANDS] [-n]

ARGUMENTS
  COMMANDS  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for snapfi-cli.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.2.4/src/commands/help.ts)_

## `snapfi-cli plugins`

List installed plugins.

```
USAGE
  $ snapfi-cli plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ snapfi-cli plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.3.2/src/commands/plugins/index.ts)_

## `snapfi-cli plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ snapfi-cli plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ snapfi-cli plugins add

EXAMPLES
  $ snapfi-cli plugins:install myplugin 

  $ snapfi-cli plugins:install https://github.com/someuser/someplugin

  $ snapfi-cli plugins:install someuser/someplugin
```

## `snapfi-cli plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ snapfi-cli plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ snapfi-cli plugins:inspect myplugin
```

## `snapfi-cli plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ snapfi-cli plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ snapfi-cli plugins add

EXAMPLES
  $ snapfi-cli plugins:install myplugin 

  $ snapfi-cli plugins:install https://github.com/someuser/someplugin

  $ snapfi-cli plugins:install someuser/someplugin
```

## `snapfi-cli plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ snapfi-cli plugins:link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ snapfi-cli plugins:link myplugin
```

## `snapfi-cli plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ snapfi-cli plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ snapfi-cli plugins unlink
  $ snapfi-cli plugins remove
```

## `snapfi-cli plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ snapfi-cli plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ snapfi-cli plugins unlink
  $ snapfi-cli plugins remove
```

## `snapfi-cli plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ snapfi-cli plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ snapfi-cli plugins unlink
  $ snapfi-cli plugins remove
```

## `snapfi-cli plugins update`

Update installed plugins.

```
USAGE
  $ snapfi-cli plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
