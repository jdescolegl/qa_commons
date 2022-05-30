# qa-commons
Functions for common use

## Env setup
### Python Installation
- Install [pyenv](https://github.com/pyenv/pyenv)
- Install Python 3.8 with pyenv: `pyenv install 3.8`
- In project's directory, set python version: `pyenv local <python-version>` (you can check available versions with `pyenv versions`)
- Install [pip](https://pip.pypa.io/en/stable/installing/) if it's not installed after downloading any Python

### Installing dependencies
#### Create a virtual environment
In project's directory:
- `python3.8 -m venv <virtual-env-directory-name>` This will create a directory containing dependencies
- `source path/to/venv/bin/activate` To start virtual environment. After this, you'll see the name of the environment at the beginning of the command line i.e. `(venv) name:uala-arg-prepaid-qa username$` 
- Install dependencies: `pip install -r requirements.txt`. This will read requirements.txt file and install all dependencies (and sub-dependencies) listed there.

To add of update dependencies, you can add it manually to requirements.txt file and then run `pip install -r requirements.txt` again 

## Notes
If you need to use RDS Invoker you must execute the following steps:
- brew install postgresql
- xcode-select --install (If it does not work, install it with app store)
- Add psycopg2 dependency to your project requirements file
- LDFLAGS=$(pg_config --ldflags) pip install -r requirements.txt