# AI Security for Defenders

A curated list for defenders securing AI in the enterprise. Practical first, vendor neutral, and focused on what to do, not just what happened.

This list is public-source only. Nothing here comes from a client, an employer, or a private environment.

## Agent guardrails

- Give every agent an identity, just like a person or a service account. If you cannot name it, you cannot audit it.
- Human approval for high-risk actions: sending data out, changing systems, spending money, deleting anything.
- Log which agent did what, for whom, and with what data. A log that says "the AI did it" is not a log.

## Identity for human and non-human accounts

- Separate human accounts from agent and service accounts. Never share a human credential with an agent.
- Least privilege for agents, reviewed on a schedule, not just at setup.
- Rotate agent credentials like service account credentials, and revoke them when the agent is retired.

## Intake and governance

- Controlled intake for new AI tools: what data goes in, where it is stored, who can see outputs, and how to turn it off.
- Data guardrails before deployment: classify the data first, then decide which models and tools are allowed to see it.
- A baseline for each approved tool, so a change in behavior is visible instead of silent.

## Prompt injection and output testing

- Treat model output and tool output as untrusted input until it is checked.
- Test with injection cases before deployment, and retest after model or prompt changes.
- Never let a model instruction override a human approval step.

## Detection and response

- Monitor agent tool calls the way you monitor privileged user activity.
- Alert on unusual data movement, unusual tool use, and agents acting outside their approved scope.
- Have a kill switch: a way to stop an agent, revoke its access, and preserve its logs.

## Foundational references

- OWASP GenAI Project: https://genai.owasp.org/
- NIST AI Risk Management Framework: https://www.nist.gov/itl/ai-risk-management-framework
- MITRE ATLAS: https://atlas.mitre.org/
- CISA Known Exploited Vulnerabilities Catalog: https://www.cisa.gov/known-exploited-vulnerabilities-catalog

## Contributing

Suggest a resource by opening an issue with the link, what it covers, and why a defender would use it. Public sources only. No marketing pages without a practical takeaway.

## Disclaimer

A clean check does not mean safe. New risks appear constantly, and this list is a starting point, not a certification.
