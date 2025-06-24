# fdt - Discord Token Validator

[![Basher](https://img.shields.io/badge/basher-install-brightgreen)](https://github.com/basherpm/basher)

Extract and validate Discord tokens from files and directories with comprehensive verification and reporting.

## Features

- **Token Extraction**: Find Discord tokens using regex patterns in files and directories
- **Token Validation**: Verify tokens against Discord's API
- **Multiple Output Formats**: JSON, TXT, and CSV output options
- **Detailed Reporting**: Get user information, verification status, and confidence scores
- **Source Tracking**: Track where tokens were found with timestamps
- **Recursive Search**: Search through directory structures
- **Progress Indicators**: Visual progress bars and status updates

## Installation

### Using Basher

```bash
basher install gnomegl/fdt
```

### Manual Installation

```bash
git clone https://github.com/gnomegl/fdt.git
cd fdt
chmod +x bin/fdt
# Add to PATH or copy to /usr/local/bin
```

## Usage

### Basic Commands

```bash
# Validate tokens in current directory
fdt validate .

# Validate tokens in specific directory recursively
fdt validate /path/to/logs --recursive

# Check a single token
fdt check --token 'YOUR_TOKEN_HERE'

# Extract tokens without validation
fdt extract ./logs --format csv
```

### Options

- `-t, --token` - Single token to validate directly
- `-o, --output` - Output directory for valid tokens
- `-f, --format` - Output format (json, txt, csv)
- `-r, --recursive` - Search recursively in directories
- `-s, --silent` - Suppress loading animations
- `-q, --quiet` - Suppress colored output

### Examples

```bash
# Validate all tokens found in logs directory
fdt validate ./logs --recursive --format json

# Check if a specific token is valid
fdt check --token "NzA4NzA4NzA4NzA4NzA4NzA4.Xqr5Tg.dQw4w9WgXcQ"

# Extract tokens to CSV format
fdt extract /var/log --format csv --output ./results
```

## Output Formats

### JSON
Detailed information including user data, verification status, and metadata.

### TXT
Simple text format with just the token values.

### CSV
Spreadsheet-compatible format with token, username, user ID, and timestamp.

## Requirements

- `curl` - For API requests
- `rg` (ripgrep) - For fast text searching
- `jq` - For JSON processing

## License

MIT License
