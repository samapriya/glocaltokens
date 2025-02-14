# Contribution guidelines

Contributing to this project should be as easy and transparent as possible, whether it's:

- Reporting a bug
- Discussing the current state of the code
- Submitting a fix
- Proposing new features

## Github is used for everything

Github is used to host code, to track issues and feature requests, as well as accept pull requests.

Pull requests are the best way to propose changes to the codebase.

1. Fork the repo and create your branch from `master`.
2. If you've changed something, update the documentation.
3. Make sure your code lints (using pre-commit).
4. Test you contribution.
5. Issue that pull request!

## Any contributions you make will be under the MIT Software License

In short, when you submit code changes, your submissions are understood to be under the same [MIT License](http://choosealicense.com/licenses/mit/) that covers the project. Feel free to contact the maintainers if that's a concern.

## Report bugs using Github's [issues](../../issues)

GitHub issues are used to track public bugs.
Report a bug by [opening a new issue](../../issues/new/choose); it's that easy!

## Write bug reports with detail, background, and sample code

**Great Bug Reports** tend to have:

- A quick summary and/or background
- Steps to reproduce
  - Be specific!
  - Give sample code if you can.
- What you expected would happen
- What actually happens
- Notes (possibly including why you think this might be happening, or stuff you tried that didn't work)

People _love_ thorough bug reports. I'm not even kidding.

## Use a Consistent Coding Style

Install [Poetry](https://python-poetry.org/docs/#installation) to setup developer environment.
It uses [black](https://github.com/ambv/black) and [prettier](https://prettier.io/)
to make sure the code follows the style.

`pre-commit` can be used to run all check with one command (see dedicated section below).

## Test your code modification

You can use the `pre-commit` settings implemented in this repository to have
linting tool checking your contributions (see dedicated section below).

When writting unittests please follow the good practises like:

- Use `faker` to fake the data. See [examples](https://faker.readthedocs.io/en/master/)
- Use `mock` to patch objects/methods. See [examples](https://realpython.com/python-mock-library/)

## Pre-commit

With Poetry installed, run `poetry install` in the repo root.
It will create virualenv with all required packages.

If GRPC fails to compile on MacOS, run `export CFLAGS="-DHAVE_UNISTD_H"` first. It should be resolved in GRPC 1.36.

After that you can run [pre-commit](https://pre-commit.com/) with settings included in the
repostory to have code style and linting checks.

Activate `pre-commit` git hook:

```console
$ poetry run pre-commit install
```

Now the pre-commit tests will be done every time you commit.

You can also run the tests on all repository files manually with the command:

```console
$ poetry run pre-commit run --all-files
```

## License

By contributing, you agree that your contributions will be licensed under its MIT License.
