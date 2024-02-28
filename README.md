# vscem

Very basic VS Code extension manager to export, install, update or uninstall VS Code extensions.

## Prerequisit

`code` must be in your `PATH`.

To add it, open VS Code's command palette > `Install 'code' command in PATH`.

## Usage

Use `export` to save all installed extension IDs in a file called `vscode-extensions.txt`. The file will be located in vscem directory.

``` zsh
bash vscem export
```

This is convenient to install or reinstall your favorite extensions later on.

vscem provides the following functions to manage extensions:

- `install` to install extensions.
- `update` to update extensions.
- `uninstall` to uninstall extensions.

Use them as follows:

``` zsh
# process all currently installed extensions
bash vscem <function> -a

# process all extensions stored in a file
bash vscem <function> file

# process specific extensions
bash vscem <function> extension_1 extension_2 ... extension_n
```

Note that each extension ID must be on a new line when processing extensions from a file.

## Examples

``` zsh
# install all extensions in 'vscode-extensions.txt'
bash vscem install vscode-extensions.txt

# update all currently installed extensions
bash vscem update -a
```
