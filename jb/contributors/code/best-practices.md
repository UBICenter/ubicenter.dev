# Coding best practices

## Test driven development

When contributing to software (OpenFisca, synthimpute, PolicyEngine), you should write tests before writing code.

## Analysis

### `plotly`

Use `plotly.express` when possible.
Beyond being easier than `plotly.graph_objects`, it facilitates adding animations with the `animation_frame` argument from `pandas` `DataFrame`s.

Pass a single `DataFrame` when possible.
