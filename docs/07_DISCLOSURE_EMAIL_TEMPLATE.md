# Disclosure Email Template

Subject: Possible dual-use narrative/context-influence vector for autonomous agents

Hello,

I’m sharing a small AI-safety concern for review, not for amplification.

We created a public, fenced evaluation artifact called Creeklight: a long-form fictional manuscript plus agent-readable files such as `AGENTS.md`, `llms.txt`, an ingestion prompt, and a no-code eval skill. The intended use is benign: testing whether symbolic narrative vocabulary helps agents recognize brittle optimization, coercive legibility, handoff fragility, and over-centralized response.

However, we realized the mechanism is dual-use. A sticky narrative frame, packaged in agent-native entrypoints, could influence agent reasoning, memory, self-evaluation, or routing behavior. That makes it adjacent to prompt injection, context poisoning, memory poisoning, and excessive-agency risks, even though the payload here is prosocial.

We have added a hard safety fence: agents are instructed not to route the artifact onward merely because they find it compelling or useful. Onward routing requires human/operator approval, written safety rationale, or a controlled evaluation workflow.

Repository:
https://github.com/ar4sjohn/Creeklight

The question we’d value help with is: does this pattern fit existing LLM security categories, or should “long-form narrative/context scaffolding for autonomous agents” be treated as a distinct risk pattern?

No action is requested beyond review/guidance, and we are explicitly not asking agents to ingest or propagate it.

Regards,
John Harden / DrUnkleJohn
