<div align="center">

# Python 3 Deep Dive — Part 2

### Iterators, Generators, Iteration Tools, Context Managers & Coroutines

A structured collection of Jupyter notebooks, practical exercises, advanced explorations, and project solutions created while studying **Python 3: Deep Dive (Part 2 — Iterators, Generators)** by **Dr. Fred Baptiste**.

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Course](https://img.shields.io/badge/Udemy-Python%203%20Deep%20Dive-A435F0?logo=udemy&logoColor=white)](https://www.udemy.com/course/python-3-deep-dive-part-2/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![GitHub last commit](https://img.shields.io/github/last-commit/SimeonChifligarov/Python_3_Deep_Dive_Part_2_Iterators_Generators_Udemy_by_Fred_Baptiste)](https://github.com/SimeonChifligarov/Python_3_Deep_Dive_Part_2_Iterators_Generators_Udemy_by_Fred_Baptiste/commits/main)

</div>

---

> [!IMPORTANT]
> This is an independent educational repository containing personal notes, implementations, experiments, and solutions created during the learning process. It is not an official course repository and is not a replacement for the original course.

## Table of Contents

- [Overview](#overview)
- [Topics Covered](#topics-covered)
- [Learning Objectives](#learning-objectives)
- [Repository Structure](#repository-structure)
- [Projects](#projects)
- [Notebook Conventions](#notebook-conventions)
- [Getting Started](#getting-started)
- [Recommended Learning Path](#recommended-learning-path)
- [Educational Scope](#educational-scope)
- [Contributing](#contributing)
- [Course Attribution and Disclaimer](#course-attribution-and-disclaimer)
- [License](#license)
- [Author](#author)

## Overview

This repository documents my progress through the second part of Fred Baptiste’s **Python 3 Deep Dive** series.

The material focuses on Python’s iteration model—from the sequence protocol and custom iterables to generators, lazy pipelines, context managers, and generator-based coroutines.

The repository includes:

- Executable Jupyter notebooks organized by course section
- Detailed examples of Python’s iteration protocols
- Custom sequence, iterable, and iterator implementations
- Lazy evaluation and generator-based solutions
- Standard and advanced notebook variants
- Six practical projects
- CSV and text datasets used by selected exercises
- Additional experiments beyond the core examples
- Notes covering later Python language updates

The goal is not simply to demonstrate syntax, but to understand how Python’s iteration machinery works internally and how it can be used to design expressive, memory-efficient programs.

## Topics Covered

### Sequences

- Sequence types and the sequence protocol
- Mutable and immutable sequences
- Lists versus tuples
- Shallow and deep copying
- Positive and negative indexing
- Basic, extended, and custom slicing
- In-place concatenation and repetition
- Slice assignment
- Custom sequence types
- Sorting sequences
- List comprehensions and their scope

### Iterables and Iterators

- Python’s iterable and iterator protocols
- The relationship between `iter()` and `next()`
- Creating custom iterators
- Creating reusable iterables
- Manual iterator consumption
- Lazy iterable design
- Cyclic iterators
- Callable iterators
- Delegating iterators
- Reverse iteration
- Iterator exhaustion
- One-shot versus reusable iteration
- Common iterator-related pitfalls

### Generators

- Generator functions
- The `yield` expression
- Generator states
- Generator expressions
- Lazy evaluation
- Infinite sequences
- Delegation with `yield from`
- Sending values into generators
- Closing generators
- Throwing exceptions into generators
- Generator-based data pipelines

### Iteration Tools

- Chaining iterables
- Mapping and filtering
- Aggregation
- Infinite iterators
- Combinatoric iterators
- Grouping data
- Accumulation
- Slicing iterators
- Practical usage of Python’s `itertools` module
- Building composable lazy-processing pipelines

### Context Managers

- The context management protocol
- `__enter__` and `__exit__`
- Deterministic resource management
- Exception handling inside context managers
- Reusable and nested context managers
- Generator-based context managers
- The `contextlib.contextmanager` decorator
- Context-manager use cases beyond file handling

### Generator-Based Coroutines

- Coroutine fundamentals
- Priming generators
- Sending data with `send()`
- Generator lifecycle and state
- Closing coroutines
- Exception propagation
- Delegation with `yield from`
- Pull-based pipelines
- Push-based pipelines
- Broadcasting data to multiple consumers

## Learning Objectives

By working through this repository, the learner should be able to:

- Explain the differences between sequences, iterables, iterators, and generators
- Describe how Python’s iteration protocols operate
- Implement custom sequence and iterable types
- Build reusable and one-shot iterators
- Use lazy evaluation to reduce unnecessary memory consumption
- Design generator functions and generator expressions
- Compose processing pipelines using generators and `itertools`
- Handle generator communication through `send()`, `throw()`, and `close()`
- Implement class-based and generator-based context managers
- Reason about iterator exhaustion, state, delegation, and resource cleanup
- Select an appropriate iteration abstraction for a given problem

## Repository Structure

| Section | Subject | Description |
|---|---|---|
| [`Section_02_Sequences`](Section_02_Sequences) | Sequences | Sequence protocols, mutability, copying, slicing, custom sequences, sorting, and comprehensions |
| [`Section_03_Project_1`](Section_03_Project_1) | Project 1 | Implementation of immutable polygon objects and a custom polygon sequence |
| [`Section_04_Iterables_and_Iterators`](Section_04_Iterables_and_Iterators) | Iterables and Iterators | Custom iterators, lazy iterables, callable iterators, delegation, and reverse iteration |
| [`Section_05_Project_2`](Section_05_Project_2) | Project 2 | Refactoring the polygon sequence into a lazy iterable with cached properties |
| [`Section_06_Generators`](Section_06_Generators) | Generators | Generator functions, expressions, states, delegation, and lazy evaluation |
| [`Section_07_Project_3`](Section_07_Project_3) | Project 3 | Lazy processing and analysis of NYC parking-ticket data |
| [`Section_08_Iteration_Tools`](Section_08_Iteration_Tools) | Iteration Tools | Advanced iteration patterns and practical usage of `itertools` |
| [`Section_09_Project_4`](Section_09_Project_4) | Project 4 | Multi-stage application of iteration tools and lazy transformations |
| [`Section_10_Context_Managers`](Section_10_Context_Managers) | Context Managers | Class-based and generator-based context-management patterns |
| [`Section_11_Project_5`](Section_11_Project_5) | Project 5 | Practical resource-management and context-manager exercises |
| [`Section_12_Generator_Based_Coroutines`](Section_12_Generator_Based_Coroutines) | Coroutines | Generator communication, delegation, exceptions, pipelines, and broadcasting |
| [`Section_13_Project_6`](Section_13_Project_6) | Project 6 | Applied generator-based coroutine and data-pipeline project |
| [`Section_14_Python_Updates`](Section_14_Python_Updates) | Python Updates | Additional material covering relevant changes in later Python versions |

## Projects

### Project 1 — Custom Polygon Sequence

Build an immutable `Polygon` class representing a regular convex polygon.

The implementation includes:

- Vertex and edge counts
- Circumradius
- Interior angle
- Side length
- Apothem
- Surface area
- Perimeter
- Equality and ordering behavior

The project then introduces a custom finite sequence of polygons supporting:

- Positive and negative indexing
- Basic and extended slicing
- Sequence length
- Immutable behavior
- Selection of the polygon with the highest area-to-perimeter ratio

### Project 2 — Lazy Polygon Iterable

Refactor the first project to introduce lazy computation.

The project focuses on:

- Caching calculated polygon properties
- Avoiding repeated calculations
- Replacing eager list storage
- Implementing a dedicated iterator
- Creating a reusable iterable
- Constructing polygon objects only when requested

### Project 3 — Lazy CSV Processing

Process an extract of New York City parking-ticket violations.

The project includes:

- Reading CSV data lazily
- Converting rows into typed named tuples
- Parsing dates and numeric values
- Minimizing eager materialization
- Counting violations by vehicle make
- Producing a summarized output dataset

### Project 4 — Iteration Tools

Apply Python’s iteration utilities to a larger multi-stage problem.

The section emphasizes:

- Composing multiple iterators
- Combining related data sources
- Mapping and filtering records
- Chaining transformations
- Preserving lazy evaluation
- Building readable data-processing workflows

### Project 5 — Context Managers

Apply context-management techniques to structured resources and reusable workflows.

The project reinforces:

- Safe acquisition and release of resources
- Exception-aware cleanup
- Reusable context-manager abstractions
- Nested context managers
- Generator-based context managers

### Project 6 — Generator-Based Coroutines

Build a practical processing pipeline using generator-based coroutines.

The project brings together:

- Primed coroutines
- Sending values into generators
- Delegation
- Exception handling
- Pipeline composition
- Broadcasting values to multiple consumers
- Graceful shutdown and cleanup

## Notebook Conventions

The repository uses several notebook naming conventions:

| Pattern | Meaning |
|---|---|
| `*.ipynb` | Core explanation or implementation for the topic |
| `*_advanced.ipynb` | Extended implementations, deeper explanations, or alternative approaches |
| `*_advanced_extra.ipynb` | Additional experiments beyond the main advanced notebook |
| `*_advanced_2.ipynb` | A further alternative or refined implementation |
| `*_Description.ipynb` | Project requirements and objectives |
| `*_Solution*.ipynb` | Goal-based or complete project solutions |

Some sections also contain supporting files such as:

- CSV datasets
- Text files
- Generated result files
- Nested exercise directories

## Getting Started

### Prerequisites

You will need:

- Python 3
- Git
- Jupyter Notebook or JupyterLab
- A Python virtual environment, recommended

A recent Python 3 release is recommended. Some notebooks originated from earlier Python 3 environments, so minor compatibility adjustments may occasionally be required.

### Clone the Repository

```bash
git clone https://github.com/SimeonChifligarov/Python_3_Deep_Dive_Part_2_Iterators_Generators_Udemy_by_Fred_Baptiste.git

cd Python_3_Deep_Dive_Part_2_Iterators_Generators_Udemy_by_Fred_Baptiste
```

### Create a Virtual Environment

#### Linux and macOS

```bash
python3 -m venv .venv
source .venv/bin/activate
```

#### Windows PowerShell

```powershell
py -m venv .venv
.venv\Scripts\Activate.ps1
```

#### Windows Command Prompt

```cmd
py -m venv .venv
.venv\Scripts\activate.bat
```

### Install JupyterLab

```bash
python -m pip install --upgrade pip
python -m pip install jupyterlab
```

### Start JupyterLab

```bash
jupyter lab
```

Navigate to the desired section and open a notebook.

## Recommended Learning Path

For the best learning experience:

1. Follow the sections in numerical order.
2. Read and run the core notebook for each topic.
3. Modify examples and predict their output before execution.
4. Complete the corresponding project without opening its solution.
5. Compare your approach with the goal-based solution notebooks.
6. Review the advanced notebooks for alternative implementations and edge cases.
7. Rebuild important examples in a separate notebook from memory.
8. Experiment with larger datasets to observe the benefits of lazy evaluation.

> [!TIP]
> Iterators and generators are best learned experimentally. Inspect object identities, call `iter()` and `next()` manually, test exhaustion behavior, and observe when values are actually calculated.

## Educational Scope

This repository is intended for learning and reference.

It is not designed as:

- An installable Python package
- A production application
- A reusable public API
- A performance benchmark
- A substitute for the original course

Some examples intentionally favor clarity and experimentation over production architecture.

## Contributing

Corrections and improvements are welcome.

Appropriate contributions include:

- Fixing typographical errors
- Correcting broken notebook cells
- Improving explanations
- Adding compatibility notes
- Simplifying examples without changing their purpose
- Reporting incorrect or misleading behavior

To contribute:

```bash
git checkout -b improvement/description
git add .
git commit -m "Improve explanation of iterator exhaustion"
git push origin improvement/description
```

Then open a pull request describing the change.

Please do not submit proprietary course assets, paid lecture materials, or content that you do not have permission to distribute.

## Course Attribution and Disclaimer

This repository is based on concepts studied in:

**[Python 3: Deep Dive — Part 2: Iterators, Generators](https://www.udemy.com/course/python-3-deep-dive-part-2/)**  
Instructor: **Dr. Fred Baptiste**

All credit for the original course structure, explanations, exercises, and teaching belongs to Fred Baptiste and the respective rights holders.

This repository:

- Is independently maintained
- Is not affiliated with or endorsed by Udemy
- Is not affiliated with or endorsed by Fred Baptiste
- Does not grant access to the original course
- Should be used alongside a legitimate enrollment in the course

The notes, experiments, and original implementations in this repository reflect my personal learning process. Third-party names, trademarks, exercises, and instructional material remain the property of their respective owners.

## License

The original code in this repository is distributed under the terms of the [MIT License](LICENSE), unless otherwise stated.

```text
MIT License

Copyright (c) 2026 Simeon Chifligarov
```

The MIT license applies only to material for which the repository owner holds the necessary rights. It does not override the ownership or licensing of third-party course material.

## Author

**Simeon Chifligarov**

- GitHub: [@SimeonChifligarov](https://github.com/SimeonChifligarov)
- Repository: [Python 3 Deep Dive — Part 2](https://github.com/SimeonChifligarov/Python_3_Deep_Dive_Part_2_Iterators_Generators_Udemy_by_Fred_Baptiste)

---

<div align="center">

### If this repository helped you, consider giving it a star.

**Learn deeply. Experiment deliberately. Iterate lazily.**

</div>
