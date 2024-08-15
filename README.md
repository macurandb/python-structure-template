# Python Project: Structure and Automation with Makefile
This project is designed to provide a robust and standard structure for Python projects, utilizing a Makefile to automate common tasks such as testing, dependency installation, code validation, and documentation generation.

## Requirements

- [Python](https://www.python.org/downloads/)
- [Poetry](https://python-poetry.org/docs/#installation) - For dependency management and virtual environments.
- [Make](https://www.gnu.org/software/make/) - Tool for executing tasks defined in the Makefile.
- [Tox](https://tox.readthedocs.io/en/latest/) - For running tests across multiple environments.
- [Sphinx](https://www.sphinx-doc.org/en/master/) - For generating project documentation.
- [Pylint](https://pylint.pycqa.org/en/latest/) - For code quality and style checking.


## Project Structure

```bash 
.
├── src/                     # Project source code
├── tests/                   # Unit and integration tests
├── docs/                    # Documentation source files
│   ├── source/              # Sphinx source files
│   └── build/               # Generated documentation output
├── pyproject.toml           # Poetry configuration file
├── Makefile                 # Makefile for task automation
└── README.md                # Project documentation
```

## Using the Makefile
    The Makefile in this project is configured to handle various common tasks. Below is a description of each 
    available task:

### Available Tasks

- **`test`**: Run tests using `pytest`.
- **`cov`**: Run tests and generate a coverage report using `pytest-cov`.
- **`install`**: Install dependencies and the package into a `poetry`-managed virtual environment.
- **`lint`**: Run `mypy`, `flake8`, `ruff`, and `pylint` to check code quality.
- **`fmt`**: Format code using `black`.
- **`pylint`**: Run `pylint` to check code quality and style.
- **`test_envs`**: Run tests across multiple environments using `tox`.
- **`docs`**: Generate HTML documentation using Sphinx.

### Running Tasks
        To run any of the tasks defined in the Makefile, simply use the make command followed by the task name.
        For example, to run the tests, you can use:

```bash
make test
```

## Generating Documentation
  To generate the project documentation, use the docs target:

```bash
make docs
```
    This will build the HTML documentation using Sphinx, placing the output in the docs/build/html directory.

## Help
    You can view a list of all available tasks with a brief description by using the command:

```bash
make help
```

### Installation
To set up the project and its dependencies, follow these steps:

Clone the repository:

```bash
git clone <repository_url>
cd <repository_name>
```

### Install the dependencies using poetry:

```bash
make install
```

### Contributing
If you wish to contribute to this project, please ensure that you follow best practices for clean code and utilize the
provided linting, formatting, and documentation tools.