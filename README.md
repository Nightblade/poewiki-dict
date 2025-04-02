
# poewiki-dict

This repository provides spell-checker dictionaries for Firefox and Chrome, specifically tailored for editing articles on [poewiki.net](https://www.poewiki.net).

# Limitations

The spell-checker dictionaries in this repository are generated from [CSpell](https://www.github.com/streetsidesoftware/cspell) dictionary files; by default, CSpell ignores words less than **four** characters long, and handles possessives (`'s`) automatically.  By contrast, the spell-checkers in Firefox & Chrome ignore words less than **three** characters long, and do **not** handle possessives (`'s`) automatically.

(Also, Firefox & Chrome are case-sensitive, but I have addressed this by adding each word twice with alternating capitalization, with the exception of ALLCAPS words.)

# Installation

## Firefox
* Download [persdict.dat](https://raw.githubusercontent.com/Nightblade/poewiki-dict/main/persdict.dat)
* Move/copy it to your `profile directory`.
	To quickly find your profile directory:
	* Type `about:support` into the browser's address bar,
	* Next to `Profile Folder`, click `Open Folder`.

## Chrome
* Download [Custom Dictionary.txt](https://raw.githubusercontent.com/Nightblade/poewiki-dict/main/Custom%20Dictionary.txt)
* Move/copy it to your `profile directory`.
* Delete any existing `Custom Dictionary.txt.backup` file.  (This is to stop Chrome trying to restore this file and overwriting your new file).
	To find your profile directory:
	* Type `about:version` into the browser's address bar,
	* Copy the text next to `Profile Path:`,
	* Paste this into an Explorer window or equivalent.


# Source Files

All `.txt` files listed below are `plaintext`, `UTF-8`, `LF`-`EOL`, with a single word per line.

These files are all stored in the [pob-dict](https://www.github.com/Nightblade/pob-dict) repository, except for `wiki-ignore-dict.txt` which is stored in this repo in the [src](src) directory.

| Filename                       | Description
| ------------------------------ | -----------
| [poe-dict.txt](https://github.com/Nightblade/pob-dict/blob/main/poe-dict.txt) | Words specific to [Path of Exile](https://www.pathofexile.com/).
| [extra-en-dict.txt](https://github.com/Nightblade/pob-dict/blob/main/extra-en-dict.txt) | Extra English words that are not in CSpell's dictionaries.
| [pob-dict.txt](https://github.com/Nightblade/pob-dict/blob/main/pob-dict.txt) | Words used in the PoB source-code and associated files.

| [wiki-ignore-dict.txt](src/wiki-ignore-dict.txt) | `poewiki.net`-specific words to be ignored.


# Build details

Whenever the [build](https://github.com/Nightblade/poewiki-dict/actions/workflows/build.yml) workflow is run, the source files are fetched, concatenated, sorted (unique), processed as mentioned above, and if any changes are detected the resulting files are automatically checked-in and committed.


# License

[MIT](https://opensource.org/licenses/MIT)
