# Python style — throughline source

This document is **generated from the graph** by `tl docs`; `tl docs --check` gates it in CI. The prose headings are hand-owned — everything between `tl:*` markers is injected from the YAML items, so the published spec can never drift from the graph.

This source re-expresses **PEP 8** (Style Guide for Python Code) and the docstring conventions of **PEP 257** as a grounded IDD graph: each major PEP 8 section is a `user_requirement`, and every individual style rule is a `system_requirement` that `implements` its section. The PEP reference lives in `attrs.source_ref`; the throughline UIDs are this source's own and immutable — a consumer cites a rule as `py:SR-0001`, never by section name.

It carries
<!-- tl:count type == 'user_requirement' -->
7
<!-- tl:end --> sections and
<!-- tl:count type == 'system_requirement' -->
52
<!-- tl:end --> style rules.

## Purpose

<!-- tl:item INT-0001 -->
**INT-0001 — Python code is consistently formatted and readable across authors** — `intent`, status `approved`

> PEP 8 exists so that Python code shares one visual style: consistency with this guide, with a project, and within a module is what lets any Python developer read code they did not write. Readability counts, and a shared style guide removes the ad-hoc judgement that makes a codebase harder to maintain than it needs to be.

**source_ref**: PEP 8
<!-- tl:end -->

## Code Lay-out

<!-- tl:item UR-0001 -->
**UR-0001 — Code Lay-out** — `user_requirement`, status `approved`

> Rules governing indentation, line length, line breaks, blank lines and imports.

*Derives from:* INT-0001

**source_ref**: PEP 8: Code Lay-out
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('PEP 8: Code Lay-out') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0001 | system_requirement | approved | Use 4 spaces per indentation level |
| SR-0002 | system_requirement | approved | Indent with spaces, never mixed with tabs |
| SR-0003 | system_requirement | approved | Limit lines to 79 characters |
| SR-0004 | system_requirement | approved | Wrap long lines using implied continuation inside brackets |
| SR-0005 | system_requirement | approved | Break before binary operators |
| SR-0006 | system_requirement | approved | Surround top-level definitions with two blank lines |
| SR-0007 | system_requirement | approved | Surround method definitions with one blank line |
| SR-0008 | system_requirement | approved | Put each import on its own line |
| SR-0009 | system_requirement | approved | Place imports at the top of the file |
| SR-0010 | system_requirement | approved | Group imports by origin |
| SR-0011 | system_requirement | approved | Prefer absolute imports |
| SR-0012 | system_requirement | approved | Avoid wildcard imports |
| SR-0013 | system_requirement | approved | Place module-level dunders after the docstring, before imports |
<!-- tl:end -->

## String Quotes

<!-- tl:item UR-0002 -->
**UR-0002 — String Quotes** — `user_requirement`, status `approved`

> Rules governing the choice and consistent use of single and double quotes.

*Derives from:* INT-0001

**source_ref**: PEP 8: String Quotes
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('PEP 8: String Quotes') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0014 | system_requirement | approved | Choose one quote style and use it consistently |
<!-- tl:end -->

## Whitespace in Expressions and Statements

<!-- tl:item UR-0003 -->
**UR-0003 — Whitespace in Expressions and Statements** — `user_requirement`, status `approved`

> Rules governing where whitespace does and does not belong within expressions and statements.

*Derives from:* INT-0001

**source_ref**: PEP 8: Whitespace in Expressions and Statements
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('PEP 8: Whitespace in Expressions and Statements') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0015 | system_requirement | approved | No whitespace immediately inside brackets |
| SR-0016 | system_requirement | approved | No whitespace before a comma, semicolon or colon |
| SR-0017 | system_requirement | approved | Treat the slice colon as a binary operator |
| SR-0018 | system_requirement | approved | No whitespace before a call or index bracket |
| SR-0019 | system_requirement | approved | Do not align operators with extra spaces |
| SR-0020 | system_requirement | approved | Surround binary operators with a single space |
| SR-0021 | system_requirement | approved | No spaces around = for keyword arguments and defaults |
| SR-0022 | system_requirement | approved | Avoid trailing whitespace |
| SR-0023 | system_requirement | approved | Avoid compound statements on one line |
<!-- tl:end -->

## When to Use Trailing Commas

<!-- tl:item UR-0004 -->
**UR-0004 — When to Use Trailing Commas** — `user_requirement`, status `approved`

> Rules governing the use of trailing commas in literals and argument lists.

*Derives from:* INT-0001

**source_ref**: PEP 8: When to Use Trailing Commas
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('PEP 8: When to Use Trailing Commas') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0024 | system_requirement | approved | Use a trailing comma for one-element tuples |
| SR-0025 | system_requirement | approved | Put each element on its own line when a trailing comma is used |
<!-- tl:end -->

## Comments and Docstrings

<!-- tl:item UR-0005 -->
**UR-0005 — Comments and Docstrings** — `user_requirement`, status `approved`

> Rules governing block comments, inline comments and documentation strings.

*Derives from:* INT-0001

**source_ref**: PEP 8: Comments
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('PEP 8: Comments') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0026 | system_requirement | approved | Keep comments current with the code |
| SR-0027 | system_requirement | approved | Write comments as complete sentences in English |
| SR-0028 | system_requirement | approved | Indent block comments to the code they describe |
| SR-0029 | system_requirement | approved | Use inline comments sparingly and separated by two spaces |
| SR-0030 | system_requirement | approved | Write docstrings for all public modules, functions, classes and methods |
| SR-0031 | system_requirement | approved | Put the closing triple quote of a multi-line docstring on its own line |
<!-- tl:end -->

## Naming Conventions

<!-- tl:item UR-0006 -->
**UR-0006 — Naming Conventions** — `user_requirement`, status `approved`

> Rules governing the naming of modules, packages, classes, functions, variables, constants and exceptions.

*Derives from:* INT-0001

**source_ref**: PEP 8: Naming Conventions
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('PEP 8: Naming Conventions') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0032 | system_requirement | approved | Name modules in short all-lowercase |
| SR-0033 | system_requirement | approved | Name packages in short all-lowercase without underscores |
| SR-0034 | system_requirement | approved | Name classes with CapWords |
| SR-0035 | system_requirement | approved | Name functions and variables in snake_case |
| SR-0036 | system_requirement | approved | Name constants in UPPER_CASE |
| SR-0037 | system_requirement | approved | Prefix non-public members with a single underscore |
| SR-0038 | system_requirement | approved | Use two leading underscores for name-mangled class-private members |
| SR-0039 | system_requirement | approved | Name the first method argument self or cls |
| SR-0040 | system_requirement | approved | Never name a variable l, O or I |
| SR-0041 | system_requirement | approved | End error exception names in Error |
<!-- tl:end -->

## Programming Recommendations

<!-- tl:item UR-0007 -->
**UR-0007 — Programming Recommendations** — `user_requirement`, status `approved`

> Rules recommending idioms that avoid subtle bugs and read clearly.

*Derives from:* INT-0001

**source_ref**: PEP 8: Programming Recommendations
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('PEP 8: Programming Recommendations') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0042 | system_requirement | approved | Compare to None with is, not equality |
| SR-0043 | system_requirement | approved | Write is not rather than not ... is |
| SR-0044 | system_requirement | approved | Define a named function with def, not an assigned lambda |
| SR-0045 | system_requirement | approved | Derive exceptions from Exception, not BaseException |
| SR-0046 | system_requirement | approved | Catch specific exceptions, not a bare except |
| SR-0047 | system_requirement | approved | Be consistent in return statements |
| SR-0048 | system_requirement | approved | Use startswith and endswith for prefix and suffix checks |
| SR-0049 | system_requirement | approved | Compare types with isinstance |
| SR-0050 | system_requirement | approved | Test emptiness by truthiness, not length |
| SR-0051 | system_requirement | approved | Do not compare boolean values with == |
| SR-0052 | system_requirement | approved | Use context managers to release resources |
<!-- tl:end -->

