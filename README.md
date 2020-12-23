# IDOM Package Cookiecutter

![Test](https://github.com/idom-team/idom-package-cookiecutter/workflows/Test/badge.svg) [![Gitter](https://badges.gitter.im/idom-team/idom.svg)](https://gitter.im/idom-team/idom?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

A [`cookiecutter`](https://cookiecutter.readthedocs.io/en/1.7.2/README.html) template for packaging Javascript components with IDOM

# About IDOM

IDOM is a framework for creating highly interactive web pages purely in Python. However,
IDOM also provides a way to natively interface with the Javascript ecosystem. This
repository defines a basic template for creating packages wich distribute Javascript for
use in IDOM-based applications.

For more information about IDOM refer to its [documentation](https://idom-docs.herokuapp.com/docs/index.html).

# Usage

Install [`cookiecutter`](https://cookiecutter.readthedocs.io/en/1.7.2/README.html) with `pip`:

```bash
pip install cookiecutter
```

Then use this repostory template as a cookiecutter to initalize a repository:

```bash
cookiecutter https://github.com/idom-team/idom-package-cookiecutter.git
```

As the template is being constructed you will be prompted to fill out the following information:

| Field                       | Description                                                                         |
| --------------------------- | ----------------------------------------------------------------------------------- |
| `author_name`               | your name or the name of your organization                                          |
| `author_email`              | your email of the email of your organization                                        |
| `repository_name`           | the name of your repository's root directory                                        |
| `repository_url`            | the URL your repository can be found at                                             |
| `python_package_name`       | the name of the "backend" Python package your Javascript components will be used in |
| `npm_package_name`          | the name of the "frontend" Javascript package used by your Python package           |
| `project_short_description` | a brief summary used to describe both Python and Javascript packages                |

After this you should find a new directory named after the given `repository_name`, the key contents of which are:

| Directory                | Contents                                                                                          |
| ------------------------ | ------------------------------------------------------------------------------------------------- |
| `js/`                    | a bare-bones Javascript component that is bundled with [Rollup](https://rollupjs.org/)            |
| `{python_package_name}/` | minimial code required to load the Javascript component                                           |
| `tests/`                 | a basic [`selenium`](https://selenium-python.readthedocs.io/)-based test suite for your component |
