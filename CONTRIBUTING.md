# Contributing

The documentation for each repository is available in the "**docs/**" directory of that repository.
It is written in [Markdown format] and built using [MkDocs].

## Testing Your Changes Locally

We **strongly** encourage you to test your changes locally before contributing them.
To do so, you first need to do three things; these are:

1. Have MkDocs installed.
2. Have the Laminas documentation theme available to the laminas-form directory.
3. Update `mkdocs.yml` to build the docs using the documentation theme.

To complete these steps, please follow the instructions below.

1. [Install MkDocs].
2. Install [the PyMdown Extensions].
3. Clone the [documentation-theme repository] locally.
    ```
    git clone git@github.com:laminas/documentation-theme.git documentation-theme
    ```
4. Copy the theme directory from the cloned documentation-theme repository to the root directory of this project.
5. Add the following Yaml snippet to `mkdocs.yml`, changing it to suit the repository that you are working with.
    ```yaml
    # The following example assumes that you are working with laminas-form
    repo_url: 'https://github.com/<your-project>'
    extra:
        repo_name: <your-project>
        project: Components
        base_url: https://docs.laminas.dev/
        project_url: https://docs.laminas.dev/components/
    theme:
        name: null
        custom_dir: 'theme/'
        static_templates:
          - pages/404.html
    markdown_extensions:
        - pymdownx.superfences:
        - pymdownx.tabbed:
        - toc:
            toc_depth: 2
    ```

When you have completed each of these steps then, from the root directory of the project, run `mkdocs serve`.
This builds the documentation locally, making it available on `http://127.0.0.1:8000`, if the port is not already in use, and actively watch for changes.
If changes are detected, the documentation is automatically regenerated, saving you the trouble of having to do so manually.

You should see initial output similar to the following if the process is successful.

```console
INFO    -  Building documentation...
INFO    -  Cleaning site directory
INFO    -  Documentation built in 2.47 seconds
[I 200430 22:06:08 server:296] Serving on http://127.0.0.1:8000
INFO    -  Serving on http://127.0.0.1:8000
[I 200430 22:06:08 handlers:62] Start watching changes
INFO    -  Start watching changes
[I 200430 22:06:08 handlers:64] Start detecting changes
INFO    -  Start detecting changes
```

When you view the documentation, it should be properly themed, similar to the following screenshot.

![Example of locally generated Laminas documentation](/images/example-of-generated-documentation.png)

## Need Help?

If you have trouble with any of these steps, come and ask for help in [the Laminas Slack #documentation channel].

[documentation-theme repository]: https://github.com/laminas/documentation-theme
[Install MkDocs]: https://www.mkdocs.org/#installation
[MkDocs]: https://www.mkdocs.org/
[Markdown format]: https://www.markdownguide.org/
[the Laminas Slack #documentation channel]: https://laminas.slack.com
[the PyMdown Extensions]: https://facelessuser.github.io/pymdown-extensions/installation/
