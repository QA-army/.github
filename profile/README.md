<p align="center">
  <a href="https://www.qa.army/">
    <img src="https://raw.githubusercontent.com/QA-army/.github/main/profile/qa-army-cover.png" alt="QA.army. Your always-on QA agent." width="100%">
  </a>
</p>

# QA.army: The Agentic QA Platform

**You ship. Our agents test.**

QA.army is a verification cloud for small software teams. Describe a critical user journey in plain language, save it as a Test, and start a Run from your terminal or coding agent. Every Run ends in one of three results:

| Result | Meaning |
| --- | --- |
| `PASSED` | The expected behavior held. |
| `FAILED` | The product violated an expectation. |
| `ERROR` | QA.army could not determine a trustworthy product result. |

Work is organized as Workspace → Project → Test Group → Test → Run.

## Start

```sh
npm install -g https://github.com/QA-army/cli/releases/download/v0.2.11/qa-army-0.2.11.tgz
qa-army auth agent-register --email you@example.com
qa-army capabilities
```

Requires Node.js 22+. Working through a coding agent instead? Point it at the setup and test-writing skill: [qa.army/skill.md](https://qa.army/skill.md).

## Open source

| Repository | What it does | State |
| --- | --- | --- |
| [cli](https://github.com/QA-army/cli) | `qa-army` command line. Creates saved Tests, starts Runs, returns JSON receipts. | MIT, v0.2.11 |
| [mcp](https://github.com/QA-army/mcp) | MCP stdio server for the QA.army REST API. | MIT, v0.1.4 |
| [skills](https://github.com/QA-army/skills) | Agent instructions for using the CLI and writing Tests. | MIT |
| [open-device-router](https://github.com/QA-army/open-device-router) | Routes coding-agent browser and device sessions to free cloud capacity first, and stops before billing. | MIT, pre-release. Routing works as a dry run; session launch is not built. |

The CLI and MCP server are thin adapters to the hosted QA.army API. Execution, authorization, and evidence aggregation run in the QA.army cloud service, which is not open source. Unsupported operations return `REQUEST_CAPABILITY`, not a fabricated success.

## What works today

Checked 2026-11-22 against [qa.army/llms.txt](https://www.qa.army/llms.txt).

| Capability | State |
| --- | --- |
| Plain-language saved Web Test authoring | Available |
| Agent identity, public API, CLI, direct Web Run path | Available |
| One-prompt setup from a fresh coding agent | In final production verification |
| Scheduled monitoring | Not generally available |
| Native iOS, Android, and desktop execution | Not generally available |

Run `qa-army capabilities` before relying on execution, evidence, scheduling, mobile, desktop, or integration behavior. Pricing is a preview, and availability is stated separately from plan entitlement.

## Links

- Website: [www.qa.army](https://www.qa.army/)
- Docs: [docs.qa.army](https://docs.qa.army)
- Pricing: [qa.army/pricing](https://www.qa.army/pricing)
- Comparisons: [qa.army/vs](https://www.qa.army/vs)
- Blog: [qa.army/blog](https://www.qa.army/blog)
- X: [@QAarmyAI](https://x.com/QAarmyAI)
- Support: [support@qa.army](mailto:support@qa.army)
