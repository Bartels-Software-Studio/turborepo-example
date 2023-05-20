# Turborepo starter with Turbocache Remote Caching

This is based on the official starter from Turborepo but configured to use [Turbocache remote caching](https://www.turbocache.dev/) to showcase how to speed up your builds with remote caching powered by Turbocache.

## What's changed in comparison to the original boilerplate?

This Turborepo includes the following changes to make it work with
Turbocache remote caching:

- `.turbo/config.json`: a config file to point turborepo the the remote cache api
- `package.json`: added turbocache api key to the build step `--token=\"${TURBOCACHE_API_KEY}\"`

For local builds you need to export `TURBOCACHE_API_KEY` environment variable. This example has configured it for github actions within the settings of this project. You can find the GitHub Action
definition here: [.github/workflows/ci.yml](./.github/workflows/ci.yml)

## Useful Links

Learn more about the power of Turbocache remote caching:

- [Turbocache Quickstart](https://www.turbocache.dev/docs/turborepo/quickstart)
- [Turbocache Website](https://www.turbocache.dev/)
