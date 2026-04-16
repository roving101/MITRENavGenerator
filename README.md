# MITRE ATT&CK Matrix Generator

A lightweight Python script that generates a MITRE ATT&CK matrix starting from a hardcoded list of TTP technique IDs defined directly in the script.

This first version is intentionally simple: the goal is to provide a fast and practical way to visualize a predefined set of ATT&CK techniques without requiring external input files, APIs, or command-line arguments. The project is expected to evolve over time, with future updates introducing more flexible input methods, validation, customization, and output improvements.

## Overview

The script takes a list of ATT&CK technique identifiers that are currently hardcoded in the source code and uses them to build a matrix-style output. This approach makes the script easy to test, easy to modify, and useful as a first implementation for quick internal use or experimentation.

At this stage, the design is intentionally minimal. Instead of focusing on input parsing or integrations, the script is centered on a single objective: transforming a known list of TTPs into a readable MITRE ATT&CK matrix representation.

## Current Scope

This version is built around the following assumptions:

- The input consists of ATT&CK technique IDs such as `T1059`, `T1566.001`, or similar, contained in a file with a technique on each row.
- The script generates a MITRE ATT&CK matrix view based on the techniques provided.
- The project is an initial release and will be updated in future iterations.

## Why Hardcoded TTPs

Hardcoding the list of techniques in the first version keeps the script straightforward and removes unnecessary complexity from the initial implementation. This makes it easier to validate the core logic, test matrix generation behavior, and adjust the structure before introducing external dependencies or more advanced user input handling.

This approach is especially useful during early development, internal prototyping, or when working from a known and stable set of techniques derived from a report, a case study, or a detection mapping exercise.

## Expected Evolution

Future versions may include enhancements such as:

- Input from text files, CSV, JSON, or command-line arguments.
- Validation of ATT&CK technique IDs.
- Support for sub-techniques and custom grouping.
- Export to additional formats.
- Improved matrix rendering and presentation.
- Integration with external ATT&CK data sources.

The current version should therefore be considered a foundation rather than a finished product.

## Usage Model

The intended workflow for this first version is simple:

1. Run the script with the following usage parameters:
``` bash
usage: mitre_generator.py [-h] [-o OUTPUT] file

        Parses MITRE ATT&CK TTPs from an input file and generates a JSON file ready to be imported into the MITRE ATT&CK Navigator (https://mitre-attack.github.io/attack-navigator/).
        JSON content is printed to stdout.


positional arguments:
  file                 Input file

options:
  -h, --help           show this help message and exit
  -o, --output OUTPUT  Output JSON file
  -d, --disable-ids    Disable IDs in the output matrix
```
2. Review the generated MITRE ATT&CK matrix json uploading it into MITRE ATT&CK Navigator output.


## Notes

This repository contains an early version of the project. The implementation is designed to be easy to understand and easy to extend, rather than feature-complete. As the project matures, the input model and output capabilities may change to support broader use cases.

## Credits

Credits to @roving101 and @lucareggiannini.
