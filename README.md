
# save-paste

## Description

The `save-paste` script is a convenient tool for developers who frequently need to copy and paste code from generative AI platforms like ChatGPT into their code files. This is particularly useful when working on simple scripts or refining code through iterative prompts.

When using a code editor, updating your script is straightforward—you can simply select all and paste the new code, overwriting the old code. However, for small, random scripts that you aren’t editing in a code editor, you might just want to replace the contents of a script in the current directory to test it again. Manually clearing out the file with `vi` or `nano` and pasting contents from the browser each time you make a change can be tedious.

To streamline this process, the `save-paste` script saves the contents of the macOS clipboard to a specified file. If the file already exists, it creates a hidden backup of the current file with a timestamp appended to the filename. The script also has a `--dry-run` option that shows what the backup file name will be and how many lines will be saved to the new file without actually performing the save operation.

## Usage

```sh
save-paste <file_path> [--dry-run]
```

- `<file_path>`: The path to the file where the clipboard contents will be saved.
- `--dry-run`: Optional argument that, if provided, will show the backup file name and line count without saving.

## Examples

Save clipboard contents to `test.sh`:
```sh
save-paste ~/scripts/test.sh
```

Perform a dry run to show the backup file name and line count without saving:
```sh
save-paste ~/scripts/test.sh --dry-run
```

## Installation

1. Copy the save-paste file to a directory that is in your PATH variable. For example, `/usr/local/bin/`.
2. Change the permissions to make it executable:
```sh
chmod +x /usr/local/bin/save-paste
```

## Contributing

Feel free to fork this repository, create a new branch, and submit a pull request with your improvements or bug fixes. Contributions are always welcome!

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
