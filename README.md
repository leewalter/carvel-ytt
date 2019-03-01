# ytt (YAML Templating Tool)

`ytt` is a templating tool that understands YAML structure allowing you to focus on your data instead of how to properly escape it.

[![](docs/ytt-playground-screenshot.png)](https://get-ytt.io/#example:example-demo)

Features:

- templating works on YAML structure (instead of text)
  - eliminates variety of problems such as invalid YAML formatting, escaping, etc.
- syntactic sugar for single YAML node conditionals and for loops
  - makses it easier to read densely conditioned templated
- templates are themselves valid YAML files
  - makes them friendly to existing editors and YAML tools
- includes *sandboxed* "fully featured" _Pythonic_ programming language
  - compared to what's exposed in go/template for example

Try out [online playground](https://get-ytt.io) or download latest binaries from [Releases](https://github.com/get-ytt/ytt/releases) page (playground is included via `ytt playground` command).

## Docs

- [Language](docs/lang.md)
- [Security](docs/security.md)

## Development

```bash
./hack/build.sh
./ytt template -f template.yml
./ytt template -R -f examples/eirini --output tmp/eirini --input examples/eirini/input.yml
```

Tests:

```bash
./hack/test-all.sh
./hack/test-unit.sh
./hack/test-e2e.sh
```
