## What is it? ##

`verify-string-files` is a tiny little Mac command-line tool that verifies
localized `.strings` files against the given "master" `.strings` file (typically
the one in `Base.lproj` or your development language).

The tool will output problems (like missing strings in your localizations) as
errors, warnings or notes that Xcode will pick up and display.

Combined with a custom build step in your Xcode project, it can be used to
automatically give compile-time checked keys for your localised strings.

## Examples ##

### `-warning-level error` ###

![alt tag](doc/error.png)

### `-warning-level warning` ###

![alt tag](doc/warning.png)

## License ##

`verify-string-files` is licensed under three-clause BSD. The license document can be
found [here](https://github.com/iKenndac/generate-string-symbols/blob/master/LICENSE.markdown).

## Building ##

1. Clone verify-string-files using `$ git clone git://github.com/iKenndac/verify-string-files.git`.
2. Open the project and build away!

## Usage ##

`$ verify-string-files -master <strings file path> [-warning-level <error | warning | note>]`

* `-master` The path to a valid .strings file. Should be localized (that is,
  inside an .lproj folder and what's considered the "base" strings file for the
  project.

* `-warning-level` The warning level to use: `error`, `warning` or `note`. Defaults
 to `error`.
