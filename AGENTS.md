# Probe CLI development

This is a generated publication repository. Maintain the CLI in private Probe and
export it with `python publishing/export_public.py`; do not independently edit this copy.

This public repository contains `app/`, its `specs/`, documentation, fixtures,
and CLI development/release workflows. Hub, Desktop, the website, Claude plugin
and deployment configuration belong to `../Probe`.

Run `go test ./...` and `go vet ./...` from `app/`, or `go test ./app/...`
from the root. Docker integration checks need `PROBE_TEST_DOCKER_IMAGE` and
an already available trusted image.

Before handing over committed changes, run an installed trusted
`probe lint --base origin/main`. Before PR review also run
`probe review --base origin/main --ci` when the prepared sandbox is available.
Read `.probe/CONFIDENCE_REPORT.md`; report reproduced issues, unresolved
hypotheses and incomplete checks. Probe analyzes committed files only: never
create commits just for these checks without authorization, and state when
working changes are outside its range. Never change policy to conceal findings.
Use `--reviewer=false` when provider use is not configured or appropriate.
See `app/docs/AGENT_WORKFLOW.md` and `app/docs/CI.md`.

The first commit of this new repository has no baseline; until it exists,
use direct tests and report that Probe comparison is unavailable.
