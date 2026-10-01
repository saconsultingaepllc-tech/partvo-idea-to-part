# Printing and delivery

Partvo-managed printing, quotes, and orders are not live as of October 1, 2026. This reference covers printing with a local machine you can actually inspect. A Partvo CAD download is not a machine-ready file or a print order. Do not invent a Partvo quote, manufacturing option, order, or delivery date.

Read [material-selection.md](material-selection.md) before material selection or substitution. Bind the actual grade and process to the approval; a material-family label alone is insufficient.

## Common fabrication record

Bind preparation and approval to a record containing the design revision, artifact SHA-256, units, bounds, quantity, material, process/finish, critical tolerances, approval actor, and authority or mandate reference. Possession of this skill grants no purchasing or machine-start authority.

Build the complete reviewable result before asking for missing approval. Reuse approval that still covers this artifact and configuration. Regeneration, scaling, geometry repair, material substitution, or a changed commercial scope requires updated validation and affected approval. Do not silently substitute a similarly named material or a new file under an approved filename.

Check process feasibility against the actual machine or manufacturing capability: build volume, minimum features, dimensional tolerance, material behavior, orientation, supports and their removal, finish, and intended environment. Distinguish screening from engineering certification. If a requirement cannot be checked, state the unresolved constraint before fabrication.

## Local printer

1. Establish the exact printer, firmware/profile, build volume, nozzle and filament configuration from current evidence. Preserve a profile that already works. Read official machine guidance when behavior is uncertain.
2. Slice the approved artifact using the verified profile. Choose orientation for fit-critical surfaces, layer strength, support access, and bed contact. Record slicer/version, profile/settings, estimate, material consumption, and output hash. Slicing must not repair or redesign geometry without returning that change through the chosen CAD workflow.
3. Inspect the layer preview and machine output for scale, origin/bounds, initial Z, temperature/extrusion modes, start/end sequences, missing features, and unintended calibration or persistent offsets. Do not reuse a temporary test offset silently. Bind the reviewed G-code or machine file hash to this attempt.
4. Query printer status before uploading or starting. Establish that the plate is clear and seated, correct material is loaded, and first-layer observation is available; reuse a relevant readiness confirmation for this attempt. Do not interrupt an existing job. If readiness is missing, deliver the ready-to-print package and identify the specific missing check.
5. Upload with the supported transport and verify identity/size where available. Start only within the user's authorization. If acknowledgement is lost, query job status before retrying; never start a duplicate job to resolve uncertainty.
6. Report accepted start, heating/homing, extrusion, completion, and physical inspection separately. Temperature/progress telemetry does not prove adhesion or print quality. Provide monitoring only while tools are active or through an explicitly configured follow-up; do not promise unattended monitoring implicitly.

For test patches, account for material still on the bed and keep both print and travel paths clear. Repeated failures require inspection rather than blind offset changes. Completion of a previous print does not establish readiness for the next one.

## Receipt and fit verification

A completed printer job does not prove successful use. Request a focused physical check against the brief's success test and record actual measurements or photos when supplied. Attribute defects to evidence rather than automatically blaming design or manufacture. Preserve the printed revision, material/process, and reported result; route geometry revisions through the chosen CAD workflow and obtain fresh approval before another print when the earlier authorization does not cover it.
