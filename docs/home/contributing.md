## Installation

To build and preview this site, you must have the following packages installed:

- [mkdocs/mkdocs](https://github.com/mkdocs/mkdocs): the site generator
- [squidfunk/mkdocs-material](https://github.com/squidfunk/mkdocs-material): the Material theme for MkDocs
- [facelessuser/pymdown-extensions](https://github.com/facelessuser/pymdown-extensions): a Python Markdown extension bundle

If you don't want to install the packages locally, use the official [Docker image](https://hub.docker.com/r/squidfunk/mkdocs-material/), which includes everything you need to preview, build, and deploy the documentation site.

```sh
docker pull squidfunk/mkdocs-material
```

For more installation options, see
http://squidfunk.github.io/mkdocs-material/

## Previewing docs

1. Fork and clone this repository.

2. Start the live development server from the project root.

    ```sh
    make serve
    ```

3. Add new files and save your changes.
4. Navigate to http://localhost:8000/ to review your updates.

## Publishing docs

1. Push your changes to the upstream `master` branch.

2. Build the static site files.

    ```sh
    make build
    ```

3. Deploy the documentation site to GitHub Pages.

    ```sh
    make publish
    ```
    
