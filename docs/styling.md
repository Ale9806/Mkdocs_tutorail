# Styling your docs

In order to style our Mkdocs we will access the `mkdocs.yml` file. 

## What is YAML?
[YAML](https://en.wikipedia.org/wiki/YAML) (a recursive acronym for "YAML Ain't Markup Language") is a human-readable data-serialization language. It is commonly used for configuration files and in applications where data is being stored or transmitted

### How to write YAML 
The basic structure of a YAML file is a map. 

A map is made of  keys and values all the way down:

```yml
key: value
```

You can denote a list using dashes:

```yml
list:
    - element1: file.txt
    - element2: file.md
    - element3: photo.png
```

## Configure Pages and Navigation

The nav configuration setting in your mkdocs.yml file defines which pages are included in the global site navigation menu as well as the structure of that menu. If not provided, the navigation will be automatically created by discovering all the Markdown files in the documentation directory. An automatically created navigation configuration will always be sorted alphanumerically by file name (except that index files will always be listed first within a sub-section). You will need to manually define your navigation configuration if you would like your navigation menu sorted differently.

A minimal navigation configuration could look like this:

```yml
nav:
    - 'index.md'
    - 'about.md'
```

To override the title in the nav setting add a title right before the filename.

```yml
nav:
    - Home: 'index.md'
    - About: 'about.md'
```

Navigation sub-sections can be created by listing related pages together under a section title. For example:

All paths in the navigation configuration must be relative to the docs_dir configuration option. If that option is set to the default value, docs, the source files for the above configuration would be located at docs/index.md and docs/about.md

```yml
nav:
    - Home: 'index.md'
    -'User Guide':
        -'Writing your docs': 'writing-your-docs.md'
        -'Styling your docs': 'styling-your-docs.md'
    - About:
        -'License': 'license.md'
        -'Release Notes': 'release-notes.md'
```
## Themes 
MkDocs includes a couple built-in themes as well as various third party themes, all of which can easily be customized with extra CSS or JavaScript or overridden from the theme's custom_dir. You can also create your own custom theme from the ground up for your documentation.

To use a theme that is included in MkDocs, simply add this to your `mkdocs.yml` config file.

`
theme: [name of theme]
`

MkDocs comes with some pre-built themes, but you can exapnd your arsenal with Boostrap Themes. [The Bootstrap theme](https://mkdocs.readthedocs.io/en/0.15.2/user-guide/styling-your-docs/)  provides 12 different themed Bootstrap themes based on the Bootswatch project.

In order to acces this themes you need to install them via pip

`pip install mkdocs-bootstrap` or `pip install mkdocs-bootswatch`

