Dependency Validator
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
$ npm install -g dependency-validator
$ dep COMMAND
running command...
$ dep (--version)
dependency-validator/0.0.0 darwin-x64 node-v16.14.2
$ dep --help [COMMAND]
USAGE
  $ dep COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`dep hello PERSON`](#dep-hello-person)
* [`dep hello world`](#dep-hello-world)
* [`dep help [COMMAND]`](#dep-help-command)
* [`dep plugins`](#dep-plugins)
* [`dep plugins:install PLUGIN...`](#dep-pluginsinstall-plugin)
* [`dep plugins:inspect PLUGIN...`](#dep-pluginsinspect-plugin)
* [`dep plugins:install PLUGIN...`](#dep-pluginsinstall-plugin-1)
* [`dep plugins:link PLUGIN`](#dep-pluginslink-plugin)
* [`dep plugins:uninstall PLUGIN...`](#dep-pluginsuninstall-plugin)
* [`dep plugins:uninstall PLUGIN...`](#dep-pluginsuninstall-plugin-1)
* [`dep plugins:uninstall PLUGIN...`](#dep-pluginsuninstall-plugin-2)
* [`dep plugins update`](#dep-plugins-update)

## `dep hello PERSON`

Say hello

```
USAGE
  $ dep hello [PERSON] -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Whom is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/rkesters/dependency-validator/blob/v0.0.0/dist/commands/hello/index.ts)_

## `dep hello world`

Say hello world

```
USAGE
  $ dep hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ oex hello world
  hello world! (./src/commands/hello/world.ts)
```

## `dep help [COMMAND]`

Display help for dep.

```
USAGE
  $ dep help [COMMAND] [-n]

ARGUMENTS
  COMMAND  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for dep.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.1.12/src/commands/help.ts)_

## `dep plugins`

List installed plugins.

```
USAGE
  $ dep plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ dep plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.0.11/src/commands/plugins/index.ts)_

## `dep plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ dep plugins:install PLUGIN...

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
  $ dep plugins add

EXAMPLES
  $ dep plugins:install myplugin 

  $ dep plugins:install https://github.com/someuser/someplugin

  $ dep plugins:install someuser/someplugin
```

## `dep plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ dep plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ dep plugins:inspect myplugin
```

## `dep plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ dep plugins:install PLUGIN...

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
  $ dep plugins add

EXAMPLES
  $ dep plugins:install myplugin 

  $ dep plugins:install https://github.com/someuser/someplugin

  $ dep plugins:install someuser/someplugin
```

## `dep plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ dep plugins:link PLUGIN

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
  $ dep plugins:link myplugin
```

## `dep plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ dep plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ dep plugins unlink
  $ dep plugins remove
```

## `dep plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ dep plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ dep plugins unlink
  $ dep plugins remove
```

## `dep plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ dep plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ dep plugins unlink
  $ dep plugins remove
```

## `dep plugins update`

Update installed plugins.

```
USAGE
  $ dep plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
