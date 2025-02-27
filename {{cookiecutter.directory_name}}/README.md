# Data Science Cookie Cutter

[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)][pre-commit]
[![Black](https://img.shields.io/badge/code%20style-black-000000.svg)][black]

[pre-commit]: https://github.com/pre-commit/pre-commit
[black]: https://github.com/psf/black

Forked and edited from [Data Science Template](https://github.com/khuyentran1401/data-science-template)

## Quick Start

### Set up the environment

1. Install [Poetry](https://python-poetry.org/docs/#installation)
2. Set up the environment:

```bash
make setup
make activate
```

### Install new packages

To install new PyPI packages, run:

```bash
poetry add <package-name>
```

### Run Python scripts

To run the Python scripts to process data, train model, and run a notebook, type the following:

```bash
make pipeline
```

### View all flow runs

A [flow](https://docs.prefect.io/concepts/flows/) is the basis of all Prefect workflows.

To view your flow runs from a UI, sign in to your [Prefect Cloud](https://app.prefect.cloud/) account or spin up a Prefect Orion server on your local machine:

```bash
prefect orion start
```

Open the URL <http://127.0.0.1:4200/>, and you should see the Prefect UI:

![](images/prefect_cloud.png)

### Run flows from the UI

After [creating a deployment](https://towardsdatascience.com/build-a-full-stack-ml-application-with-pydantic-and-prefect-915f00fe0c62?sk=b1f8c5cb53a6a9d7f48d66fa778e9cf0), you can run a flow from the UI with default parameters:

![](https://miro.medium.com/max/1400/1*KPRQS3aeuYhL_Anv3-r9Ag.gif)
or custom parameters:
![](https://miro.medium.com/max/1400/1*jGKmPR3aoXeIs3SEaHPhBg.gif)

### Auto-generate API documentation

To auto-generate API document for your project, run:

```bash
make docs_save
```

### Run tests when creating a PR

When creating a PR, the tests in your `tests` folder will automatically run.

![](images/github_actions.png)
