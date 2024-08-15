= POC Architecture as Code

== Project Description

This project is a proof-of-concept for investigating the possibility to use [LinkML](https://linkml.io/) to manage ontology for describing system architecture.
It include the creation of meta-ontologies like ArchiMate, DCAT and DataProduct, that will be used to describe a given system architecture.

== Installation Instructions

To run the site locally use [Python](https://www.python.org/) 3.11+. It will likely be easiest to use a Python virtual environment as shown below to install the dependencies.
```cmd
python -m venv venv
venv\Scripts\activate
pip install mkdocs-material linkml
```
For exact (known working) versions of dependencies, run `pip install -r requirements.txt` instead.

Once installed, you can then run the documentation site locally with hot reload using `mkdocs serve`
```cmd
mkdocs serve
```
Or you can build the static HTML files once with
```sh
mkdocs build
```

== Usage

This project uses [LinkML](https://linkml.io/) to generate Markdown files from LinkML schemas. So a typical workflow for working on this project is to add or update LinkML `.yaml` files to the `schemas` subdirectory, do the following:

1. Run the `make clean` command to delete all Markdown files in the subdirectories of `docs`. It does not change `images` and `stylesheets` subdirectories or the `docs/index.md` file.
```sh
make clean
```
2. Use [LinkML's Markdown generator](https://linkml.io/linkml/generators/markdown.html) to create the static Markdown files from the LinkML schema by running `make markdown`
```sh
make mardown
```

This is using `Makefile` to hide the complexity of running commands manually. You can see the full usage by running `make help`.

Note that if a new profile has been added, make sure to add it to the list in the `docs/index.md` file.

== Configuration

* If applicable, explain any configuration options or settings users may need to adjust.
* Provide guidance on how to customize or configure the project according to specific needs.

== Contributing Guidelines

* Encourage contributions from the community by outlining how others can contribute to your project.
* Include guidelines for submitting bug reports, feature requests, or code contributions.
* Specify the preferred workflow for contributions, such as using pull requests or issue tracking.

== License Information

* Clearly state the license under which your project is released.
* Include license text or provide a link to the full license file for reference.
* Ensure that your chosen license aligns with your project's intended use and distribution.

== Acknowledgements

* Acknowledge and give credit to individuals or organizations that have contributed to your project.
* Include links to relevant resources or libraries that you've used in your project.

== Contact Information

* Provide contact information or links to your social media profiles, website, or email address.
* Encourage users to reach out with questions, feedback, or inquiries about the project.

== Badges

* Include badges for build status, code coverage, version, etc., if applicable.
* Badges can provide quick insights into the project's health and status.

== Table of Contents

* Include a table of contents with links to different sections of the README for easy navigation.

== Screenshots or Demo

* If applicable, include screenshots, gifs, or links to demos showcasing your project in action.
* Visual elements can help users quickly understand what your project does and its capabilities.

== Changelog

* Maintain a changelog or release notes section to document changes between different versions of your project.
* Include information about new features, bug fixes, and improvements in each release.
