
# poewiki-dict

This repo provides spell-checker dictionary files that can be used while editing articles on [poewiki.net](https://www.poewiki.net) with Firefox or Chrome.  It contains words & names specific to [Path of Exile](https://www.pathofexile.com) together with words commonly used while editing pages on [Mediawiki](https://www.mediawiki.org)-based sites.

# Limitations

The dictionary files here are generated from [CSpell](http://www.github.com/streetsidesoftware/cspell) dictionary files.  CSpell's spell-checker ignores words less than four characters long by default, and handles possessives (`'s`) correctly.  By contrast, the spell-checkers in Firefox & Chrome ignore words less than **three** characters long, and do **not** handle possessives (`'s`) correctly.

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

# Misc info

The PoE dictionary is stored in the [pob-dict](http://www.github.com/Nightblade/pob-dict) repository, and is merged with the wiki dictionary from the `src` folder here whenever the [build](https://github.com/Nightblade/poewiki-dict/actions/workflows/build.yml) workflow is run.


# License

[MIT](https://opensource.org/licenses/MIT)
