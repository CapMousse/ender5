---
layout: default
title: Home
nav_order: 1
description: "Ender 5/Ender 5 Pro/Ender 5 Plus unofficial community documentation"
permalink: /
---

# Welcome to the Ender 5 unofficial community documentation
{: .fs-7 }

If you need help to setup your Ender 5 / Ender 5 Pro / Ender 5 Plus or want to upgrade your printer, here is a list of great community ressources and parts to help you on the way.
{: .fs-6 .fw-300 }

This website is not affiliated with Creality and is 100% community managed.

[Join the Reddit community](https://reddit.com/r/ender5){: .btn .btn-primary .fs-5 .mb-4} [Help us on GitHub](https://github.com/CapMousse/ender5){: .btn .btn-outline .fs-5 .mb-4 } [Creality Website](https://www.creality.com/){: .btn .fs-5 .mb-4 }

---

## Getting started

- [User Manual]({% link pages/user-manual.md %})
- [Specifications]({%link pages/specifications.md %})
    - [Ender 5]({%link pages/specifications.md %}#ender-5)
    - [Ender 5 Pro]({%link pages/specifications.md %}#ender-5-pro)
    - [Ender 5 Plus]({%link pages/specifications.md %}#ender-5-plus)
- [Where to purchase]({%link pages/where-to-buy.md %})
- [Maintenance]({%link pages/maintenance.md %})
    - [Update firmware]({%link pages/maintenance.md %}#update-firmware)
    - [Bed leveling]({%link pages/maintenance.md %}#bed-leveling)
    - [Extruder calibration]({%link pages/maintenance.md %}#extruder-calibration)
    - [Linear advance]({%link pages/maintenance.md %}#linear-advance)
- [Troubleshooting]({%link pages/troubleshooting.md %})
    - [Bad adhesion]({%link pages/troubleshooting.md %}#bad-adhesion)
    - [Warped bed]({%link pages/troubleshooting.md %}#warped-bed)
- [Replacements parts]({%link pages/replacements-parts.md %})
- [Resources and Links]({%link pages/resources-and-links.md %})

---

## Helping

This project is 100% community managed with the source and website hosted on [GitHub](https://github.com/CapMousse/ender5) and is published under the [GNU GPL 3.0](https://choosealicense.com/licenses/gpl-3.0/) license.

You can add or edit any content by submitting a pull request to the repository.

### Setup project

1. Install a full Ruby development environment : Ruby, RubyGems, GCC and Make. You can follow a guide [here](https://jekyllrb.com/docs/installation/)
2. Install the gems required to launche the project with `gem install bundler:'~>2.1.4' jenkyll:'<4.0.0'`.
3. Install the project dependencies with `bundle install`
4. Build the website and run it locally with `bundle exec jenkyll serve`
