---
dg-publish:
---
# Julia Installation
Julia's regularly gets version updates that include new features and changes to its internal mechanism. Updating Julia is primarily done with [Juliaup](https://github.com/julialang/juliaup), which is a cross-platform installer for the Julia programming language. While Julia can be installed in other ways, this is the best way of installing and managing Julia versions on one's local machine. Installation begins by downloading it onto the local device, which is done as follows on Windows:
```powershell
winget install --name Julia --id 9NJNWW8PVKMN -e -s msstore
```

Once it has been installed, confirming that it works can be done using the CLI:
```powershell
Juliaup
```

### Important Commands and Keywords
Juliaup provides many commands for managing the various Julia installations on one's local machine. Below are the main commands which are most useful:
- `juliaup list` lists all the available channels.
- `juliaup update` installs the latest available Julia version for all currently installed channels.
- `juliaup update release` updates the `release` channel to the latest version.
- `juliaup status` shows the user which Julia versions they have installed and which one is configured as the default.
- `juliaup add <version>` adds a specific Julia version to the system (it can then be launched via the command `julia +<version>`).
- `juliaup default <version>` configures the `julia` command to start Julia `<version>` as the default when `julia` is entered in the CLI.
- `juliaup default release` configures the `julia` command to start the latest stable version of Julia (this is also the default value).
- `juliaup remove <version>` deletes the specific Julia version from the system.
- `juliaup self update` installs the latest version, which is necessary if new releases reach the beta channel, etc.
- `juliaup self uninstall` uninstalls Juliaup. Note that on some platforms this command is not available, in those situations one should use platform specific methods to uninstall Juliaup.
- `juliaup override status` shows all configured directory overrides.
- `juliaup override set lts` sets a directory override for the current working directory to the `lts` channel.
- `juliaup override unset` removes a directory override for the current working directory.

Note that all commands offered by Juliaup can be checked by simply entering `Juliaup` into the CLI. 