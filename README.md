# MITRE ATT&CK Matrix Generator

A lightweight Python script that generates a MITRE ATT&CK matrix starting from a list of TTP technique IDs.
The project is expected to evolve over time, with future updates introducing more flexible input methods, validation, customization, and output improvements.

## Overview

The script takes a list of ATT&CK technique identifiers that are currently imported from a file and uses them to build a matrix-style output. This approach makes the script easy to test, easy to modify, and useful as a first implementation for quick internal use or experimentation.

At this stage, the design is intentionally minimal. Instead of focusing on input parsing or integrations, the script is centered on a single objective: transforming a known list of TTPs into a readable MITRE ATT&CK matrix representation.

## Current Scope

This version is built around the following assumptions:

- The input consists of ATT&CK technique IDs such as `T1059`, `T1566.001`, or similar, contained in a file with a technique on each row.
- The script generates a MITRE ATT&CK matrix view based on the techniques provided.
- The project is an initial release and will be updated in future iterations.


## Expected Evolution

Future versions may include enhancements such as:

- Support for sub-techniques and custom grouping.
- Export to additional formats.
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
  -v, --verbose        Verbose Output
  -m, --v19            Output to Mitre ATT&CK v19 Matrix
```
2. Review the generated MITRE ATT&CK matrix json uploading it into MITRE ATT&CK Navigator output.

Usage Screenshots:

1. Input File
<img width="102" height="500" alt="image" src="https://github.com/user-attachments/assets/4a520c62-65d4-4c8c-9529-38a21cb376b5" />
2.Visualization of the JSON in the MITRE Navigator
<img width="1900" height="613" alt="image" src="https://github.com/user-attachments/assets/94429c0c-7d01-4dc1-8bc1-ef6ef418a6c4" />


## Notes

This repository contains an early version of the project. The implementation is designed to be easy to understand and easy to extend, rather than feature-complete. As the project matures, the input model and output capabilities may change to support broader use cases.

## Credits

Credits to @roving101 and @lucareggiannini.
