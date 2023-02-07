
# poewiki-dict

This repo provides spell-checker dictionary files that can be used while editing articles on [poewiki.net](https://www.poewiki.net) with Firefox or Chrome.  It contains words & names specific to [Path of Exile](https://www.pathofexile.com) together with words commonly used while editing pages on [Mediawiki](https://www.mediawiki.org)-based sites.

# Limitations

The dictionary files here are generated from [CSpell](https://www.github.com/streetsidesoftware/cspell) dictionary files.  CSpell's spell-checker ignores words less than four characters long by default, and handles possessives (`'s`) correctly.  By contrast, the spell-checkers in Firefox & Chrome ignore words less than **three** characters long, and do **not** handle possessives (`'s`) correctly.

(Also, Firefox & Chrome are strictly case-sensitive, but I have addressed this by adding each word twice with alternating capitalization.  Words in ALLCAPS are the exception.)

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


# Source

The source files listed below are all `plaintext`, `UTF-8`, `LF`-terminated, with a single word on each line.

These files are all stored in the [pob-dict](https://www.github.com/Nightblade/pob-dict) repository, except for `wiki-ignore-dict.txt` which is stored in this repo under the [src](src) directory.

| Filename                       | Description
| ------------------------------ | -----------
| [poe-dict.txt](https://github.com/Nightblade/pob-dict/blob/main/poe-dict.txt) | Words specific to [Path of Exile](https://www.pathofexile.com/).
| [pob-dict.txt](https://github.com/Nightblade/pob-dict/blob/main/pob-dict.txt) | Words used in the PoB source-code and associated files.
| [ignore-dict.txt](https://github.com/Nightblade/pob-dict/blob/main/ignore-dict.txt) | PoB-specific-words to be ignored.
| [extra-en-dict.txt](https://github.com/Nightblade/pob-dict/blob/main/extra-en-dict.txt) | Extra English words that are not in cSpell's dictionaries.
| [wiki-ignore-dict.txt](src/wiki-ignore-dict.txt) | `poewiki.net`-specific words to be ignored.


# Build details 

Whenever the [build](https://github.com/Nightblade/poewiki-dict/actions/workflows/build.yml) workflow is run, the source-files mentioned above are fetched, concatenated, sorted, processed as mentioned earlier, and then automatically checked-in and committed if any changes are detected.


# License

[MIT](https://opensource.org/licenses/MIT)
