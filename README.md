# Continuous Delivery Foundation Landscape

[![Netlify Status](https://api.netlify.com/api/v1/badges/38f97d3e-ec09-4de5-aa53-49f9e5c3eabb/deploy-status)](https://app.netlify.com/sites/cdf-landscape/deploys)

![CDF Landscape Logo](https://github.com/cdfoundation/artwork/blob/main/cdf/other/landscape/cdf-landscape-horizontal-color-logo.svg)

- [CDF Landscape](#cloud-native-landscape)
  * [Current Version](#current-version)
  * [Interactive Version](#interactive-version)
  * [New Entries](#new-entries)
  * [Logos](#logos)
  * [SVGs](#svgs)
  * [Installation](#installation)
  * [Corrections](#corrections)
  * [External Data](#external-data)
  * [Best Practices Badge](#best-practices-badge)
  * [Non-Updated Items](#non-updated-items)
  * [License](#license)
  * [Formats](#formats)
  * [Vulnerability reporting](#vulnerability-reporting)
  * [Adjusting the Landscape View](#adjusting-the-landscape-view)

This landscape is intended as a map to explore various tools and services that support a continuous delivery-oriented software environment from individual process steps to full pipeline orchestration, and also shows the member companies of the LF Continuous Delivery Foundation. It is modeled after the Cloud Native Computing Foundation (CNCF) [landscape](https://landscape.cncf.io) and based on the same open source code.

## Current Version

[![CDF Landscape](https://landscape.cd.foundation/images/landscape.png)](https://landscape.cd.foundation/images/landscape.png)

## Interactive Version

Please see [landscape.cd.foundation](https://landscape.cd.foundation).

## New Entries

* We welcome additions for CI/CD projects that clearly fit in an existing landscape category, and that have 300+ GitHub stars. 
* Put the project in the single category where it best fits.
* We are unlikely to create a new category for projects as we'd rather find the best home with the current options.
* Projects must be hosted on or mirrored to GitHub.
* Your project or company needs a logo and the logo needs to include the name.
* Crunchbase organization should be the company or organization that controls the software. That is normally the owner of the trademark, whether or not a trademark has been formally filed.

 If a project doesn't match the above new entry guidelines, you may still open a pull request (PR) to have the project included in the CDF landscape, but please provide additional information as to why an exception is required.

If you think your project should be included, please open a PR to add it to [landscape.yml](landscape.yml). It is necessary to include a logo in the PR. For the logo, upload an SVG to the `hosted_logos` directory and reference it there.

Netlify will generate a staging server for you to preview your updates. Please check that the logo and information appear correctly and then add `LGTM` to the pull request confirming your review and requesting a merge.

## Logos

The following rules will produce the most readable and attractive logos:

1. We require SVGs, as they are smaller, display correctly at any scale, and work on all modern browsers. Please note that we require pure SVGs and will reject SVGs that contain embedded PNGs since they have the same problems of being bigger and not scaling seamlessly. We also require that SVGs convert fonts to outlines so that they will render correctly whether or not a font is installed. For additional directions on how to source logo SVGs and how to conform to landscape SVG requirements, please see [SVGs](#svgs) below.
1. When multiple variants exist, use stacked (not horizontal) logos. For example, we use the second column (stacked), not the first (horizontal), of CDF project [logos](https://github.com/cdfoundation/artwork).
1. Don't use reversed logos (i.e., with a non-white, non-transparent background color). If you only have a reversed logo, create an issue with it attached and we'll produce a non-reversed version for you.
1. Logos must include the company, product or project name in English. It's fine to also include words from another language. If you don't have a version of your logo with the name in it, please open an issue and we'll create one for you (and please specify the font).
1. Match the item name to the English words in the logos. So an Acme Rocket logo that shows "Rocket" should have product name "Rocket", while if the logo shows "Acme Rocket", the product name should be "Acme Rocket". Otherwise, logos look out of place when you sort alphabetically.
1. Google images is often the best way to find a good version of the logo (but ensure it's the up-to-date version). Search for [grpc logo filetype:svg](https://www.google.com/search?q=grpc+logo&tbs=ift:svg,imgo:1&tbm=isch) but substitute your project or product name for grpc.
1. Upload the SVG to the `hosted_logos` directory.

## SVGs

[Directions](https://github.com/cncf/landscapeapp/blob/master/README.md#logos) on how to conform to landscape SVG requirements.

## Installation

To edit the landscape, it's not necessary to install and run the app locally.

1. You can edit [landscape.yml](landscape.yml) via the GitHub web interface.
2. To add a new card, fork and clone this repo to have a local copy, make changes to [landscape.yml](landscape.yml), add the required SVG to the `hosted_logos` directory, and create a PR.
Netlify will generate a staging server for you to preview your changes. After about 10 minutes, a link will be added to your PR for you to preview your updates. Please check that the logo and information appear correctly.

If desired, you can install and run the landscape app locally with the [install directions](INSTALL.md).

## Corrections

Please open a pull request with edits to [landscape.yml](landscape.yml). The file [processed_landscape.yml](processed_landscape.yml) is generated and so should never be edited directly.

If the error is with data from [Crunchbase](https://www.crunchbase.com/) you should open an account there and edit the data. If you don't like a project description, edit it in GitHub. If your project isn't showing the license correctly, you may need to paste the unmodified text of the license into a LICENSE file at the root of your project in GitHub, in order for GitHub to serve the license information correctly.

## External Data

The canonical source for all data is [landscape.yml](landscape.yml). Once a day, we download data for projects and companies from the following sources:

* Project info from GitHub
* Funding info from [Crunchbase](https://www.crunchbase.com/)
* Market cap data from Yahoo Finance
* CII Best Practices Badge [data](https://bestpractices.coreinfrastructure.org/)

The update server enhances the source data with the fetched data and saves the result in [processed_landscape.yml](processed_landscape.yml). The app loads a JSON representation of processed_landscape.yml to display data.

## Best Practices Badge

As explained at https://bestpractices.coreinfrastructure.org/:
>The Linux Foundation (LF) Core Infrastructure Initiative (CII) Best Practices badge is a way for Free/Libre and Open Source Software (FLOSS) projects to show that they follow best practices. Projects can voluntarily self-certify, at no cost, by using this web application to explain how they follow each best practice. The CII Best Practices Badge is inspired by the many badges available to projects on GitHub. Consumers of the badge can quickly assess which FLOSS projects are following best practices and as a result are more likely to produce higher-quality secure software.

The interactive landscape displays the status (or non-existence) of a badge for each open-source project. There's also a feature not available through the filter bar to see all items [with](https://landscape.cd.foundation/?bestpractices=yes) and [without](https://landscape.cd.foundation/?bestpractices=no) badges. Note that a passing badge is a requirement for projects to [graduate](https://github.com/cncf/toc/blob/master/process/graduation_criteria.adoc) in the CDF.

## Non-Updated Items

We generally remove open source projects that have not had a commit in over three months. Note that for projects not hosted on GitHub, we need them to mirror to GitHub to fetch updates, and we try to work with projects when their mirrors are broken. Here is the view of projects sorted by the last update: https://landscape.cd.foundation/?grouping=no&license=open-source&sort=latest-commit

We generally remove closed source products when they have not tweeted in over three months. This doesn't apply to Chinese companies without Twitter accounts, since Twitter is blocked there. Here is a view of products sorted by the last tweet: https://landscape.cd.foundation/?grouping=no&license=not-open-source&sort=latest-tweet

Items that have been removed can apply to be re-added using the regular New Entries criteria above.

## License

This repository contains data received from [Crunchbase](http://www.crunchbase.com). This data is not licensed pursuant to the Apache License. It is subject to Crunchbase’s Data Access Terms, available at [https://data.crunchbase.com/v3.1/docs/terms](https://data.crunchbase.com/v3.1/docs/terms), and is only permitted to be used with this Landscape Project which is hosted by the Linux Foundation.

Everything else is under the Apache License, Version 2.0, except for project and product logos, which are generally copyrighted by the company that created them, and are simply cached here for reliability. The trail map, static landscape, serverless landscape, and [landscape.yml](landscape.yml) file are alternatively available under the [Creative Commons Attribution 4.0 license](https://creativecommons.org/licenses/by/4.0/).

## Formats

The CDF Landscape is available in these formats:

* [PNG](https://landscape.cd.foundation/images/landscape.png)
* [PDF](https://landscape.cd.foundation/images/landscape.pdf)

## Issue and Vulnerability reporting

Please open an [issue](https://github.com/cdfoundation/cdf-landscape/issues/new) or, for sensitive information, email info@cd.foundation. Original source code inquiries: info@cncf.io

## Adjusting the Landscape View
The file [settings.yml](settings.yml) describes the key elements of a landscape big picture.
It specifies where to put these sections: CI & Pipeline Orchestration, Continuous Automation, Config & Library Management, Infrastructure Deployments, Container Registry and Image Build,
DevSecOps & Monitoring, Change and Defect Management, Protocols and Messaging, CDF Members.
Also it specifies where to locate the link to the serverless preview and an info with a QR code.

All these elements should have `top`, `left`, `width` and `height` properties to
position them.
Properties `rows` and `cols` specify how many columns or rows we expect in a
given horizontal or vertical section.
The `fit_width` property is used to get rid of extra space on the right of a section.

When we see that those elements can not fit the sections, we need to either increase
the width of all the horizontal sections, or increase height and amount of rows
in a single horizontal section and adjust the position of sections below.

Beside that, we have to adjust the width of a parent div (1620), the width in a
`src/components/BigPicture/FullscreenLandscape.js` (1640) and the width in a
`tools/renderLandscape.js` (6560, because of x4 zoom and margins)

Sometimes the total height is changed too, then we need to adjust the height the
same way as we adjust the width.
