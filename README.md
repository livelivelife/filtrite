## filtrite
filtrite is a project for generating filter lists for [Bromite](https://www.bromite.org/).
See the page about [Custom Ad Block Filters](https://www.bromite.org/custom-filters) for more info.

# Lists
You can choose any list from below, copy the link and add it in Bromite by going to settings > AdBlock settings, then setting Filters URL to the one you just copied.

Here's a list:


| Link | Description  |
| ------ | ------|
| [Bromite Default](https://github.com/xarantolus/filtrite/releases/latest/download/bromite-default.dat) | Bromite [default filter list](https://github.com/bromite/filters), but generated by this tool |
| [Bromite Extended](https://github.com/xarantolus/filtrite/releases/latest/download/bromite-extended.dat) | The default list with additional annoyance blockers I use with [uBlock Origin](https://github.com/gorhill/uBlock) on Desktop |

These lists are regularly updated automatically using GitHub Actions.

**Note**: I'm not 100% sure if all list formats that are used are actually supported by [the ruleset generation tool](https://github.com/xarantolus/subresource_filter_tools) (as the output indicates some failures). If you have a comment on that, please open an issue :)

### Using your own filter lists
This program is designed in a way that allows easily adding new lists. 

To create a new list:

1. Fork this repository
2. Enable GitHub Actions by switching to the "Actions" tab of your repo, then confirming that you want to enable them
3. Choose a name for the list, e.g. `example-list`
4. Create a file `lists/example-list.txt` (aka in the `lists` directory) that contains all URLs. It should look like this:
```
# Comments and empty lines are allowed
# List one URL per line:
https://...
https://...

# The following line doesn't work, only put either a comment or an URL in one line, not both
http://  # Invalid comment on URL
```
5. Save your file, commit and push
6. After GitHub Actions generated the release, you can copy the linked URL in the release to always get the latest generated version. This URL looks something like `https://github.com/USERNAME/filtrite/releases/latest/download/FILENAME.dat`. 
7. Set this URL as the filter file in Bromite settings.

### [License](LICENSE)
This is free as in freedom software. Do whatever you like with it.
