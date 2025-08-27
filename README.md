# Hugo template: `hugo-theme-dev`

⚠️ **Experimental - Not ready for production use yet.**

A lightweight Hugo theme designed for `exampleSite` content, component development, and testing.


# Table of contents

- [Usage](#usage)
  - [In projects / `exampleSite`](#usage-module)
  - [Try it directly](#usage-directly)
- [Licensing, copyright](#licensing-copyright)
- [Author information](#author-information)


## Usage<a id="usage"></a>

### As module in projects / `exampleSite`<a id="usage-module"></a>

Add the module path to your [`theme:` configuration](https://gohugo.io/hugo-modules/theme-components/):

```yaml
theme:
  - "golang.foundata.com/hugo-theme-dev"
```

This path refers to a Go / Hugo module. Hugo automatically fetches and imports the theme as a module, so you do **not** need to add it to your `module.imports` manually.
You can then add any additional configuration your `exampleSite` requires.

The theme provides demo content in **English** and **German**, along with a built-in language switcher. If you don't want to provide German content in your examples, you can simply disable the language and/or the language navigation in your site configuration:

```yaml
disableLanguages:
  - "de"

params:
  # Theme-specific features and parameters.
  # All have sensible defaults, so you don't need to define them unless you
  # want to override the behavior globally or per page (via front matter).
  feature:
    langNav: false # default: true
```


### Try it directly<a id="usage-directly"></a>

Clone the repository and run the included example content:

```bash
git clone https://github.com/foundata/hugo-theme-dev.git
cd hugo-theme-dev
HUGO_MODULE_WORKSPACE=hugo.work hugo server --ignoreVendorPaths "**"
```


## Licensing, copyright<a id="licensing-copyright"></a>

<!--REUSE-IgnoreStart-->
Copyright (c) 2025 foundata GmbH (https://foundata.com)

This project is licensed under the GNU General Public License v3.0 or later (SPDX-License-Identifier: `GPL-3.0-or-later`), see [`LICENSES/GPL-3.0-or-later.txt`](LICENSES/GPL-3.0-or-later.txt) for the full text.

The [`REUSE.toml`](REUSE.toml) file provides detailed licensing and copyright information in a human- and machine-readable format. This includes parts that may be subject to different licensing or usage terms, such as third-party components. The repository conforms to the [REUSE specification](https://reuse.software/spec/). You can use [`reuse spdx`](https://reuse.readthedocs.io/en/latest/readme.html#cli) to create a [SPDX software bill of materials (SBOM)](https://en.wikipedia.org/wiki/Software_Package_Data_Exchange).
<!--REUSE-IgnoreEnd-->

[![REUSE status](https://api.reuse.software/badge/github.com/foundata/hugo-theme-dev)](https://api.reuse.software/info/github.com/foundata/hugo-theme-dev)


## Author information<a id="author-information"></a>

This project was created and is maintained by [foundata](https://foundata.com/).
