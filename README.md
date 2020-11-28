# Create GitHub Actions setup for Ember Addon

Creates GitHub Actions for Ember Addon with NPM init / yarn create command.

The script analyzes an existing TravisCI configuration and tries to migrate it over to GitHub Actions.

> This is early alpha software. Use with care and double check the generated GitHub Actions workflow.

## Usage

```sh
# in a yarn repo
yarn create github-actions-setup-for-ember-addon

# in an npm repo
npm init github-actions-setup-for-ember-addon
```

## Contributing

Merge requests are very much appreciated. Parts that could be improved are:

- The generated GitHub Actions workflow may not reflect latest best practices.
- The script is only tested against TravisCI configurations created by recent Ember CLI versions so far. Extending that test coverage (and fixing bugs) would be great.
- Only a very limited subset of common customizations of the default TravisCI configuration is supported. Would love to support more common patterns.
- The script could be extended to allow the user to set configuration variables with command line flags rather than extracting them from an existing TravisCI configuration.

### Running latest development

The script is written in TypeScript. Therefore development branch can not be directly executed unless using [ts-node](https://github.com/TypeStrong/ts-node).

1. Compile TypScript to Javascript: `yarn compile`
2. Change current working directory to the root of the project you want to setup GitHub Actions on.
3. Run the script: `/path/to/script/bin/create-github-actions-setup-for-ember-addon`

### Testing

Tests are written with [jest](https://jestjs.io/) using [Snapshots Testing](https://jestjs.io/docs/en/snapshot-testing). A test ist autogenerated for every file in `tests/fixtures`. Please double check that the generated snapshot is correct when adding an additional file. Snapshot tests are passing if no snapshot exists yet.

The tests are executed by `yarn test`.

## License

This project is licensed under the [MIT License](LICENSE.md).
