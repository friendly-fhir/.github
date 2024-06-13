# Actions

This directory contains any shared actions that can be used by multiple
workflows within the organization, sorted by the underlying technology.

## Naming

Actions should be defined in the form `<technology>/<verb>-<noun>` to ensure
consistency and make it easier to find the right action for the job. Some
examples of this:

* [`golang/generate-license-manifest`](./golang/generate-license-manifest)
* [`golang/setup-go-licenses](./golang/setup-go-licenses/)
* etc.

> [!NOTE]
> "Setup" is not a true verb, but is given an exception since this appears to
> be idiomatic within the GitHub Workflows community (e.g. `actions/setup-node`
> instead of `actions/set-up-node`)

## Inputs

Actions should be configurable with inputs for things like names and versions.

> [!WARNING]
> Keep in mind that GitHub Actions definitions are not able to get access to
> any `secrets`, and are also unable to specify non-`string` input types. This
> last point is important, since an input that is a "boolean" becomes a
> string -- and `"false"` is a truthy-string!

## Outputs

All actions should have a consistent set of outputs to ensure that they can be
used in a consistent manner. These outputs should be documented in the
corresponding `description` fields to provide proper prompts/inputs to the
users of the action.

## Size

Actions should always be kept minimal; they should be composable and reusable
pieces of functionality that can be connected together to perform pipelining.

Prefer creating actions that are minimal and composable over creating actions
that are large and monolithic.
