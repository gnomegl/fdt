# fdt

[![basher install](https://www.basher.it/assets/logo/basher_install.svg)](https://www.basher.it/package/)

discord token validator and extractor

## install

```bash
basher install gnomegl/fdt
```

## usage

```bash
fdt /path/to/search
```

extract and validate discord tokens from files.

## options

- `-r, --recursive` - search recursively
- `-v, --validate` - validate found tokens
- `-o, --output` - output file for tokens
- `-q, --quiet` - suppress output
- `-j, --json` - json output format

## requirements

- curl
- jq
- grep