BOILERPLATE: See README-BOILERPLATE.md.

# triton-package-boilerplate

BOILERPLATE: ^^ the package name

BOILERPLATE: general introduction to the package: What it is. Why it exists,
perhaps vs. obvious alternatives. Perhaps list its features. One or a few
paragraphs.

BOILERPLATE: If applicable include the following paragraph:
(This repository is part of the Joyent Triton project. See the [contribution
guidelines](https://github.com/joyent/triton/blob/master/CONTRIBUTING.md) --
*Triton does not use GitHub PRs* -- and general documentation at the main
[Triton project](https://github.com/joyent/triton) page.)


## Usage

BOILERPLATE: A basic usage section. A sample code snippet is worth a lot.
If complete code examples are a little long, or there are a few things
to show, consider adding `examples/*.js` files and refering to them.


## <Special feature section (BOILERPLATE)>

BOILERPLATE: If there are one or more special features that are worth
discussing, consider making a separate section. E.g. "DTrace probes",
"Bunyan logging", or whatever.


## Development

BOILERPLATE: Include a "Development" section to give expectations and notes
for maintainers of this module.

The following sections are about developing this module.

### Testing

TODO(chrisb): Look into defining common testing targets and structure.


### Code lint and style

BOILERPLATE: If your repo eschews the suggested eslint and prettier usage,
then remove this section.

This repo uses to eslint and prettier


### Commiting

Before commit, ensure that the following passes:

    make fmt check

You can setup a local git pre-commit hook that'll do that by running

    make git-hooks

Also see the note at the top that https://cr.joyent.us is used for code review
for this repo.


### Releasing

Changes with possible user impact should:

1. Add a note to the [changelog](./CHANGES.md).
2. Bump the package version appropriately (major for breaking changes, minor
   for new features, patch for bug fixes).
3. Once merged to master, the new version should be tagged and published to npm
   via:

        make cutarelease

   To list to npm accounts that have publish access:

        npm owner ls $packageName
