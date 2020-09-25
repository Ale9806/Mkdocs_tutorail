# MkDocs Basics Tutorial 
**This is a fast and perzonalized tutorial for MKDocs**


MkDocs is a simple static site generator that's geared towards building project documentation. Documentation source files are written in Markdown, and configured with a single YAML configuration file.For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Installation
MkDocs supports Python 2.6, 2.7, 3.3 and 3.4.

*  `pip install mkdocs` 


## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server, hosted at local host.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.

## Adding Pages
The process of adding pages consists of two stages:

1.- Add a `.md` file at  the `docs` directory.

2.- Track the file inside the `mkdocs.yml` file.

**Example:**
``` bash
user@~\project\docs$ touch about.md   # Create md file
user@~\project\docs$ cd ..            # Go to parent directory
user@~\project\$  ls                  # List Directories 
docs mkdocs.yml 
user@~\project\$ nano mkdocs.yml      # Open and edit yml file 

GNU nano 2.5.3                New Buffer
site_name: MkLorum                    # Default value 
nav:                                  # Default value 
- Home: index.md                      # Default value 
- About: about.md                     # Add new element to track 

### save, if page is in local host it will be updated automatically ###
```

## Teheming documentation:
We can edit the `mkdocs.yml` to add a theme:
``` bash
site_name: MkLorum
pages:
- Home: index.md
- About: about.md
theme: readthedocs
```

For more on theme customization go to the theme section.


## Building the site
In order to build a site we use: 
`
mkdocs build 
`
This will create a new directory, named `site`.
If you're using source code control such as git you probably don't want to check your documentation builds into the repository. Add a line containing site/ to your .gitignore file.
```
echo "site/" >> .gitignore
```

## Depolyin your docs to Github Pages 
Building is necesary in order to host the source code to pages that are not able to host markdown, github pages is able to host markdow so we do not need to build we only need to:

1.- `git init`, `git add *`, `git commit-m "message"` , `git add remote [origin]`, `git push `

2.-  `mkdocs gh-deploy --clean`
Behind the scenes, MkDocs will build your docs and use the ghp-import tool to commit them to the gh-pages branch and push the gh-pages branch to GitHub.

Use mkdocs gh-deploy --help to get a full list of options available for the gh-deploy command.

