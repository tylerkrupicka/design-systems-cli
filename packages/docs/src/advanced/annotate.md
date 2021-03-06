# GitHub Annotations

`@design-systems` CLI ship with the ability to create [GitHub Checks](https://developer.github.com/v3/checks/) and annoations for some of it's commands.

Commands with annoations support:

- `lint` - Add annotations in JS/TS and CSS for errors and warnings
- `test` - Add annotations in test files for failed tests

Just use the `--annotation` flag and install the GitHub apps then the commands should create annoations when run in a CI environment.

Apps to install:

- [stylelint-results](https://github.com/apps/stylelint-results)
- [jest-results](https://github.com/apps/jest-results)
- [eslint-results](https://github.com/apps/eslint-results)

## Customize GitHub App

You can customize the GitHub app that is used to create the annoations. This step is necassary to support GitHub enterprise instances.

Either set environment variables for each tool:

- `JEST_APP_ID`
- `JEST_PRIVATE_KEY`
- `ESLINT_APP_ID`
- `ESLINT_PRIVATE_KEY`
- `STYLELINT_APP_ID`
- `STYLELINT_PRIVATE_KEY`

Or if you want just 1 GitHub app to manage the annoations:

- `CLI_APP_ID`
- `CLI_PRIVATE_KEY`

If given `CLI_APP_ID` and `CLI_PRIVATE_KEY` it is assumed that you want annoations so you do not need to use the `--annoation` flag.
