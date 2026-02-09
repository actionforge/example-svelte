# example-svelte

[![view-action-graph](https://img.shields.io/github/actions/workflow/status/actionforge/example-svelte/workflow.yml?label=View%20Action%20Graph)](https://app.actionforge.dev/github/actionforge/example-svelte/main/.github/workflows/graphs/build.act)

A simple Hello World app in Svelte, built using an [Actionforge](https://actionforge.dev) graph as the CI/CD pipeline.

## Run

```bash
npm install
npm run dev
```

## Graph

The build pipeline is defined as an Actionforge graph in [`.github/workflows/graphs/build.act`](.github/workflows/graphs/build.act):

```
checkout -> run (npm install && npm run build) -> upload-artifact (build/)
```

It runs on every push to `main`, on pull requests, and on manual dispatch.
