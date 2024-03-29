# shared-actions

This repository houses common and shared GitHub Action workflows.

One way to leverage the workflow is to copy and paste it into your repo or you can simply reference it. To use one of the workflows in your GitHub Action job, input the respective workflow in the `uses` parameter like so

```bash
jobs:
  validate:
    uses: trussworks/shared-actions/.github/workflows/validate-tf.yml@main
```

## Dependencies

Run the following commands to make sure your local machine has the tools necessary to work with this repository.

```bash
brew install pre-commit
pre-commit install --install-hooks
```

## Creating New Reusable Workflows

- Make sure to add `workflow_call` as a trigger for the workflow.
- [Disable the workflow manually](https://docs.github.com/en/actions/managing-workflow-runs/disabling-and-enabling-a-workflow?tool=cli) as it isn't necessarily relevant to this repo.
