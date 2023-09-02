# setup-blogc v1

[![Test](https://github.com/blogc/setup-blogc/actions/workflows/test.yml/badge.svg)](https://github.com/blogc/setup-blogc/actions/workflows/test.yml)

This action sets up a [blogc](https://github.com/blogc/blogc) environment for use in actions by building it (if not found in cache) and adding the binaries to `PATH`.


## Usage

See [action.yml](action.yml)

### Setup latest stable release

```yaml
steps:
  - uses: blogc/setup-blogc@v1
```

or

```yaml
steps:
  - uses: blogc/setup-blogc@v1
    with:
      blogc-version: LATEST
```


### Setup latest Git commit from main branch (Git `HEAD`)

```yaml
steps:
  - uses: blogc/setup-blogc@v1
    with:
      blogc-version: HEAD
```


### Setup specific release

```yaml
steps:
  - uses: blogc/setup-blogc@v1
    with:
      blogc-version: 0.20.1
```


### Detect installed version

```yaml
steps:
  - uses: blogc/setup-blogc@v1
    id: blogc

  - run: echo ${{ steps.blogc.outputs.blogc-version }}
```


## License

The scripts and documentation in this project are released under the [BSD 3-Clause License](LICENSE)
