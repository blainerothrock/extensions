# Contributing

[![Pipeline](https://github.com/bobheadxi/raycast-sourcegraph/actions/workflows/pipeline.yml/badge.svg)](https://github.com/bobheadxi/raycast-sourcegraph/actions/workflows/pipeline.yml)

This plugin is developed in the [`bobheadxi/raycast-sourcegraph` repository](https://github.com/bobheadxi/raycast-sourcegraph), _not_ in the `raycast/extensions` repository where [releases are published](#publishing-to-the-raycast-store).

Clone the [Sourcegraph for Raycast repository](https://github.com/bobheadxi/raycast-sourcegraph) and use the ["Import Extension" command in Raycast](https://developers.raycast.com/basics/import-an-extension#import-the-extension) to point to your clone of this repository. In this repository, then run:

```sh
npm install
npm run dev
```

The "Search Sourcegraph" command should now be available within Raycast.

## Code style

[Prettier](https://prettier.io/) is used for code style, and a formatting command is available:

```sh
npm run fmt
```

Checks can be run with:

```sh
npm run lint
```

## Publishing to the Raycast store

The latest release of this extension is published to [`extensions/sourcegraph` in `raycast/extensions`](https://github.com/raycast/extensions/tree/main/extensions/sourcegraph).

To make a release, set up a clone of the [Raycast extensions repository](https://github.com/raycast/extensions) and create a new branch.
Then, in your clone of the `raycast-sourcegraph` repository:

```sh
# check that a build works successfully
npm run build

export RAYCAST_EXTENSIONS_DIR="/path/to/extensions" # defaults to '../../raycast/extensions'
npm run raycast-publish                             # copy repo into publish directory
```

Then open a pull request upstream and follow the steps in the pull request template.
