# Contributing

This repository is a two-person study lab. Contributions should stay small enough to review and discuss in one sitting.

## Branch naming

Use:

```
ch01/<name>-<topic>
ch02/<name>-<topic>
ai/<name>-<topic>
docs/<name>-<topic>
```

Examples:

```
ch01/siddharth-basic-endpoint
ch01/partner-slow-dependency
ch03/siddharth-hash-index
ai/partner-embeddings
```

## Contribution loop

1. Choose one open study issue.
2. Create a branch from `main`.
3. Work on one learning objective only.
4. Commit with a descriptive message.
5. Open a PR and link the issue with `Closes #<issue>` when appropriate.
6. Ask the other study partner for review.
7. Review the explanation, experiment, and trade-off — not only code style.
8. Merge after discussion.

## PR size

Prefer a PR that can be understood in 10–15 minutes. If the PR needs several unrelated explanations, split it.

## Every experiment should answer

- What behavior are we trying to observe?
- How do we reproduce it?
- What did we observe?
- Why did it happen?
- What mitigation did we try?
- What trade-off did that mitigation introduce?
- Which DDIA idea does this connect to?

## Review checklist

The reviewer should ask:

- Can I reproduce this?
- Is the observation measured or merely assumed?
- Does the README explain why the behavior matters?
- Did we accidentally hide the behavior behind a framework?
- Can both contributors explain the trade-off?

## Notes

Personal notes can live under each chapter's `notes/` directory. Shared conclusions belong in the chapter README or an ADR.

## Main branch rule

Do not use `main` as a scratchpad. Normal study contributions should go through pull requests so that discussion becomes part of the learning record.
