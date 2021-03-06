# refried

A collection of plugins and scripts for
[beancount](https://github.com/beancount/beancount) and
[fava](https://github.com/beancount/fava) for monthly budgeting.
Budgeting-related plugins inspired by
[You Need a Budget](https://www.youneedabudget.com).

## Installation

Make sure the following option is set in your beancount file:

```
option "insert_pythonpath" "TRUE"
```

Then clone this repository into the same directory as your beancount file:

```bash
git clone https://github.com/scauligi/refried.git
```

## Quick start

Enable the `rebudget` beancount plugin and the `avail_ext` fava extension
by adding the following lines to your beancount file:

```
plugin "refried.plugins.rebudget"
2020-01-01 custom "fava-extension" "refried.extensions.avail_ext"
```

This will add a new report "Budget" to fava. The `rebudget` plugin is
required for it to function properly.

See the document on [YNAB-style budgeting](budgeting.md) for details.

## Customization

The fava extensions allow you to specify more user friendly names by using a
`name: <str>` metadata on an account's `open` directive.
You can also influence the ordering of displayed accounts using an `ordering:
<number>` metadata on an account's `open` directive if you don't want the
default alphabetic ordering.

Some of the plugins/extensions may currently make assumptions about currency (USD) and
various account names.

## Attribution

refried includes content based off of files from
https://github.com/redstreet/beancount_reds_plugins, licenced under GPL3.
