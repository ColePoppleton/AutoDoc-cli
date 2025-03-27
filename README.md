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
