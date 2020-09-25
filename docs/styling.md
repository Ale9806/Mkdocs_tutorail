# Styling your docs

MkDocs includes a couple built-in themes as well as various third party themes, all of which can easily be customized with extra CSS or JavaScript or overridden from the theme's custom_dir. You can also create your own custom theme from the ground up for your documentation.

To use a theme that is included in MkDocs, simply add this to your `mkdocs.yml` config file.

`
theme: [name of theme]
`

MkDocs comes with some pre-built themes, but you can exapnd your arsenal with Boostrap Themes. [The Bootstrap theme](https://mkdocs.readthedocs.io/en/0.15.2/user-guide/styling-your-docs/)  provides 12 different themed Bootstrap themes based on the Bootswatch project.

In order to acces this themes you need to install them via pip

`pip install mkdocs-bootstrap` or `pip install mkdocs-bootswatch`