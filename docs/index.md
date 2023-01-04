# Getting started with MkDocs



## File layout

Your docs are regular Markdown files and placed in the `docs` directory, along with a config file `mkdocs.yml` at the top level.


```text
mkdocs.yml
docs/
    index.md
```


## Configure Pages and Navigation

The `nav` configuration setting in your `mkdocs.yml` file defines which pages are included in the global site navigation menu as well as the structure of that menu. 
If not provided, the navigation will be automatically created by discovering all the Markdown files in the `docs`.

An automatically created navigation configuration will always be sorted alphanumerically by file name (except that index files will always be listed first within a sub-section). 
You need to manually define your navigation configuration if you would like your navigation menu sorted differently.

A minimal navigation configuration could look like this:

```yaml
nav:
    - 'index.md'
    - 'about.md'
    - 'additional.md'
```


The above example will result in three navigation items being created at the top level and with their titles inferred from the contents of the Markdown file or, if no title is defined within the file, of the file name. 
To override the title in the `nav` setting add a title right before the filename.

```yaml
nav:
    - Home: 'index.md'
    - About: 'about.md'
    - Resources: 'additional.md'
```


See 100 Days of Docs
