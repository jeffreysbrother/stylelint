### installation

- install the [stylelint CLI](http://stylelint.io/user-guide/cli/)
- [configure](http://stylelint.io/user-guide/configuration/)

### configuration file (**.stylelintrc**)

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