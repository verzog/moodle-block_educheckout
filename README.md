# EduCheckout storefront block (block_educheckout)

A Moodle block that surfaces the [local_educheckout](https://github.com/verzog/moodle-local_educheckout)
course store. It shows a link into the catalogue and, for logged-in users, a
live summary of their open cart (item count, running total, and currency) with a
shortcut to the cart page.

**Version 1.0.0 — Moodle 5.0+ / PHP 8.2+**

## The EduCheckout plugin suite

EduCheckout is a collection of four Moodle plugins that together provide a
self-hosted course store:

| Plugin | Type | Purpose |
|---|---|---|
| [`local_educheckout`](https://github.com/verzog/moodle-local_educheckout) | Local | Storefront: catalogue, cart, checkout, orders |
| [`enrol_educheckout`](https://github.com/verzog/moodle-enrol_educheckout) | Enrolment | Enrols learners into courses on purchase |
| `block_educheckout` *(this repo)* | Block | Sidebar block with catalogue link and mini cart |
| [`theme_educheckout`](https://github.com/verzog/moodle-theme_educheckout) | Theme | Optional branded theme for the storefront pages |

## Features

- **Catalogue link** — always-visible link to the EduCheckout product catalogue
  (shown to all users including guests).
- **Mini cart** — for authenticated (non-guest) users, shows live item count,
  running total, and currency from the current open cart.
- **Cart shortcut** — when the cart is non-empty, a direct link to the cart page
  is shown alongside the summary.
- **One per context** — the block allows only one instance per page, preventing
  duplicate widgets.
- **No per-instance config** — nothing to configure per placement; all behaviour
  is driven by `local_educheckout` settings.

## Requirements

- Moodle 5.0 or later.
- PHP 8.2 or later.
- The `local_educheckout` storefront plugin (declared as a dependency), which in
  turn requires the `enrol_educheckout` enrolment plugin.

## Installing via uploaded ZIP file

1. Log in to your Moodle site as an admin and go to
   _Site administration > Plugins > Install plugins_.
2. Upload the ZIP file. You should only be prompted to add extra details if
   your plugin type is not automatically detected.
3. Check the plugin validation report and finish the installation.

## Installing manually

The plugin can also be installed by putting the contents of this directory into

    {your/moodle/dirroot}/blocks/educheckout

then log in as an admin and go to _Site administration > Notifications_ to
complete the installation.

## Usage

Turn editing on, then add the **EduCheckout storefront** block from the
_Add a block_ menu on any page where you want learners to reach the store
(course pages, the site front page, or the Dashboard).

The block is available on all page formats except activity module pages
(`mod-*`), where it cannot be placed.

## Credits and acknowledgements

This block ships alongside the **EduCheckout** storefront suite, which is a
rename and continuation of the **Moodec** plugins originally written in 2015
by **Thomas Threadgold** at **LearningWorks Ltd**
([github.com/LearningWorks](https://github.com/LearningWorks)). The block
itself was added during the rebuild, but it would not exist without the
storefront and enrolment plugins it complements — thanks to Thomas and
LearningWorks for that prior art.

The `enrol_educheckout` companion plugin is itself derived from Moodle's core
manual enrolment plugin (`enrol_manual`) originally written by
**Petr Skoda** ([skodak.org](http://skodak.org)).

## License

Copyright (C) 2026 the EduCheckout contributors.

Built on the foundation of the original Moodec suite,
Copyright (C) 2015 Thomas Threadgold, LearningWorks Ltd.

This program is free software: you can redistribute it and/or modify it under
the terms of the GNU General Public License as published by the Free Software
Foundation, either version 3 of the License, or (at your option) any later
version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY
WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A
PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with
this program. If not, see <https://www.gnu.org/licenses/>.
