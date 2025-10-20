# Project Structure

This document provides a detailed overview of the URFallTraining2025 repository structure and organization.

## Repository Overview

The URFallTraining2025 repository is designed to archive training materials and designs used in the City University UR Fall Training program. The structure is kept simple and organized to facilitate easy navigation and contribution.

## Directory Structure

```
URFallTraining2025/
├── .git/                   # Git version control directory
├── .gitignore              # Git ignore patterns
├── LICENSE                 # CC0 1.0 Universal License
├── README.md               # Project introduction and overview
└── wiki/                   # Wiki documentation
    ├── Home.md             # Wiki home page
    ├── FAQ.md              # Frequently asked questions
    ├── Installation.md     # Installation instructions
    └── Project-Structure.md # This file
```

## File Descriptions

### Root Level Files

#### `.gitignore`

Specifies which files and directories should be ignored by Git. Currently configured to ignore:

- `*.i` - Preprocessed source files
- `*.ii` - Preprocessed C++ source files
- `*.gpu` - GPU-related files
- `*.ptx` - PTX (Parallel Thread Execution) files
- `*.cubin` - CUDA binary files
- `*.fatbin` - Fat binary files

This configuration suggests the project may work with GPU/CUDA programming for robotics applications.

#### `LICENSE`

Contains the CC0 1.0 Universal (CC0 1.0) Public Domain Dedication. This license:
- Places the work in the public domain
- Allows anyone to use, modify, and distribute the work
- Requires no attribution (though it's appreciated)
- Provides no warranty

#### `README.md`

The main entry point for the repository, providing:
- Project title
- Brief description
- Quick overview of the repository's purpose

### Wiki Directory

The `wiki/` directory contains documentation and guides:

#### `Home.md`

The main wiki page providing:
- Project overview
- Table of contents
- Getting started guide
- Quick start instructions
- Contributing guidelines
- License information
- Contact details

#### `FAQ.md`

Frequently Asked Questions covering:
- General project information
- Getting started guidance
- Contributing procedures
- Technical details
- Troubleshooting tips
- License and usage questions

#### `Installation.md`

Comprehensive installation guide including:
- Prerequisites and required software
- Step-by-step installation instructions
- Configuration guidance
- Git setup for first-time users
- Troubleshooting common issues
- Additional tools recommendations

#### `Project-Structure.md`

This document, explaining:
- Repository organization
- File and directory purposes
- Design principles
- Future structure plans

## Design Principles

The repository follows these organizational principles:

### 1. Simplicity

- Minimal directory nesting
- Clear, descriptive file names
- Logical grouping of related materials

### 2. Accessibility

- Well-documented structure
- Clear README at the root
- Comprehensive wiki documentation

### 3. Scalability

- Structure designed to accommodate growth
- Room for additional directories as content expands
- Flexible organization for various content types

### 4. Version Control

- Appropriate `.gitignore` configuration
- Clear commit history
- Branch-based development workflow

## Future Structure

As the project grows, the following additions are anticipated:

### Planned Directories

```
URFallTraining2025/
├── designs/                # Design files and CAD models
│   ├── mechanical/         # Mechanical designs
│   ├── electrical/         # Circuit designs and schematics
│   └── assembly/           # Assembly instructions
├── code/                   # Source code and scripts
│   ├── python/             # Python scripts
│   ├── urscript/           # UR robot scripts
│   └── examples/           # Code examples
├── documentation/          # Additional documentation
│   ├── tutorials/          # Step-by-step tutorials
│   ├── guides/             # User guides
│   └── references/         # Reference materials
├── resources/              # Training resources
│   ├── slides/             # Presentation slides
│   ├── videos/             # Video links or files
│   └── datasets/           # Training datasets
└── tests/                  # Test files and validation
```

### Content Categories

Future content organization will include:

1. **Training Materials**
   - Lecture slides
   - Lab exercises
   - Homework assignments
   - Project descriptions

2. **Design Files**
   - CAD models (STEP, STL, etc.)
   - Circuit schematics
   - PCB layouts
   - Assembly drawings

3. **Source Code**
   - Robot control scripts
   - Simulation code
   - Utility scripts
   - Example programs

4. **Documentation**
   - Technical specifications
   - User manuals
   - API documentation
   - Best practices guides

5. **Resources**
   - Reference materials
   - External links
   - Recommended readings
   - Tool configurations

## Navigation Tips

### Finding Specific Content

1. **Start with README.md**: Get an overview of the project
2. **Check the Wiki**: Browse documentation for detailed information
3. **Use GitHub Search**: Search for specific keywords
4. **Browse by Directory**: Navigate through folders systematically
5. **Check Commit History**: See recent changes and additions

### Understanding File Types

- `.md` - Markdown documentation files
- `.pdf` - PDF documents (when added)
- `.py` - Python source code (when added)
- `.urp` - UR robot programs (when added)
- `.stl` - 3D model files (when added)
- `.dxf` - CAD drawing files (when added)

## Contributing to Structure

When contributing new content:

1. **Follow Existing Patterns**: Match the current organization style
2. **Create Appropriate Directories**: Add new folders as needed
3. **Update Documentation**: Reflect structural changes in wiki
4. **Use Clear Names**: Choose descriptive file and folder names
5. **Add READMEs**: Include README.md in new directories

### Naming Conventions

- Use lowercase with hyphens for multi-word names: `project-structure.md`
- Be descriptive but concise: `ur-robot-config.py` not `file1.py`
- Include version numbers when relevant: `design-v2.stl`
- Use consistent prefixes for related files: `tutorial-01-basics.md`, `tutorial-02-advanced.md`

## Maintenance

The project structure is reviewed and updated:

- When adding major new content types
- Based on user feedback and navigation patterns
- To improve organization and accessibility
- As the project scope evolves

## Questions?

If you have questions about the project structure:

1. Check the [FAQ](FAQ.md)
2. Review the [Home](Home.md) page
3. Open a [GitHub Issue](https://github.com/BnB-GSorg/URFallTraining2025/issues)
4. Suggest improvements via pull request

---

*Last updated: October 2025*
