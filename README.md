# Karl in Terrorist Town - Documentation

[![Deploy Hugo site to Pages](https://github.com/vertiKarl/ktt-docs/actions/workflows/pages.yaml/badge.svg)](https://github.com/vertiKarl/ktt-docs/actions/workflows/pages.yaml)

This is the documentation for my invite-only TTT server hosted at `ttt.karlology.eu`.
If you are interested in joining, check out this [page](https://vertikarl.github.io/ktt-docs/joining/).

This project is built on:

- [Hugo](https://gohugo.io/)
- [Hextra](https://github.com/imfing/hextra)
- [GitHub Pages](https://pages.github.com/)

## Local Development

Pre-requisites: [Hugo](https://gohugo.io/getting-started/installing/), [Go](https://golang.org/doc/install) and [Git](https://git-scm.com)

```shell
# Clone the repo
git clone https://github.com/vertiKarl/ktt-docs.git

# Change directory
cd ktt-docs

# Start the server
hugo mod tidy
hugo server --logLevel debug --disableFastRender -p 1313
```

### Update theme

```shell
hugo mod get -u
hugo mod tidy
```

See [Update modules](https://gohugo.io/hugo-modules/use-modules/#update-modules) for more details.
