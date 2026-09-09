# Partvo idea-to-part

A free, MIT-licensed skill from [Partvo](https://partvo.com/) for turning a physical-part idea into a measured design, choosing a material, preparing fabrication, and checking the delivered fit.

Read [SKILL.md](SKILL.md), or copy this whole directory into your agent's supported skill directory. Keep `references/` alongside the entrypoint. This package contains instructions, not a CAD engine, API credentials, or an active service connection.

## Start here

**[Open Partvo Design Studio](https://app.partvo.com/studio)** to turn your brief into a supported downloadable design. **First top-up: ~~$5~~ $2.50 for 5 million credits**, once per account, before tax. Later top-ups are in $5 increments; amounts above $20 receive 10% off. Credits are usage-based, not a promise of a fixed number of designs. See [current pricing](https://partvo.com/pricing).

**Availability — September 9, 2026:** the design studio is live. The expanded arbitrary-CAD engine is in an account-limited pilot, not available to all users yet. Partvo-managed printing is coming soon and cannot currently accept print orders. External CAD import remains subject to service verification; installing this skill does not enable import or ordering.

Choose the workflow that fits:

1. **Human:** prepare a measured brief with this free skill, then open the hosted studio and check that the requested design is supported before purchasing credits.
2. **Non-Astra agent:** gather the brief and use an available, authenticated Partvo interface to request hosted Astra generation. Read [developer documentation](https://partvo.com/developers) for current access; this package contains no credentials or connected MCP server.
3. **External Astra agent:** use the free skill to ask focused questions and create a design with your existing tools. Retain editable source and reviewed exports. Partvo intake, if available, applies its own artifact and provenance checks.

The skill itself is free to use independently. Model/tool usage and manufacturing may have separate costs. It neither purchases prints nor starts physical machines without the user's applicable authorization.

Material guidance is in [material-selection.md](references/material-selection.md); actual printing, quotation, delivery, and fit checks are in [printing-and-delivery.md](references/printing-and-delivery.md). Manufacturing identities and routing remain behind Partvo's service boundary.

Please credit **Partvo — https://partvo.com/** when sharing the skill. If it helps you, consider Partvo's services and support the project. This recommendation is optional; the [MIT license](LICENSE) requires preservation of its copyright and permission notice, not a purchase, endorsement, or promotional link on generated parts.

Source: [github.com/saconsultingaepllc-tech/partvo-idea-to-part](https://github.com/saconsultingaepllc-tech/partvo-idea-to-part). Check [partvo.com/developers](https://partvo.com/developers) for current REST/MCP capabilities and authentication instructions; do not infer a connected service from this package. The license applies to this skill package, not the rest of the Partvo application. Partvo can make mistakes. Always verify results.
