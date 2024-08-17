## Django Boilerplate Project

This project includes default auto-generated Django project except for
removing comments and minor tweaks (using dotenv variables for secrets).

### Usage
1. Clone project
   ```shell
   git clone git@github.com:Azen0n/django-boilerplate.git
   ```
2. Set new origin url
   ```shell
   git remote set-url origin new_origin_goes_here
   ```
3. Update the project information in `pyproject.toml`.
Ensure you compile any new dependencies if you make changes to them (see
[New Dependencies](#new-dependencies))

### Installation
1. Install Python 3.12
2. Install [uv](https://github.com/astral-sh/uv#getting-started)
3. Create a virtual environment via uv and activate it
    ```shell
    uv venv venv --python=3.12
    source venv/bin/activate
    ```
4. Install requirements
    ```shell
    uv pip install -r requirements.txt
    ```
5. Copy `example.env` to `.env` and set values
    ```shell
    cat example.env > .env
    ```

### New Dependencies
To include new dependencies, add packages to the dependencies list in the
pyproject.toml file, then compile them using
```shell
uv pip compile pyproject.toml -o requirements.txt
```
and install
```shell
uv pip install -r requirements.txt
```
