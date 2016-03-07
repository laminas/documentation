# Contributing to the Documentation

Contributions to the documentation are appreciated greatly, and any and all contributions are
accepted. If you are looking to contribute to the documentation, issues are raised against each of
the components' individual repositories on their GitHub issue trackers, and are tagged with
`documentation`.

## Writing Styles

Documentation should be written in a consistent style. Some guidelines on how to write include:

- Use gender neutral pronouns when addressing a hypothetical person. Avoid usage of `he`, `she`,
  `him` and `her`. Instead use `they`, `them`, `their`, and similar.

- Try and use the second plural form rather than `I`. Terms like `we` make the documentation feel
  more inclusive.

- Spelling should be American English. Please spell-check your contribution before submitting.

## Markdown

Documentation should be written in [GitHub Flavored Markdown](https://help.github.com/articles/github-flavored-markdown/),
with some provisions in place to provide consistency:

- Use fenced code blocks to surround code examples, including the php demarcation (or other
  language-appropriate demarcation when appropriate):

<pre lang="no-highlight"><code>// PHP code:
```php
$person = new Person();
$person->setName('Cave Johnson');
```

// JSON:
```json
{
    "name": "zendframework/zend-diactoros"
}
```
</code></pre>

- Surround method names, class names, variable names, constants, etc. with backticks
  (<code>`</code>) when referencing them inline:

<pre lang="no-highlight"><code>Use the `firePortal()` method to grab a `Portal` class from any `PortalGun` object.
</code></pre>

- Suffix method and function names with parens, even if you are not specifying arguments:
  e.g., `isValid()`.

- When creating headers, use the `#` tag (rather than underlining headings with `=`, `-`, or
  similar). The number of `#` tags denotes the level of heading:

<pre lang="no-highlight"><code># Heading One

## Heading Two

### Heading Three
</code></pre>

- Limit line lengths to 100 characters. This ensures that any given line will be visible without
  horizontal scrolling when viewing diffs, or when working with documentation offline, and will improve
  reading comprehension. If possible, set line lengths and wrapping in your editor or IDE.

  Exceptions will be made for lines containing links, to ensure they are rendered properly.

## Documentation Files

In general:

- All documentation files must be under the `doc/book/` subdirectory of a component.

- All documentation files must be markdown, and use the `.md` filename suffix.

- Documentation filenames must consist of lowercase ASCII letters, digits, periods, and dashes only.

Occasionally, you will need to include images for documentation; e.g., screenshots. Place these in
`doc/html/image/`, and commit them to the repository. When doing so, you will also need to:

- Remove the line `doc/html/` from the project `.gitignore` file.
- Create the `doc/html/image/` directory.
- Create a `doc/html/.gitignore` file with the contents `*.html`.

## Rendering Documentation

Documentation may be rendered for individual components or for the full manual, using
[bookdown](http://bookdown.io). We recommend installing `bookdown` globally:

```console
$ composer global require bookdown/bookdown
```

You can keep it up-to-date using:

```console
$ composer global update bookdown/bookdown
```

`bookdown` requires a `bookdown.json` file to describe the "book" contents. This must be placed in
`doc/bookdown.json` for the component.

To render documentation for a component, invoke the `bookdown` command, passing it that location:

```console
$ bookdown doc/bookdown.json
```

This will render to the `doc/html/` directory. Do **not** commit rendered documentation to the
repository! (Repositories *should* have `*.html` in their `.gitignore` file to prevent this,
however.)

You can preview the documentation using the `php` executable's built-in web server:

```console
# From the project root:
$ php -S 0.0.0.0:8000 -t doc/html/
```

After starting that, you can browse to http://localhost:8000 to view the rendered documentation.

The above will also work for documentation in this repository.


## Conduct

Please see our [CONDUCT.md](CONDUCT.md) to understand expected behavior when interacting with others in the project.
