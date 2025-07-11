## Development Contexts

- Use context7 for documentation of frameworks, libraries, packages

## Project Requirements

### Python Environment
- ALWAYS activate and use the Python virtual environment `.venv` when working on this project
- Before running any Python code: `source .venv/bin/activate`
- All dependencies are managed by Poetry in `pyproject.toml`
- To add dependencies: `poetry add <package-name>`
- To add dev dependencies: `poetry add --group dev <package-name>`
- To install all dependencies: `poetry install`
- Package source code is in `src/trenddit_flow/`

### Development Methodology
- Follow Test-Driven Development (TDD) approach:
  1. Write tests first before implementing functionality
  2. Write minimal code to make tests pass
  3. Refactor while keeping tests green
  4. Ensure comprehensive test coverage

### Architecture Patterns
- Apply SOLID principles:
  - **S**ingle Responsibility: Each class/function should have one reason to change
  - **O**pen/Closed: Open for extension, closed for modification
  - **L**iskov Substitution: Derived classes must be substitutable for base classes
  - **I**nterface Segregation: Many specific interfaces are better than one general interface
  - **D**ependency Inversion: Depend on abstractions, not concretions

- Follow DRY (Don't Repeat Yourself):
  - Extract common functionality into reusable functions/classes
  - Use configuration and parameters instead of duplicating code
  - Create abstractions for repeated patterns