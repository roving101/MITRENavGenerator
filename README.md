# MITRE ATT&CK Matrix Generator

A lightweight Python script that generates a MITRE ATT&CK matrix starting from a hardcoded list of TTP technique IDs defined directly in the script.

This first version is intentionally simple: the goal is to provide a fast and practical way to visualize a predefined set of ATT&CK techniques without requiring external input files, APIs, or command-line arguments. The project is expected to evolve over time, with future updates introducing more flexible input methods, validation, customization, and output improvements.

## Overview

The script takes a list of ATT&CK technique identifiers that are currently hardcoded in the source code and uses them to build a matrix-style output. This approach makes the script easy to test, easy to modify, and useful as a first implementation for quick internal use or experimentation.

At this stage, the design is intentionally minimal. Instead of focusing on input parsing or integrations, the script is centered on a single objective: transforming a known list of TTPs into a readable MITRE ATT&CK matrix representation.

## Current Scope

This version is built around the following assumptions:

- TTPs are defined manually inside the Python script.
- The input consists of ATT&CK technique IDs such as `T1059`, `T1566.001`, or similar.
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

1. Open the Python script.
2. Edit the hardcoded TTP list.
3. Run the script.
4. Review the generated MITRE ATT&CK matrix output.

Because the techniques are embedded directly in the source code, updating the matrix is as simple as modifying the list and re-running the script.

## Example Input Concept

A typical hardcoded list inside the script may look conceptually like this:

```python
text = """
,T1560.001,
"T1560.002"
T1204.001 hjkl
hjkljkhl T1059 hjklhjkl
T1553.005 - 
T1082
T1083
T1059.006
T1547.001
T1005
T1567.002
T1105
T1078
T1555.003
T1555
T1555.004
T1003
T1528
T1018
T1046
 
"""
```

The exact implementation may vary, but the current model assumes that the script reads from a list like the one above and maps those entries into the corresponding ATT&CK matrix structure.

## Notes

This repository contains an early version of the project. The implementation is designed to be easy to understand and easy to extend, rather than feature-complete. As the project matures, the input model and output capabilities may change to support broader use cases.

## Credits

Credits to @roving101 and @lucareggiannini.
