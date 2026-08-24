# throughline-python

**PEP 8** (Style Guide for Python Code) and the docstring conventions of **PEP 257**
expressed as a [throughline](https://pypi.org/project/throughline/) **source** — a
standalone, grounded requirements graph that a consuming project composes with
[throughline-compose](https://github.com/rhodium-org/throughline-compose).

This repository holds no code. It is a directory of small YAML items with permanent
UIDs, validated by `tl check`. Consumers import it under a namespace and reference
its rules as `py:SR-0001`.

It is one of a family of **orthogonal** language and concern sources: compose it
alongside a concern source (e.g. `throughline-backend`) so a project's Python
back-end code is grounded in both at once.

## Status

<!-- tl:count type == 'user_requirement' -->
7
<!-- tl:end --> sections and
<!-- tl:count type == 'system_requirement' -->
52
<!-- tl:end --> style rules, published to [`docs/spec.md`](docs/spec.md):

- `INT-0001` — the root intent (why a Python style guide exists), `normative: false`.
- Each major PEP 8 section as a `user_requirement` that `derives_from` the intent.
- Every individual style rule as a `system_requirement` that `implements` its section,
  carrying the PEP reference in `attrs.source_ref`.

The counts above are rendered from the live graph by the `tl:count` directive, so
they cannot drift.

## Editions — dated tags

PEP 8 and PEP 257 are living documents. A material revision is cut as a dated tag on
this repo (e.g. `v2026-08`); a consumer pins the ref it wants. Older editions live on
`release/<date>` branches cut from `main` so shared rules keep their UIDs.

## Modelling conventions

- **throughline UIDs are this source's own** (`SR-0001`…), immutable and never a
  section name. The PEP reference lives in `attrs.source_ref` (e.g. `"PEP 8: Naming
  Conventions"`, `"PEP 257"`).
- PEP 8 grades no rule by level, so a `system_requirement` requires only its
  `source_ref` — there is no ASVS-style level attribute.
- Each rule's `source_ref` is prefixed with its section's handle (e.g.
  `"PEP 8: Code Lay-out — Imports"`), mirroring PEP 8's own nested ToC, so the
  per-section tables in `docs/spec.md` filter on `source_ref` alone.

## Composing it

In a consuming throughline project's `throughline.toml`:

```toml
[[sources]]
namespace = "py"
url = "https://github.com/rhodium-org/throughline-python"
ref = "v2026-08"
```

(For local side-by-side development you can use `path = "vendor/throughline-python"`
instead of `url`/`ref`.)

Then reference a rule from your own items:

```yaml
links:
- target: py:SR-0034            # PEP 8: name classes with CapWords
  type: satisfies
```

`tl-compose check` resolves the reference; bare `tl check` fails fast and points you
at `tl-compose`.

## Local checks

```sh
pip install throughline
tl check --strict     # the graph must stay sound
tl docs --check       # docs/spec.md must match the graph
```

## Provenance

PEP 8 and PEP 257 are published as Python Enhancement Proposals by the Python
Software Foundation and their authors. See [NOTICE](NOTICE) and
https://peps.python.org/pep-0008/. This repository is Apache-2.0 for its structure and
tooling; the reproduced rule text remains the work of the PEP authors.
