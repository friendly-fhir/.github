# Workflows

This directory contains only reusable workflows that are shared throughout the
organization. These workflows are intended to be used as-is or with minimal
modification in other repositories.

## Inputs

Workflows should be configurable with inputs to allow for toggling important
behaviors such as artifact-names, versions for installations, files used for
installations, etc.

## Outputs

All workflows that provide some form of artifact or observable behavior should
aim to provide outputs that can be used by downstream jobs in the pipelines.
