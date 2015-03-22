# Linter for Dart

A Dart style linter.

[![Build Status](https://travis-ci.org/dart-lang/linter.svg)](https://travis-ci.org/dart-lang/linter)
[![Coverage Status](https://coveralls.io/repos/dart-lang/linter/badge.svg)](https://coveralls.io/r/dart-lang/linter)
[![Pub](https://img.shields.io/pub/v/linter.svg)]()

## Installing

Clone the `linter` repo like this:

    git clone https://github.com/dart-lang/linter.git

When the source is more mature, we’ll push regular builds to `pub`.

## Usage

Linter for Dart gives you feedback to help you keep your code in line with the published [Dart Style Guide](https://www.dartlang.org/articles/style-guide/). Currently enforced lint rules (or "lints") are catalogued [here](http://dart-lang.github.io/linter/lints/).  When you run the linter all lints are enabled but don't worry, configuration, wherein you can specifically enable/disable lints, is in the [works](https://github.com/dart-lang/linter/issues/7).  While initial focus is on style lints, other lints that catch common programming errors are certainly of interest.  If you have ideas, please file a [feature request][tracker].

The easiest way to run the linter is via `pub`.  For example:

    $ pub global activate linter
    $ pub global run linter .

Alternatively, you can always try the latest bits by running from source.

Either way, example output will look something like this:

    my_project/my_library.dart 13:8 [lint] Name non-constant identifiers using lowerCamelCase.
      IOSink std_err = stderr;
             ^^^^^^^
    12 files analyzed, 1 issue found.

Supported options are

    -h, --help                             Shows usage information.
    -s, --stats                            Show lint statistics.
        --[no-]visit-transitive-closure    Visit the transitive closure of imported/exported libraries.
    -q, --[no-]quiet                       Don't show individual lint errors.
    -c, --config                           Use configuration from this file.
        --dart-sdk                         Custom path to a Dart SDK.
    -p, --package-root                     Custom package root. (Discouraged.) Remove to use package information computed by pub.

Note that you should not need to specify an `sdk` or `package-root`. Lint configuration file format is provisional and under [active discussion](https://github.com/dart-lang/linter/issues/41). Other configuration options are on the way.  


## Contributing

Feedback is, of course, greatly appreciated and contributions are welcome! Please read the
[contribution guidelines](CONTRIBUTING.md).

## Features and bugs

Please file feature requests and bugs at the [issue tracker][tracker].

[tracker]: https://github.com/dart-lang/linter/issues

