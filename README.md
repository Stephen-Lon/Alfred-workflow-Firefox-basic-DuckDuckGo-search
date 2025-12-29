# Firefox basic DuckDuckGo search
Basic DuckDuckGo search in Firefox using optional exclusions

# Introduction

The purpose of this workflow is to allow a search of DuckDuckGo in Firefox using URL parameters. In the workflow configuration you can also choose whether or not to exclude from the search Amazon, eBay, Facebook and/or YouTube (by default all are excluded). The search results will open in a Firefox private window. (If you change the default exclusions don't forget to save the changed configuration!)

See [here](https://duckduckgo.com/duckduckgo-help-pages/settings/params) for DuckDuckGo search parameters. This workflow uses (in the workflow configuration):

- `&kp=-2` to turn off safe search
- `&kl=uk-en` to set the results to UK
- `&k-1` to turn off advertisements
- `kac-1` to turn off auto-suggest
- `&kz-1` to turn off open instant answers.

You can choose in the configuration to concentrate the search results on the UK region or all regions.

# Usage

Either:

1. Type the keyword (the default is `duck`) followed by a space and your search term then press <kbd>⏎</kbd>.

Or:

2. Select some text, press your Universal Actions hotkey, start typing "Firefox", select from the list of results `Firefox basic DuckDuckGo search`then press <kbd>⏎</kbd>.

The search results open in a new Firefox private tab.

# How to add a new exclusion

We shall take Pinterest as an example.

1. Add a new checklist item in the workflow configuration builder.
2. Set the variable name, in this case, to `exPinterest`.
3. Now we need to amend the `Run Script` action by adding at the end of the list of exclusions the following line:  

`[ "${exPinterest}" -eq 1 ] && exsite+=' - site:pinterest'`  

Be careful with the quotation marks and the spaces (including the leading space) in ` - site:Pinterest`!

Don't forget to save the new script!
