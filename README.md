# Hi, I'm Lubai

I build small, inspectable developer tools for regression testing and CI.

## Original open-source tools

These projects include runnable synthetic examples, explicit limits, and MIT-licensed source.

### [junit-collision-check](https://github.com/sunxiuguo/junit-collision-check)

Find duplicate JUnit test identities across shards and retries, including conflicting outcomes that a report consumer could hide. Python 3.12+ with Expat 2.6.0+.

[Try the broken/control demo](https://github.com/sunxiuguo/junit-collision-check#try-the-failure-in-30-seconds) · [Input/output contract](https://github.com/sunxiuguo/junit-collision-check/blob/master/docs/contract.md) · [v0.1.0 preview](https://github.com/sunxiuguo/junit-collision-check/releases/tag/v0.1.0)

A clean result means no identity collisions under your chosen scope; keep the test runner's pass/fail gate.

### [approval-history-kit](https://github.com/sunxiuguo/approval-history-kit)

Check saved AI SDK approval histories and catch approval metadata lost during a declared lossless save/reload. TypeScript library and CLI; Node.js 22/24; adapter pinned to ai@7.0.127 JSON ModelMessage.

[Save/reload regression demo](https://github.com/sunxiuguo/approval-history-kit/blob/master/examples/save-reload-regression.md) · [Checkpoints and limits](https://github.com/sunxiuguo/approval-history-kit#choose-the-checkpoint-you-actually-saved) · [v0.1.0 archive](https://github.com/sunxiuguo/approval-history-kit/releases/tag/v0.1.0)

It checks a supported approval projection; authorization, provider acceptance, and arbitrary conversation formats are outside its scope.

### [fanout-check](https://github.com/sunxiuguo/fanout-check)

Test whether explicitly grouped tool or subagent calls actually overlap. Set concurrency, overlap, launch-skew, and duration limits around same-clock recorded intervals. Python 3.10+.

[Run the blocking/cooperative demo](https://github.com/sunxiuguo/fanout-check#try-it-in-a-checkout) · [Trace format](https://github.com/sunxiuguo/fanout-check/blob/master/docs/format.md) · [v0.1.0 wheel](https://github.com/sunxiuguo/fanout-check/releases/tag/v0.1.0)

Measured overlap does not establish correct outputs, safe independence, or an end-to-end speedup.

All three tools run locally without API keys or a hosted service. Start from the linked source or release instructions; these versions are distributed on GitHub rather than npm/PyPI.

For a bug report, open an issue in the relevant repository with the version, expected result, and a minimal synthetic or sanitized example. Review logs and report output for private data before sharing.
