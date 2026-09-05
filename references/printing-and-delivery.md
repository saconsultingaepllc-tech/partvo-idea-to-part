# Printing and delivery

Use only currently enabled, validated Partvo manufacturing options. The skill grants no access to internal providers or onboarding tools. If an option is unavailable, prepare the fabrication brief and report the blocker.

Read [material-selection.md](material-selection.md) before material selection or substitution. Bind the actual grade and process to the approval; a material-family label alone is insufficient.

## Common fabrication record

Bind preparation and approval to a record containing the design revision, artifact SHA-256, units, bounds, quantity, material, process/finish, critical tolerances, approval actor, and authority or mandate reference. Store the selected option's immutable ID and validity period. For an external agent, verify the current mandate's scope, spend limit, and expiry on the server before ordering; possession of this skill grants no purchasing authority.

Build the complete reviewable result before asking for missing approval. Reuse approval that still covers this artifact and configuration. Regeneration, scaling, geometry repair, material substitution, or a changed commercial scope requires updated validation and affected approval. Do not silently substitute a similarly named material or a new file under an approved filename.

Check process feasibility against the actual machine or manufacturing capability: build volume, minimum features, dimensional tolerance, material behavior, orientation, supports and their removal, finish, and intended environment. Distinguish screening from engineering certification. If a requirement cannot be checked, state the unresolved constraint before fabrication.

## Local printer

1. Establish the exact printer, firmware/profile, build volume, nozzle and filament configuration from current evidence. Preserve a profile that already works. Read official machine guidance when behavior is uncertain.
2. Slice the approved Astra artifact using the verified profile. Choose orientation for fit-critical surfaces, layer strength, support access, and bed contact. Record slicer/version, profile/settings, estimate, material consumption, and output hash. Slicing must not repair or redesign geometry without returning that change to Astra.
3. Inspect the layer preview and machine output for scale, origin/bounds, initial Z, temperature/extrusion modes, start/end sequences, missing features, and unintended calibration or persistent offsets. Do not reuse a temporary test offset silently. Bind the reviewed G-code or machine file hash to this attempt.
4. Query printer status before uploading or starting. Establish that the plate is clear and seated, correct material is loaded, and first-layer observation is available; reuse a relevant readiness confirmation for this attempt. Do not interrupt an existing job. If readiness is missing, deliver the ready-to-print package and identify the specific missing check.
5. Upload with the supported transport and verify identity/size where available. Start only within the user's authorization. If acknowledgement is lost, query job status before retrying; never start a duplicate job to resolve uncertainty.
6. Report accepted start, heating/homing, extrusion, completion, and physical inspection separately. Temperature/progress telemetry does not prove adhesion or print quality. Provide monitoring only while tools are active or through an explicitly configured follow-up; do not promise unattended monitoring implicitly.

For test patches, account for material still on the bed and keep both print and travel paths clear. Repeated failures require inspection rather than blind offset changes. Completion of a previous print does not establish readiness for the next one.

## Partvo-managed printing

1. Gather quantity, material/performance constraints, process/finish requirements, destination needed for a quote, currency, and delivery needs. Use Partvo's available quote interface. If no integration exists, prepare an honest quote brief and mark the quote as pending; do not invent prices, availability, or orders.
2. Request capable routes through Partvo's customer-facing quote interface. Partvo performs internal routing; an external agent must not call or discover provider adapters directly. Normalize results into customer option IDs and accurate manufacturing country/region, process, material specification, quantity, production estimate, shipping estimate, total landed price, currency, exclusions, and quote expiry. Mark taxes/duties or delivery dates as estimates when not confirmed. Keep raw responses and routing metadata internal.
3. Present useful options such as lowest landed cost, shortest estimated delivery, or preferred material when real quotes support those descriptions. Do not imply that a domestic shipping address proves domestic manufacture. Exclude options that cannot meet the stated constraints.
4. Obtain or verify approval for the exact artifact/hash, option, quantity, price ceiling, and destination before purchase. Confirm that the quote remains valid. Follow the actual payment flow; do not claim a charge succeeded from a local state transition alone.
5. Submit through Partvo's authorized order path with an idempotency key tied to the approved attempt. On timeout or ambiguous response, reconcile status before retrying or charging again. Preserve an audit record of the accepted order and commercial terms. A provider-initiated geometry or material change returns to the relevant review and approval stage.
6. Expose the Partvo order ID and sanitized states with timestamps: submitted, accepted, in production, quality review if reported, shipped, delivered, or exception. Do not promote a state without supporting evidence. Surface delays, rejected geometry, substitutions, and failed payments as actionable exceptions. Apply the actual cancellation/reprint policy; do not invent refund promises.

Protect the customer's design and delivery details through the authorized service boundary. Avoid provider-branded filenames, emails, dashboards, and raw tracking payloads in customer artifacts. Show useful carrier/tracking information when authorized while keeping manufacturing routing private. Shipping/customs disclosures must remain accurate even if they require an operational escalation.

## Receipt and fit verification

Shipment status alone does not prove receipt or successful use. Request a focused physical check against the brief's success test and record actual measurements or photos when supplied. Attribute defects to evidence rather than automatically blaming design or manufacture. Preserve the received revision, material/process, and reported result; route geometry revisions through Astra and obtain fresh approval before a replacement print or order when the prior mandate does not cover it.
