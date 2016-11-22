## Installation

- install the [stylelint CLI](http://stylelint.io/user-guide/cli/)
- [configure](http://stylelint.io/user-guide/configuration/)

## Example configuration file (**.stylelintrc**)

```json
{
  "rules": {
    "no-duplicate-selectors": true,
    "declaration-block-no-duplicate-properties": true,
    "declaration-block-no-redundant-longhand-properties": true,
    "shorthand-property-no-redundant-values": true,
    "length-zero-no-unit": true,
    "color-hex-case": "lower",
    "color-hex-length": "short",
    "color-no-invalid-hex": true
  }
}
```

## Automate formatting

install [stylefmt](https://github.com/morishitter/stylefmt). Given that we'll be working with the above config options, only the items below are supported by **stylefmt**.

- shorthand-property-no-redundant-values
- length-zero-no-unit
- color-hex-case
- color-hex-length

## Running

To be clear, **stylelint** is the linting tool and **stylefmt** is the formatting tool. The `.stylelintrc` file tells **stylelint** what constitutes an invalid rule, and **stylefmt** which rules to modify.

Run stylelint: `stylelint style.css`

Run stylefmt: `stylefmt [options] input-file [output-file]`

## What to expect

Running Stylelint appears to first check for critical syntax errors in the stylesheet. For example, running this command against style.css in this repo produces a **CssSyntaxError** because of an unexpected curly brace...then a couple "unknown word" errors. After fixing these, the CLI tool will list all the lint errors. It also appears to be the case that stylefmt *will not* run without first fixing the critical errors in the stylesheet. It's also important to remember that stylefmt will ONLY fix available items listed in the `.stylelintrc`.