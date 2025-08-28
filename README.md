# Hugo theme: dev

⚠️ **Experimental - Not ready for production use yet.**

A Hugo theme for `exampleSite` content, component development, and testing. It is not a production-ready theme, but rather a sandbox for experimenting. It intentionally provides no styling.

Feel free to use it to explore, debug, and contribute new components!


# Table of contents

- [Installation and usage](#installation)
- [Configuration](#configuration)
- [Demo](#demo)
- [Licensing, copyright](#licensing-copyright)
- [Author information](#author-information)


## Installation and usage<a id="installation"></a>

The theme is intended to be added as Hugo module in your `exampleSite` and sandbox projects. Simply add the following to your [`theme:` configuration](https://gohugo.io/hugo-modules/theme-components/):

```yaml
theme:
  - "golang.foundata.com/hugo-theme-dev"
```

Hugo automatically fetches and import theme module paths as Go/Hugo modules, so you do **not** need to list them under `module.imports` manually. Using modules requires [Hugo, Go, and Git](https://gohugo.io/hugo-modules/use-modules/#prerequisite) to be installed on your system.


## Configuration<a id="configuration"></a>

No additional configuration is required by default.

But the theme provides demo content in **English** and **German**, along with a built-in language switcher. If you don’t want to include German demo content in your examples, you can disable the language and/or the language navigation in your site configuration:

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

There is also a built-in debugging feature, which dumps `.Page`, `.Params` and `.Site.Params` in the footer:

```yaml
params:
  feature:
    debug: true # default: false
```

Every feature can also be controlled per page via front matter:

```yaml
---
title: "Demo homepage"
feature:
  pagesNav: false
  langNav: false
  debug: false
---
```


### Demo<a id="demo"></a>

Clone the repository and run the included example content (requires Hugo, Go, and Git):

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
