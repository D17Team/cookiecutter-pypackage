# {{ cookiecutter.project_name }}



{{ cookiecutter.project_short_description }}

## How should we install this package?

We are installing the package using poetry , make sure  you have poetry installed on your machine.

If that is the case you can run the following commands.



- `poetry config repositories.auto_tagger http://auto-tagger-pkg-load-balancer-819345320.us-east-2.elb.amazonaws.com/`
- `poetry config http-basic.auto_tagger $PYPI_USERNAME $PYPI_PASSWORD`
- `poetry add {{ cookiecutter.project_slug }} -vvv`

You can can get the password and the username directly from the the slack channel or from any team member. 

## Features

* TODO


## Making Changes to the package

Once you you are done with your changes you can push them directly and it will trigger the Github action to publish the package.

- Run `git tag v1.X.X`
- Run `git push --tags`


## Features

* TODO

## Credits

This package was created with [Cookiecutter](https://github.com/audreyr/cookiecutter) and the [zillionare/cookiecutter-pypackage](https://github.com/zillionare/cookiecutter-pypackage) project template.
