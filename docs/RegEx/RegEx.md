## Resource :
- [Learn RegEx the easy way](https://github.com/ziishaned/learn-regex)
- [RegEx onine editor](https://regex101.com/)

## Cheat sheet :
### Meta character
|Meta character|Description|
|:----:|:----|
|^|Matches the beginning of the input.|
|$|Matches the end of the input.|
|.|Matches any single character except a new line character.|
|[ ]|Matches any character contained between the square brackets.|
|[^ ]|Matches any character that is not contained between the square brackets|
|*|Matches `0` or more repetitions of the preceding symbol.|
|+|Matches `1` or more repetitions of the preceding symbol.|
|?|Makes the preceding symbol optional.|
|{n}|The preceding item is matched exactly n times.|
|{min,}|	The preceding item is matched min or more times.|
|{,max} | The preceding item is matched up to max times.|
|{min,max} | The preceding item is matched at least min times, but not more than max times.|
|(xyz)|Matches the characters xyz in that exact order.|
|&#124;|Matches either the characters before or the characters after the symbol.|
|&#92;|Match reserved characters <code>[ ] ( ) { } . * + ? ^ $ \ &#124;</code>|


### Shorthand character sets
|Shorthand|Description|
|:----:|----|
|.|Any character except new line|
|\w|Matches alphanumeric characters: `[a-zA-Z0-9_]`|
|\W|Matches non-alphanumeric characters: `[^\w]`|
|\d|Matches digits: `[0-9]`|
|\D|Matches non-digits: `[^\d]`|
|\s|Matches whitespace characters: `[\t\n\f\r\p{Z}]`|
|\S|Matches non-whitespace characters: `[^\s]`|


### Lookarounds
|Symbol|Description|
|:----:|----|
|?=|Positive Lookahead|
|?!|Negative Lookahead|
|?<=|Positive Lookbehind|
|?<!|Negative Lookbehind|

### Flags
|Flag|Description|
|:----:|----|
|i|Case insensitive: Match will be case-insensitive.|
|g|Global Search: Match all instances, not just the first.|
|m|Multiline: Anchor meta characters work on each line.|

- `?` makes the preceding character
optional. This symbol matches zero or one instance of the preceding character.
- Non-Capturing group : `(?:...)`
- `\w` = `[a-zA-Z0-9]`
- `\b...\b` : Match Whole Words
