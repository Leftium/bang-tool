bang-tool
=================

CLI tools for handling bang files.


[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/bang-tool.svg)](https://npmjs.org/package/bang-tool)
[![Downloads/week](https://img.shields.io/npm/dw/bang-tool.svg)](https://npmjs.org/package/bang-tool)


<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g bang-tool
$ bang-tool COMMAND
running command...
$ bang-tool (--version)
bang-tool/0.0.0 win32-x64 node-v20.18.0
$ bang-tool --help [COMMAND]
USAGE
  $ bang-tool COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`bang-tool hello PERSON`](#bang-tool-hello-person)
* [`bang-tool hello world`](#bang-tool-hello-world)
* [`bang-tool help [COMMAND]`](#bang-tool-help-command)
* [`bang-tool plugins`](#bang-tool-plugins)
* [`bang-tool plugins add PLUGIN`](#bang-tool-plugins-add-plugin)
* [`bang-tool plugins:inspect PLUGIN...`](#bang-tool-pluginsinspect-plugin)
* [`bang-tool plugins install PLUGIN`](#bang-tool-plugins-install-plugin)
* [`bang-tool plugins link PATH`](#bang-tool-plugins-link-path)
* [`bang-tool plugins remove [PLUGIN]`](#bang-tool-plugins-remove-plugin)
* [`bang-tool plugins reset`](#bang-tool-plugins-reset)
* [`bang-tool plugins uninstall [PLUGIN]`](#bang-tool-plugins-uninstall-plugin)
* [`bang-tool plugins unlink [PLUGIN]`](#bang-tool-plugins-unlink-plugin)
* [`bang-tool plugins update`](#bang-tool-plugins-update)

## `bang-tool hello PERSON`

Say hello

```
USAGE
  $ bang-tool hello PERSON -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ bang-tool hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [src/commands/hello/index.ts](https://github.com/leftium/bang-tool/blob/v0.0.0/src/commands/hello/index.ts)_

## `bang-tool hello world`

Say hello world

```
USAGE
  $ bang-tool hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ bang-tool hello world
  hello world! (./src/commands/hello/world.ts)
```

_See code: [src/commands/hello/world.ts](https://github.com/leftium/bang-tool/blob/v0.0.0/src/commands/hello/world.ts)_

## `bang-tool help [COMMAND]`

Display help for bang-tool.

```
USAGE
  $ bang-tool help [COMMAND...] [-n]

ARGUMENTS
  COMMAND...  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for bang-tool.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v6.2.15/src/commands/help.ts)_

## `bang-tool plugins`

List installed plugins.

```
USAGE
  $ bang-tool plugins [--json] [--core]

FLAGS
  --core  Show core plugins.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ bang-tool plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.15/src/commands/plugins/index.ts)_

## `bang-tool plugins add PLUGIN`

Installs a plugin into bang-tool.

```
USAGE
  $ bang-tool plugins add PLUGIN... [--json] [-f] [-h] [-s | -v]

ARGUMENTS
  PLUGIN...  Plugin to install.

FLAGS
  -f, --force    Force npm to fetch remote resources even if a local copy exists on disk.
  -h, --help     Show CLI help.
  -s, --silent   Silences npm output.
  -v, --verbose  Show verbose npm output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into bang-tool.

  Uses npm to install plugins.

  Installation of a user-installed plugin will override a core plugin.

  Use the BANG_TOOL_NPM_LOG_LEVEL environment variable to set the npm loglevel.
  Use the BANG_TOOL_NPM_REGISTRY environment variable to set the npm registry.

ALIASES
  $ bang-tool plugins add

EXAMPLES
  Install a plugin from npm registry.

    $ bang-tool plugins add myplugin

  Install a plugin from a github url.

    $ bang-tool plugins add https://github.com/someuser/someplugin

  Install a plugin from a github slug.

    $ bang-tool plugins add someuser/someplugin
```

## `bang-tool plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ bang-tool plugins inspect PLUGIN...

ARGUMENTS
  PLUGIN...  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ bang-tool plugins inspect myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.15/src/commands/plugins/inspect.ts)_

## `bang-tool plugins install PLUGIN`

Installs a plugin into bang-tool.

```
USAGE
  $ bang-tool plugins install PLUGIN... [--json] [-f] [-h] [-s | -v]

ARGUMENTS
  PLUGIN...  Plugin to install.

FLAGS
  -f, --force    Force npm to fetch remote resources even if a local copy exists on disk.
  -h, --help     Show CLI help.
  -s, --silent   Silences npm output.
  -v, --verbose  Show verbose npm output.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Installs a plugin into bang-tool.

  Uses npm to install plugins.

  Installation of a user-installed plugin will override a core plugin.

  Use the BANG_TOOL_NPM_LOG_LEVEL environment variable to set the npm loglevel.
  Use the BANG_TOOL_NPM_REGISTRY environment variable to set the npm registry.

ALIASES
  $ bang-tool plugins add

EXAMPLES
  Install a plugin from npm registry.

    $ bang-tool plugins install myplugin

  Install a plugin from a github url.

    $ bang-tool plugins install https://github.com/someuser/someplugin

  Install a plugin from a github slug.

    $ bang-tool plugins install someuser/someplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.15/src/commands/plugins/install.ts)_

## `bang-tool plugins link PATH`

Links a plugin into the CLI for development.

```
USAGE
  $ bang-tool plugins link PATH [-h] [--install] [-v]

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help          Show CLI help.
  -v, --verbose
      --[no-]install  Install dependencies after linking the plugin.

DESCRIPTION
  Links a plugin into the CLI for development.

  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ bang-tool plugins link myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.15/src/commands/plugins/link.ts)_

## `bang-tool plugins remove [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ bang-tool plugins remove [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ bang-tool plugins unlink
  $ bang-tool plugins remove

EXAMPLES
  $ bang-tool plugins remove myplugin
```

## `bang-tool plugins reset`

Remove all user-installed and linked plugins.

```
USAGE
  $ bang-tool plugins reset [--hard] [--reinstall]

FLAGS
  --hard       Delete node_modules and package manager related files in addition to uninstalling plugins.
  --reinstall  Reinstall all plugins after uninstalling.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.15/src/commands/plugins/reset.ts)_

## `bang-tool plugins uninstall [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ bang-tool plugins uninstall [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ bang-tool plugins unlink
  $ bang-tool plugins remove

EXAMPLES
  $ bang-tool plugins uninstall myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.15/src/commands/plugins/uninstall.ts)_

## `bang-tool plugins unlink [PLUGIN]`

Removes a plugin from the CLI.

```
USAGE
  $ bang-tool plugins unlink [PLUGIN...] [-h] [-v]

ARGUMENTS
  PLUGIN...  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ bang-tool plugins unlink
  $ bang-tool plugins remove

EXAMPLES
  $ bang-tool plugins unlink myplugin
```

## `bang-tool plugins update`

Update installed plugins.

```
USAGE
  $ bang-tool plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v5.4.15/src/commands/plugins/update.ts)_
<!-- commandsstop -->
