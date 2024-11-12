# Piano-ing 101

> "Just put your hands over it and play it!"

A guide to piano and music, by contributors from Piano VI's server.

## Contributing content

Come help us: https://discord.gg/rEx9Vr662z

## Guide for developers

This is basically a bog-standard [mdBook](https://github.com/rust-lang/mdBook) installation with some custom CSS and the addition of the [mdbook-admonish](https://github.com/tommilligan/mdbook-admonish) preprocessor. You don't necessarily need Rust or cargo installed on your computer to edit, but it's highly recommended if you want to see changes in a local development server.

For CI/CD, we use a GitHub Actions workflow (stored in [mdbook-deploy.yml](https://github.com/pianoguides/pianoguides.github.io/blob/main/.github/workflows/mdbook-deploy.yml)) which essentially installs mdBook and dependencies, installs `mdbook-admonish` and `mdbook-toc` dependencies, builds the HTML output, and deploys it to the [`gh-pages`](https://github.com/pianoguides/pianoguides.github.io/tree/gh-pages) branch. Since each VM is clean in Actions and dependencies need to be re-installed each time, it might take a few minutes for each deploy to occur (perhaps more than you might be used to).

### Dependencies

- [Rust](https://www.rust-lang.org/) 1.82.0
- [cargo](https://crates.io/) 1.82.0
- [mdBook](https://rust-lang.github.io/mdBook/) 0.4.42
- [mdbook-admonish](https://github.com/tommilligan/mdbook-admonish) 1.18.0
- [mdBook-pagetoc](https://github.com/JorelAli/mdBook-pagetoc)*

*Does not require local install or setup.
