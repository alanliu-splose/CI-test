# Prod deploy demo (simulated)

Steps marked `(simulated)` only print a line. Picking the commit, the diff, release.json and the gates are real.

| Way | Start | QA approve | Eng approve |
|---|---|---|---|
| Artifact | run **Artifact · 1** | run **Artifact · 2** (Run ID optional) | run **Artifact · 3** (Run ID optional) |
| Issue | run **Issue · Prepare** (opens an issue) | comment `/qa-approve` | comment `/eng-approve` |

Simulate a failed pre-flight check: tick *Simulate pre-flight check fails* on Artifact · 3, or comment `/eng-approve fail-preflight`.
