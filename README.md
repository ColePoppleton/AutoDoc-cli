<div align="center">
![GitHub License](https://img.shields.io/github/license/ColePoppleton/AutoDoc-cli)

</div>

# AutoDoc: Your Automated Documentation Generator

AutoDoc is a command-line tool designed to streamline the documentation process for JavaScript/Node.js projects. It automatically generates a basic `README.md` file by parsing your code and extracting relevant information, saving you valuable time and effort.

**Key Features:**

* **Automated README Generation:** Quickly create a foundational `README.md` with project details.
* **JSDoc Parsing:** Extracts documentation from JSDoc-style comments in your code.
* **Dependency Listing:** Automatically lists your project's dependencies from `package.json`.
* **Configurable Sections:** Organize your README with sections for installation, usage, contributing, etc.
* **Customizable Output:** Tailor the generated README to your project's needs.

**Important Note:** AutoDoc is currently in development and requires manual setup.  Future releases will be published to npm for easier installation.

## Table of Contents

* [Installation](#installation)
* [Usage](#usage)
* [Configuration](#configuration)
* [Dependencies](#dependencies)
* [Contributing](#contributing)
* [License](#license)

## Installation

Since AutoDoc is not yet published to npm, you'll need to clone the repository and set it up manually:

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/ColePoppleton/AutoDoc-cli
    cd https://github.com/ColePoppleton/AutoDoc-cli
    ```

2.  **Install dependencies:**

    AutoDoc relies on several Node.js packages. Make sure you have Node.js and npm installed. Then, run:

    ```bash
    npm install
    ```

## Usage

AutoDoc provides two main commands: `init` and `generate`.

### `init` Command

The `init` command initializes a `AutoDoc.yaml` configuration file and sample Markdown files in your project's root directory.

```bash
./index.js init
```

This command will prompt you for:

* Project name: The name of your project.
* Project description: A brief description of your project.
* Generate INSTALL.md?: Whether to create an INSTALL.md file.
* Generate CONTRIBUTING.md?: Whether to create a CONTRIBUTING.md file.
* Generate USAGE.md?: Whether to create a USAGE.md file.
* generate Command

The generate command generates the README.md file based on the settings in docgen.yaml and the content of your code and Markdown files.

```Bash
./index.js generate
```
This command will create (or overwrite) the README.md file in your project's root directory.

## Configuration
AutoDoc uses a docgen.yaml file for configuration. This file is created by the init command and allows you to customize the README generation process.

Example docgen.yaml:

```YAML
projectName: MyProject
projectDescription: A cool project.
files:
  - src/**/*.js
exclude:
  - src/test/**/*.js
output: README.md
sections:
  - title: Installation
    files:
      - ./INSTALL.md
  - title: API Documentation
    files:
      - src/index.js
      - src/utils.js
  - title: Contributing
    files:
      - ./CONTRIBUTING.md
  - title: Dependencies
    files:
      - ./DEPENDENCIES.md
  - title: Usage
    files:
      - ./USAGE.md
```
### Configuration Options:

* projectName: The name of your project (used in generated files).
* projectDescription: A description of your project (included at the beginning of README.md).
* files: An array of file paths or glob patterns to include in documentation generation.
* exclude: An array of file paths or glob patterns to exclude.
* output: The name of the output README file (default: README.md).
* sections: An array of objects defining the sections of your README:
* title: The title of the section.
* files: An array of file paths to include in the section.

## Dependencies
AutoDoc relies on the following Node.js packages:

* commander: For parsing command-line arguments.
* fs-extra: For enhanced file system operations.
* js-yaml: For parsing the docgen.yaml configuration file.
* glob: For file globbing.
* acorn: For parsing JavaScript code into Abstract Syntax Trees (ASTs).
* doctrine: For parsing JSDoc-style comments.
* prompts: For interactive command-line prompts.
These dependencies are automatically installed when you run npm install in the project directory.

## Contributing
We welcome contributions to AutoDoc! Please follow these guidelines:

* Fork the repository on GitHub.
* Create a new branch for your feature or bug fix.
* Make your changes and commit
* Submit a pull request.
