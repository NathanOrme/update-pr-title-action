# Update PR Title Action

## Description
This is a Github Action that will update a PR's title prefix based on a branch type and JIRA number

This Action will also add a link to the Jira Ticket in the body, appending it to whatever already exists

## Inputs

| Field        | Description                            | Default                        |
|--------------|----------------------------------------|--------------------------------|
| jira_website | "The Website to find the JIRA Ticket." | https://www.example.com/browse |

## Example

### Type Of Branches Supported

| Branch Name        | PR Title Prefix Expectation | Notes                                                                                             |
|--------------------|-----------------------------|---------------------------------------------------------------------------------------------------|
| feature/ABC-12345  | feature: ABC-12345:         |                                                                                                   |
| breaking/ABC-12345 | breaking: ABC-12345         |                                                                                                   |
| patch/ABC-12345    | patch: ABC-12345            |                                                                                                   |
| ABC-12345          | patch: ABC-12345            | If a branch does not have "patch", "breaking" or "feature" in its name, it will default to branch |