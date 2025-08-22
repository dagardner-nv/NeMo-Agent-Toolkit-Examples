<!--
SPDX-FileCopyrightText: Copyright (c) 2024-2025, NVIDIA CORPORATION & AFFILIATES. All rights reserved.
SPDX-License-Identifier: Apache-2.0

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
-->


# Contributing Guidelines

The NeMo Agent Toolkit Examples repository is a collection of examples that demonstrate how to use the NeMo Agent Toolkit. We welcome contributions from the community to add new examples, improve existing examples, and fix bugs.

To ensure your contribution is accepted, please follow the guidelines below.

## What to Contribute

### New Examples

If you have an idea for a new example, or would like to contribute an example you have created, please enture that your example follows these general guidelines:

1. Examples should demonstrate a specific use case or feature of the NeMo Agent Toolkit.
2. Examples should be unique and not already covered by an existing example.
3. Examples should be reliable and reproducible.

If you have an example you would like to contribute, please open up an issue to discuss your idea before submitting a pull request.

### New Features



### Bug Fixes

## Example Requirements

### Organization
Examples should follow a specified structure to maintain consistency across the repository. The recommended structure is:
```bash
examples/
  $EXAMPLE_NAME/
    configs/ # Symlink to `src/nat_$EXAMPLE_NAME/configs/`
    data/ # [Optional] Symlink to `src/nat_$EXAMPLE_NAME/data/`
    scripts/ # [Optional] Directory for scripts needed to setup the example
    src/
      nat_$EXAMPLE_NAME/ # All example modules must start with the prefix `nat_`
        configs/
          config.yml # At least one config file for the example
        data/ # [Optional] Directory for data files needed to run the example
          ... # [Optional] Data files needed to run the example
        __init__.py
        register.py
    README.md or README.ipynb # Documentation for the example
    pyproject.toml # Must register the example with `nat`
```

### Documentation
Each example must include clear documentation on how to run it. This can be provided in either:
- A README.md file at the top level of the example directory
- A README.ipynb Jupyter notebook that walks through the example

In both cases, the documentation should include:

- A description of the example
- Key features of the example
- Setup instructions
- How to run the example
- Expected results
- [Optional] Troubleshooting tips

## Testing
To ensure examples remain functional, each example must include unit tests written using `pytest`. Tests should verify the core functionality of the example and help catch issues when dependencies are updated.

## Code Style
All code should be compatible with the linting rules defined in the root `pyproject.toml` file. To ensure your code is compatible, run the following command:

```bash
./ci/scripts/checks.sh
```

## License
All contributions must be made under the [Apache 2.0 License](https://www.apache.org/licenses/LICENSE-2.0).

## Code of Conduct
All contributors must follow the [Code of Conduct](CODE_OF_CONDUCT.md).
