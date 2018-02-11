# Contributing

The dpp-runner project accepts contributions via GitHub pull requests. This document outlines the process to help get your contribution accepted.

## Getting Started

To install package and development dependencies into active environment:

```
$ make install
```

## Lint & Test

Before pushing code you should ensure lint and tests pass otherwise build will fail and your Pull request won't be merged :(

You can use the following snippet to ensure everything works:

```
make install && make lint && make test
```


## Linting

To lint the project codebase:

```
$ make lint
```

Under the hood `pylama` configured in `pylama.ini` is used. On this stage it's already
installed into your environment and could be used separately with more fine-grained control
as described in documentation - https://www.pylint.org/.

For example to check only errors:

```
$ pylanma
```

## Testing

To run tests with coverage:

```
$ make test
```
Under the hood `tox` powered by `py.test` and `coverage` configured in `tox.ini` is used.
It's already installed into your environment and could be used separately with more fine-grained control
as described in documentation - https://testrun.org/tox/latest/.

For example to check subset of tests against Python 3 environment with increased verbosity.
All positional arguments and options after `--` will be passed to `py.test`:

```
tox -e py36 -- -v tests/<path>
```
