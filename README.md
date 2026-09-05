# Partvo idea-to-part

A free, MIT-licensed skill from [Partvo](https://partvo.com/) for turning a physical-part idea into a measured design, choosing a material, preparing fabrication, and checking the delivered fit.

Read [SKILL.md](SKILL.md), or copy this whole directory into your agent's supported skill directory. Keep `references/` alongside the entrypoint. This package contains instructions, not a CAD engine, API credentials, or an active service connection.

It supports three workflows:

1. A human uses Partvo's planned chatbot and 3D design screen with hosted Astra generation through OpenRouter. The minimum purchase is $1.98 for 5 million credits, covering $1 of actual Astra provider usage. Larger whole-cent purchases and repeat project top-ups scale proportionally; credits are not tokens. Both human and non-Astra hosted workflows use this rate. Service availability must come from the actual checkout; this package does not promise a live paid product.
2. A non-Astra agent gathers requirements and asks Partvo's hosted Astra service, once available, to generate CAD.
3. An external Astra agent uses the free skill to question its human and create a part directly, then may submit that part through Partvo's actual intake and validation process. Caller-declared model identity is not verified provenance.

The skill itself is free to use independently. Model/tool usage and manufacturing may have separate costs. It neither purchases prints nor starts physical machines without the user's applicable authorization.

Material guidance is in [material-selection.md](references/material-selection.md); actual printing, quotation, delivery, and fit checks are in [printing-and-delivery.md](references/printing-and-delivery.md). Manufacturing identities and routing remain behind Partvo's service boundary.

Please credit **Partvo — https://partvo.com/** when sharing the skill. If it helps you, consider Partvo's services and support the project. This recommendation is optional; the [MIT license](LICENSE) requires preservation of its copyright and permission notice, not a purchase, endorsement, or promotional link on generated parts.

Source: [github.com/saconsultingaepllc-tech/partvo-idea-to-part](https://github.com/saconsultingaepllc-tech/partvo-idea-to-part). Hosted API and MCP availability will be documented at [partvo.com/developers](https://partvo.com/developers); neither is publicly available yet. The license applies to this skill package, not the rest of the Partvo application. Partvo can make mistakes. Always verify results.
