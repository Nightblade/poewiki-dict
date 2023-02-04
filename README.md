
# poewiki-dict

This repo provides a spell-checker dictionary-file that can be used while editing articles on [`poewiki.net`](https://www.poewiki.net).  It contains words & names specific to [`Path of Exile`](https://www.pathofexile.com) together with words commonly used while editing pages on [`Mediawiki`](https://www.mediawiki.org)-based sites.

<u>**Note:**  This is a WIP and currently only supports `Firefox`.</u>

# Specifics & Limitations
([`persdict.dat`](https://github.com/Nightblade/poewiki-dict/blob/main/persdict.dat)) is meant to replace your "personal dictionary" file in Firefox.

The PoE dictionary is stored in the [`pob-dict`](http://www.github.com/Nightblade/pob-dict) repository, and is merged with the wiki dictionary from the `src` folder here whenever the [`build`](https://github.com/Nightblade/poewiki-dict/actions/workflows/build.yml) workflow is run.

As Firefox's personal dictionary is case-sensitive, all words are included twice (lower-case and proper-caps) to reduce false spelling errors.   Words in **ALLCAPS** are the exception.

Currently, the following features are not supported:
* words containing apostrophes
* three-letter-words


# Installation
* Download [`persdict.dat`](https://raw.githubusercontent.com/Nightblade/poewiki-dict/main/persdict.dat) 
* Move/copy to your `profile directory`.  
	To quickly find it:
	* Type `about:support` into the FF address bar,
	* Next to `Profile Folder` click `Open Folder`


# License

[MIT](https://opensource.org/licenses/MIT)
