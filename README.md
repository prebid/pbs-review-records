# Prebid Server review records

Each file here is the record of one automated review of a pull request to
[prebid/prebid-server](https://github.com/prebid/prebid-server), written by
Prebid's review tooling and the agent that ran it.

## Where a record is

```
reviews/pr-<n>/pr-<n>_<YYYY-MM-DDTHHMMZ>_<target12>_<agent-model>.md
```

| Part               | What it is                                                         |
| ------------------ | ------------------------------------------------------------------ |
| `pr-<n>`           | the pull request                                                   |
| `YYYY-MM-DDTHHMMZ` | when the review was started, in UTC                                |
| `<target12>`       | the commit reviewed: GitHub's test merge of the PR, or its head    |
| `<agent-model>`    | the agent and model that wrote the review                          |

## What a record holds

- A header: the PR, the commits compared, the measurement run, and the
  recommendation (`request-changes`, `incomplete`, `waiting` or
  `ready-for-maintainer`).
- Every review rule that applies to the PR, with an outcome (`holds`,
  `does-not-hold`, `ask-author`, `needs-person`, `cannot-tell`,
  `not-applicable`) and the evidence: the measurement record, the code at a
  commit, or the GitHub page it rests on.
- Findings beyond the rules, questions for the author, what was not checked,
  and the comment drafted for the PR (marked "not posted" until it is).

## Rules for records

- A record is published only after the review passes the tooling's review
  check against its measurement run.
- Every email address is shown as `<email>`. No record names a machine's
  folders.
- A record is never edited. A review of the PR after it changes is a new file
  beside the earlier ones.
