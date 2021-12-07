# Spiny Custom Model Template

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


### Create a Repo
These instructions may have caused the following error: Failed to install pre-commit hooks. Please run `pre-commit install` by your self.  This is due to not having a repository. 

Go to github.
Log in to your account. Go to the D17 repositories.
Click the new repository button in the top-right. You’ll have an option there to initialize the repository with a README file, but I don’t.
Click the “Create repository” button and create your repository.  

From the command line:
run `pre-commit install` if that failed before
cd into your created project 
git init 
git remote add origin https://github.com/D17Team/project.git

## Deploy to the server 

Once you have install everything and write you code under the script, you push directly to the main branch. (using git add, git commit, git push)

The push will trigger a workflow that will deploy your project to our server.
For more details about the workflow you can check the code under `{{cookiecutter.project_name}}/.github/publish.yml`

PS : just check the publish.yml file and check the repository name if it was correctly rendered
