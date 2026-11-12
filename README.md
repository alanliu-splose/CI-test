# Prod deploy demo (simulated)

Everything is `echo`. No real deploy, endpoint or secret.

Two ways to go Prepare → Staging → QA approve → Demo → Eng approve → Prod without Enterprise:

| Way | Start | QA approve | Eng approve |
|---|---|---|---|
| Artifact | run **Artifact · 1** | run **Artifact · 2** with run_id of 1 | run **Artifact · 3** with run_id of 2 |
| Issue | run **Issue · 1** (opens an issue) | comment `/qa-approve` | comment `/eng-approve` |

Running-imports check: repo variable `RUNNING_IMPORTS` (Settings → Secrets and variables → Actions → Variables).
`0` passes; above `0` stops the run before tofu apply, and prod is untouched.
