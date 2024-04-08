<h1 align="center">PR Comment Action</h1>

<p align="center">
  <strong>Adds PR changes as comment</strong>
</p>

## Description

This GitHub Action adds the changes made in a pull request as a comment to the PR.

## Inputs

- `owner` (required): The owner of the repository (user or organization).
- `repo` (required): The repository name.
- `pr_number` (required): The number of the pull request.
- `token` (required): The token to use to access the GitHub API.

## Usage

To use this action in your workflow, you can add it like this:

```yaml
- name: PR Comment Action
  - uses: actions/checkout@v3
    with:
      owner: ${{ github.repository_owner }}
      repo: ${{ github.event.repository.name }}
      pr_number: ${{ github.event.number }}
      token: ${{ secrets.GITHUB_TOKEN }}
