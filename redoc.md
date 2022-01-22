<div align="center">
  <img alt="Redoc logo" src="https://raw.githubusercontent.com/Redocly/redoc/master//docs/images/redoc.png" width="400px" />

  # Generate interactive API documentation from OpenAPI definitions

  [![Build Status](https://travis-ci.com/Redocly/redoc.svg?branch=master)](https://travis-ci.com/Redocly/redoc) [![Coverage Status](https://coveralls.io/repos/Redocly/redoc/badge.svg?branch=master&service=github)](https://coveralls.io/github/Redocly/redoc?branch=master) [![npm](http://img.shields.io/npm/v/redoc.svg)](https://www.npmjs.com/package/redoc) [![License](https://img.shields.io/npm/l/redoc.svg)](https://github.com/Redocly/redoc/blob/master/LICENSE)

  [![bundle size](http://img.badgesize.io/https://cdn.jsdelivr.net/npm/redoc/bundles/redoc.standalone.js?compression=gzip&max=300000)](https://cdn.jsdelivr.net/npm/redoc/bundles/redoc.standalone.js) [![npm](https://img.shields.io/npm/dm/redoc.svg)](https://www.npmjs.com/package/redoc) [![](https://data.jsdelivr.com/v1/package/npm/redoc/badge)](https://www.jsdelivr.com/package/npm/redoc) [![Docker Build Status](https://img.shields.io/docker/build/redocly/redoc.svg)](https://hub.docker.com/r/redocly/redoc/)
</div>

**This is the README for the `2.x` version of Redoc (React-based).**
**The README for the `1.x` version is on the [v1.x](https://github.com/Redocly/redoc/tree/v1.x) branch**

## About Redoc

Redoc is an open-source tool for generating documentation from OpenAPI (fka Swagger) definitions.

By default Redoc offers a three-panel, responsive layout:

- The left panel contains a search bar and navigation menu.
- The central panel contains the documentation.
- The right panel contains request and response examples.

![Redoc demo](https://raw.githubusercontent.com/Redocly/redoc/master/demo/redoc-demo.png)

## Live demo

If you want to see how Redoc will render your OpenAPI definition,
you can try it out online at https://redocly.github.io/redoc/.

A version of the Swagger Petstore API is displayed by default.
To test it with your own OpenAPI definition,
enter the URL for your definition and select **TRY IT**.

## Redoc vs. Reference vs. Portals

Redoc is Redocly's community-edition product. Looking for something more?
Checkout the following feature comparison of Redocly's premium products versus Redoc:

| Features                     | Redoc     | Reference | Portals     |
|------------------------------|:---------:|:---------:|:-----------:|
| **Specs**                    |           |           |             |
| Swagger 2.0                  | √         | √         | √           |
| OpenAPI 3.0                  | √         | √         | √           |
| OpenAPI 3.1                  | √ (basic) | √         | √           |
|                              |           |           |             |
| **Theming**                  |           |           |             |
| Fonts/colors                 | √         | √         | √           |
| Extra theme options          |           | √         | √           |
|                              |           |           |             |
| **Performance**              |           |           |             |
| Pagination                   |           | √         | √           |
| Search (enhanced)            |           | √         | √           |
| Search (server-side)         |           |           | √           |
|                              |           |           |             |
| **Multiple APIs**            |           |           |             |
| Multiple versions            |           | √         | √           |
| Multiple APIs                |           |           | √           |
| API catalog                  |           |           | √           |
|                              |           |           |             |
| **Additional features**      |           |           |             |
| Try-it console               |           | √         | √           |
| Automated code samples       |           | √         | √           |
| Deep links                   |           | √         | √           |
| More SEO control             |           |           | √           |
| Contextual docs              |           |           | √           |
| Landing pages                |           |           | √           |
| React hooks for more control |           |           | √           |
| Personalization              |           |           | √           |
| Analytics integrations       |           |           | √           |
| Feedback                     |           |           | Coming Soon |

Refer to the Redocly's documentation for more information on these products:

- [Portals](https://redoc.ly/docs/developer-portal/introduction/)
- [Reference](https://redoc.ly/docs/api-reference-docs/getting-started/)
- [Redoc](https://redoc.ly/docs/redoc/quickstart/intro/)

## Features
- Responsive three-panel design with menu/scrolling synchronization
- [Multiple deployment options](https://redoc.ly/docs/redoc/quickstart/intro/)
- [Server-side rendering (SSR) ready](https://redoc.ly/docs/redoc/quickstart/cli/#redoc-cli-commands)
- Ability to integrate your API introduction into the side menu
- [Simple integration with `create-react-app`](https://redoc.ly/docs/redoc/quickstart/react/)

  [Example repo](https://github.com/APIs-guru/create-react-app-redoc)
- [Command-line interface to bundle your docs into a **zero-dependency** HTML file](https://redoc.ly/docs/redoc/quickstart/cli/)
- Neat **interactive** documentation for nested objects <br>
  ![](docs/images/nested-demo.gif)

## Customization options
[<img alt="Customization services" src="http://i.imgur.com/c4sUF7M.png" height="60px">](https://redoc.ly/#services)
- High-level grouping in side-menu with the [`x-tagGroups`](https://redoc.ly/docs/api-reference-docs/specification-extensions/x-tag-groups/) specification extension
- Branding/customizations using the [`theme` option](https://redoc.ly/docs/api-reference-docs/configuration/theming/)

## Support
- OpenAPI v3.0 support
- Basic OpenAPI v3.1 support
- Broad OpenAPI v2.0 feature support (yes, it supports even `discriminator`) <br>
  ![](docs/images/discriminator-demo.gif)
- Code samples support (via vendor extension) <br>
  ![](docs/images/code-samples-demo.gif)

## Releases
**Important:** all the 2.x releases are deployed to npm and can be used with jsdeliver:
- particular release, for example, `v2.0.0-alpha.15`: https://cdn.jsdelivr.net/npm/redoc@2.0.0-alpha.17/bundles/redoc.standalone.js
- `next` release: https://cdn.jsdelivr.net/npm/redoc@next/bundles/redoc.standalone.js

Additionally, all the 1.x releases are hosted on our GitHub Pages-based CDN **(deprecated)**:
- particular release, for example `v1.2.0`: https://rebilly.github.io/ReDoc/releases/v1.2.0/redoc.min.js
- `v1.x.x` release: https://rebilly.github.io/ReDoc/releases/v1.x.x/redoc.min.js
- `latest` release: https://rebilly.github.io/ReDoc/releases/latest/redoc.min.js - it will point to latest 1.x.x release since 2.x releases are not hosted on this CDN but on unpkg.

## Version Guidance
| Redoc Release | OpenAPI Specification |
|:--------------|:----------------------|
| 2.0.0-alpha.54| 3.1, 3.0.x, 2.0       |
| 2.0.0-alpha.x | 3.0, 2.0              |
| 1.19.x        | 2.0                   |
| 1.18.x        | 2.0                   |
| 1.17.x        | 2.0                   |

## Showcase
- [Rebilly](https://api-reference.rebilly.com/)
- [Docker Engine](https://docs.docker.com/engine/api/v1.25/)
- [Zuora](https://www.zuora.com/developer/api-reference/)
- [Discourse](http://docs.discourse.org)
- [Commbox](https://www.commbox.io/api/)
- [APIs.guru](https://apis.guru/api-doc/)
- [BoxKnight](https://www.docs.boxknight.com/)

## Lint OpenAPI definitions

Redocly's OpenAPI CLI is an open source command-line tool that you can use to lint
your OpenAPI definition. Linting helps you to catch errors and inconsistencies in your
OpenAPI definition before publishing.

Refer to [Lint configuration](https://redoc.ly/docs/cli/guides/lint/) in the OpenAPI documentation for more information.

## Deployment

### TL;DR final code example

To render your OpenAPI definition using Redoc, use the following HTML code sample and
replace the `spec-url` attribute with the url or local file address to your definition.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Redoc</title>
    <!-- needed for adaptive design -->
    <meta charset="utf-8"/>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link href="https://fonts.googleapis.com/css?family=Montserrat:300,400,700|Roboto:300,400,700" rel="stylesheet">

    <!--
    Redoc doesn't change outer page styles
    -->
    <style>
      body {
        margin: 0;
        padding: 0;
      }
    </style>
  </head>
  <body>
    <redoc spec-url='http://petstore.swagger.io/v2/swagger.json'></redoc>
    <script src="https://cdn.jsdelivr.net/npm/redoc@latest/bundles/redoc.standalone.js"> </script>
  </body>
</html>

```

For step-by-step instructions for how to get started using Redoc
to render your OpenAPI definition, refer to the
[**Redoc quickstart guide**](https://redoc.ly/docs/redoc/quickstart/intro/).

See [**IE11 Support Notes**](docs/usage-with-ie11.md) for information on
IE support for Redoc.

## Redoc CLI
For more information on Redoc's commmand-line interface, refer to
[**Using the Redoc CLI**](https://redoc.ly/docs/redoc/quickstart/cli/).


## Configuration

### Security Definition location
You can inject the Security Definitions widget into any place in your definition `description`.
For more information, refer to [Security definitions injection](docs/security-definitions-injection.md).

### OpenAPI specification extensions
Redoc uses the following [specification extensions](https://swagger.io/specification/#specificationExtensions):
* [`x-logo`](docs/redoc-vendor-extensions.md#x-logo) - is used to specify API logo
* [`x-traitTag`](docs/redoc-vendor-extensions.md#x-traitTag) - useful for handling out common things like Pagination, Rate-Limits, etc



-----------
## Development
see [CONTRIBUTING.md](.github/CONTRIBUTING.md)