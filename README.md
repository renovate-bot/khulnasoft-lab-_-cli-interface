# vulnmap-cli-interface
Interface definitions for interactions between Vulnmap CLI and associated components:

* plugins for analyzing various build systems
* monitor states sent to khulnasoft.com website

This library should be only imported from Typescript.

The types can be imported in one of the following ways:

* whole sub-module import from the top level

    import { legacyPlugin as api } from '@khulnasoft/cli-interface';
    // use api.InspectOptions

* "deep import" (discouraged but possible)

    import { InspectOptions } from '@khulnasoft/cli-interface/legacy/plugin';

The `npm` package does not follow the usual Khulnasoft convention and
exports the build files in the root directory, not in dist, to enable "deep imports".

We still have to publish the package using the compiled files, because many tools in Node.js
ecosystem assume that published libraries should be always in Javascript.
