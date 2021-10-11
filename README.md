# Python Project Wizard

This is the skeleton for all the python package we will be deploying in Spiny. 
You can use it to generate a python package projects.
## Features

This tool will create Python project with the following features:

* [Poetry]: Manage version, dependancy, build and release
* [Mkdocs]: Writting your docs in markdown style
* Testing with [Pytest] (unittest is still supported out of the box)
* Code coverage report and endorsed by [Codecov]
* [Tox]: Test your code against environment matrix, lint and artifact check.
* Format with [Black] and [Isort]
* Lint code with [Flake8] and [Flake8-docstrings]
* [Pre-commit hooks]: Formatting/linting anytime when commit/run local tox/CI
* [Mkdocstrings]: Auto API doc generation
* Command line interface using [Python Fire] (optional)
* Continuouse Integration/Deployment by [github actions], includes:
    - publish dev build/official release to our our custom python server
    - publish documents automatically when CI success
    - extract change log from github and integrate with release notes automatically
* Host your documentation from [Git Pages] with zero-config

## Quickstart

### Install cookiecutter

To use this cookiecutter make sure you have installed  cookiecutter.

Make sure you have python and pip installed in your project. 

You can use pip to install the cookiecutter with the following command : 

`pip install cookiecutter`

### Generate a project

To generate the project you can use the following command : 

`cookiecutter https://github.com/D17Team/cookiecutter-pypackage.git`

You’ll be asked to enter values to set your project up. If you don’t know what to enter, stick with the defaults.


## Deploy to the server 

Once you have install everything and write you code under the script, you push directly to the main branch.

The push will trigger a workflow that will deploy your project to our server.
For more details about the workflow you can check the code under `{{cookiecutter.project_name}}/.github/publish.yml`
