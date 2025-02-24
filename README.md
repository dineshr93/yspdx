# yspdx

A Python package for processing several SPDX (Software Package Data Exchange) files generated from create-spdx.bbclass with different output formats.

## Installation

```bash
pip install yspdx
```

## Usage

The package provides a command-line interface with three different output modes:

1. Full output (-f or --full):
```bash
yspdx -f
generate_full_details done!
```

2. Binary-focused output (-b or --bin):
```bash
yspdx -b
generate_binary_details done!
```

3. Minimal output (-m or --min):
```bash
yspdx -m
generate_minmal_details done!
```

4. If you dont specify any of above it'll produce all 3 of the above outputs (-f,-b and-m):
```bash
> yspdx
generate_minmal_details done!
generate_binary_details done!
generate_full_details done!
```

You can also mix and match options for ex: -fb or -fm or -bm or even -fbm
By default, the tool looks for a file named `system_extra.spdx.tar.zst` in the current directory. You can specify a different archive path using the --archive option:

```bash
yspdx -f --archive /path/to/your/archive.spdx.tar.zst
```

## Output Files

The tool generates different output files based on the selected mode:
- Minimal mode: `1non_build_recipes_only.txt`
- Binary mode: `2non_build_binaries_only.txt`
- Full mode: `3with_build_deps_full.txt`

## Author

Dinesh Ravi

## License
Copyright (c) 2025 Dinesh Ravi
GPL-3.0+ License

