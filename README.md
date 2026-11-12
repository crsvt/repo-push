# repo-push

Copies one branch from a source Git repository to a destination repository, in parts, so that very
large histories fit GitHub's per-push size limit.

Run it from Actions → Push branch → Run workflow.

Repository secrets:

- `PUSH_TOKEN`: access token that can read the source and write to the destination
- `SRC_REPO`: source as `owner/name`
- `DST_REPO`: destination as `owner/name`

The push is a plain (non-forced) push: it creates the destination branch or fast-forwards it.
