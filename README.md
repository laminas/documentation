# Documentation

This repository exists for the purpose of planning and organizing documentation
changes and milestones for the Laminas Project and related subproject, and to show how to setup and update the documentation locally.

## Setup

To prepare your local development environment to build the documentation locally, follow the steps below:

1. [Install MkDocs](https://www.mkdocs.org/#installation) and all of its dependencies (The installation description for MkDocs also includes the installation of Python.)
2. Install the [Python PyMdown Extensions](https://facelessuser.github.io/pymdown-extensions/installation/#installation_1)

## Building the Documentation Locally

To build the documentation locally, follow the steps below:

1. Clone `laminas/documentation-theme` inside your development branch, by running: `git clone git://github.com/laminas/documentation-theme.git`
2. Build the documentation by running: `./documentation-theme/build.sh -u https://docs.laminas.dev/<your project>/`, swapping `<your project>` for the path of the package you’re working on, e.g., `https://docs.laminas.dev/laminas-hydrator`.

### Viewing Generated Documentation

To view the generated documentation, after building it, open `docs/html/index.html`.
