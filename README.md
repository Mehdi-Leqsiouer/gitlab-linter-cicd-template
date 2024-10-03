# linter-template

## CICD Templates
This repo implements Gitlab CI/CD templates to lint your code.


## Usage
```yaml
include:
- project: "badgerworks/cicd-template/linter-template"
    ref: <version_tag>
    file: "linter.yml"
```

You need, at the root of the project a requirements.txt file so the pytest tests will run.


## Stages
The following stages are used :
- Python Lint (using Ruff package)
- Terraform lint (with Checkov and "fmt" for format)
- Python tests with Pytest

## Configuration 
| Name                  | description                   | default value |
|-----------------------|-------------------------------|---------------|
| `SRC_DIR`        | Folder containing python code | `src`         ||
| `TEST_DIRECTORY`      | pytest test directory         | `tests`       |
| `COV_FAIL` | minimum coverage for pytest   | `70`          |


