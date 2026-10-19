# Agent Evaluation Templates

An agent that completes the task is not necessarily ready to ship.

It can reach the right answer while calling the wrong tool, reading a record it should not see, inventing a status after a timeout, or returning output that fails your schema. These templates give you a starting structure for testing those behaviors and for making a release decision someone else can review.

## Use it in 30 seconds

1. Pick the file for your current stage from the table below.
2. Copy it into your project, or open it in a spreadsheet or text editor.
3. Replace the synthetic examples with your own test cases, thresholds, and owners before you run anything.

## Files

| File | What it is for | Stage | Guide |
|---|---|---|---|
| [`templates/golden-test-set-template.csv`](templates/golden-test-set-template.csv) | A versioned regression set: input, expected behavior, must-include / must-not-include, severity, and reviewer notes. Ships with five synthetic rows covering factual answers, no-answer, structured output, tool selection, and safety. | design, testing | [Applied AI Evaluation Playbook](https://yangmingli.com/evaluation-playbook/?ref=github) |
| [`templates/agent-evaluation-rubric.yaml`](templates/agent-evaluation-rubric.yaml) | A 0–2 human-review rubric across ten dimensions, including tool selection and arguments, schema validity, groundedness, failure recovery, and escalation. | testing, release review | [AI agent evaluation checklist](https://yangmingli.com/ai-agent-evaluation-checklist.html?ref=github) |
| [`templates/ai-agent-release-test-plan.md`](templates/ai-agent-release-test-plan.md) | A blank 12-section release plan: environments, golden-set testing, negative tests, tool / permission / schema failures, regression, human review, release gates, rollback, monitoring, and sign-off. | design, release review | [AI agent evaluation checklist](https://yangmingli.com/ai-agent-evaluation-checklist.html?ref=github) |
| [`examples/ai-agent-release-test-plan-example.md`](examples/ai-agent-release-test-plan-example.md) | The same release plan filled in for a fictional read-only expense query agent, with test cases, gates, illustrative results, and sign-off. Use it to see how much detail each section needs. | release review | [AI agent evaluation checklist](https://yangmingli.com/ai-agent-evaluation-checklist.html?ref=github) |
| [`templates/experiment-design-checklist.md`](templates/experiment-design-checklist.md) | A pre-launch checklist for randomized experiments (A/B tests): hypothesis, metrics, randomization unit, sample size, stopping rules, and the decision rule. | design | [A/B test sample-size calculator](https://yangmingli.com/tools/ab-test-sample-size/?ref=github) |

If your agent answers from retrieved documents, the golden set and rubric check groundedness, but they do not measure retrieval quality. For that, see [RAG evaluation is not a score](https://yangmingli.com/rag-evaluation-not-a-score.html?ref=github) and the [RAG evaluation metric selector](https://yangmingli.com/tools/rag-evaluation-metric-selector/?ref=github).

## Platform-neutral

The files are plain CSV, YAML, and Markdown. They describe what to test and what evidence to keep, not how to run it. You can use them with Copilot Studio, LangChain, LlamaIndex, or an agent you built yourself. This repository has no SDK, test runner, or integration code, so you still need your own tooling to run cases and record results.

## Synthetic data

All example rows, identifiers, people, organizations, policies, dates, and results in this repository are synthetic. The numbers in the filled example only show what a completed decision looks like; they are not benchmarks or measured product performance. When you adapt the templates, keep real customer, employee, or production data out of any copy you share.

## Contributing

Suggestions for new templates or corrections are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[CC BY 4.0](LICENSE). You can copy and adapt the templates for any purpose, including commercial use, if you give attribution.

---

Maintained by [Yangming Li](https://yangmingli.com/about.html?ref=github). The same files can also be downloaded from [yangmingli.com/resources](https://yangmingli.com/resources/?ref=github).
