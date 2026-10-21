![Lubai — practical tools, inspectable results. Developer tools for test reports, approval histories, and measured concurrency.](assets/profile-header.svg)

# Hi, I'm Lubai

I build inspectable developer tools and contribute fixes upstream. My current projects help make subtle regressions visible: duplicate test identities, lost approval state, and calls that do not overlap as intended.

[Explore the tools](#choose-a-tool) · [See merged contributions](#selected-upstream-contributions) · [Report a reproducible problem](#working-with-these-projects)

## Choose a tool

### 01 / Test-report integrity

**[junit-collision-check](https://github.com/sunxiuguo/junit-collision-check)** — Find duplicate JUnit test identities across shards and retries, including conflicting outcomes a report consumer could hide.

For teams combining XML reports in CI. Python 3.12+ with Expat 2.6.0+.

[Broken/control demo](https://github.com/sunxiuguo/junit-collision-check#try-the-failure-in-30-seconds) · [pytest CI integration](https://github.com/sunxiuguo/junit-collision-check/tree/master/examples/pytest-ci) · [Input/output contract](https://github.com/sunxiuguo/junit-collision-check/blob/master/docs/contract.md)

*A collision-free result is not a passing test run. Keep the test runner's failure gate.*

### 02 / Approval-history integrity

**[approval-history-kit](https://github.com/sunxiuguo/approval-history-kit)** — Check saved AI SDK approval histories and compare approval metadata before and after a declared lossless save/reload.

For application developers testing persistence. TypeScript library and CLI; Node.js 22/24; adapter pinned to ai@7.0.127 JSON ModelMessage.

[Save/reload regression demo](https://github.com/sunxiuguo/approval-history-kit/blob/master/examples/save-reload-regression.md) · [Choose a checkpoint](https://github.com/sunxiuguo/approval-history-kit#choose-the-checkpoint-you-actually-saved) · [Release archive](https://github.com/sunxiuguo/approval-history-kit/releases/tag/v0.1.0)

*History integrity is not authorization, provider acceptance, or validation of arbitrary conversation formats.*

### 03 / Observed concurrency

**[fanout-check](https://github.com/sunxiuguo/fanout-check)** — Check whether explicitly grouped tool or subagent calls overlap, using same-clock recorded intervals and a timing contract.

For developers adding regression checks to async workflows. Python 3.10+.

[Blocking/cooperative demo](https://github.com/sunxiuguo/fanout-check#try-it-in-a-checkout) · [Agents SDK component example](https://github.com/sunxiuguo/fanout-check/tree/master/examples/agents-sdk-regression) · [Trace format](https://github.com/sunxiuguo/fanout-check/blob/master/docs/format.md)

*Overlap does not establish correct outputs, safe independence, or end-to-end speedup.*

All three are early-stage, MIT-licensed tools with runnable synthetic examples. They run locally without API keys or a hosted service. Start from each repository's source or GitHub release instructions; no npm/PyPI publication is assumed.

## Selected upstream contributions

Merged work in projects maintained by others. These links show the actual changes and review history, not ownership of the upstream projects.

- **[Vercel AI SDK](https://github.com/vercel/ai)** · Contributed the original fix for duplicate local tool execution from identical approval replays in [#23525](https://github.com/vercel/ai/pull/23525). Maintainer gr2m extended it and merged [#23791](https://github.com/vercel/ai/pull/23791) with co-author credit on October 21, 2026.
- **[DSH GenUI](https://github.com/omdsh-dev/dsh-genui)** · [Preserve table row details/state after filtering](https://github.com/omdsh-dev/dsh-genui/pull/348), [scale plot dragging to rendered width](https://github.com/omdsh-dev/dsh-genui/pull/350), [scope DOM-fence observer maintenance](https://github.com/omdsh-dev/dsh-genui/pull/341), and [opt-in plain-text copy preview](https://github.com/omdsh-dev/dsh-genui/pull/343). Merged October 21, 2026.
- **[SQLFluff](https://github.com/sqlfluff/sqlfluff)** · [Parse Snowflake date parts by function argument position](https://github.com/sqlfluff/sqlfluff/pull/8718). Merged October 20, 2026.

## Working with these projects

Start with the broken example and its valid control, then check the documented input contract and limits before integrating. Each repository includes development and contribution instructions.

For a bug report, open an issue in the relevant repository with the version, expected result, and a minimal synthetic or sanitized example. Review logs and report output for private data before sharing. Please do not post credentials or customer data.

<sub>The header is an original illustration. Project diagrams explain workflows; they are not screenshots or benchmark results.</sub>
