# cwpass - Pass for Windows

cwpass is a packaging of the classic Unix-style password manager `pass` for Windows systems. It provides a self-contained Cygwin-based environment with GnuPG, pass, and required utilities already included, offering a ready-to-use command-line password-store solution for Windows.

## Features

- **Standard pass workflow**: Implements the standard `pass` password-store workflow on Windows
- **Bundled GnuPG**: Includes its own GnuPG, no external installation required
- **Standard storage format**: Stores passwords as individually encrypted files using the conventional `~/.password-store` layout
- **Common commands**: Supports commonly used commands such as `show`, `insert`, `generate`, `rm`, and `grep`
- **Portable**: Unzip and run, no installation or system modifications required
- **Wide compatibility**: Works on Windows Vista and newer

### Limitations

- `edit` and `git` features are not implemented
- Clipboard is not cleared automatically after copying

## Requirements

- Windows Vista or later
- No external GnuPG installation required — included in the package

## Download

Latest releases of cwpass are available on GitHub:

https://github.com/itefixnet/cwpass

Each release includes:
- The complete cwpass ZIP package (Cygwin runtime, GnuPG, pass)
- Release notes and version history

## Basic Usage

1. Unzip the downloaded archive

2. Start the cwpass environment:
   ```
   cwpass.cmd
   ```

3. If needed, create a GPG key within the environment:
   ```
   gpg --gen-key
   ```

4. Initialize your password store:
   ```
   pass init <your-gpg-key-id>
   ```

5. Use commands such as:
   ```
   pass show example
   pass insert email/github
   pass generate email/github 16
   pass grep admin
   ```

The password store remains fully compatible with Linux and macOS versions of `pass`.

## Links

- **cwpass homepage**: https://itefix.net/cwpass
- **cwpass repository**: https://github.com/itefixnet/cwpass
- **pass homepage**: https://www.passwordstore.org/
- **pass repository**: https://git.zx2c4.com/password-store/

## Support

Support and issue tracking are handled via GitHub Issues:

https://github.com/itefixnet/cwpass/issues

## License

See LICENSE file for details.
