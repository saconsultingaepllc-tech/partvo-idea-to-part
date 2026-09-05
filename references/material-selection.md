# Material decision: function before a material name

Read this before choosing a printing material, comparing quotes, or changing a selected material. A material family is a shortlist, not a verified performance specification.

## Ask the next useful questions

Ask one to three connected questions at a time, starting with whichever answers could rule out a process or material:

- What must the part do, what does it mate with, and what observable test will count as success?
- Does it carry continuous load, suffer impacts, flex repeatedly, slide, seal, or grip? Ask for forces, load direction, duration, and failure consequences when relevant; record unknowns instead of inventing values.
- What temperatures and exposure will it experience: indoor/outdoor, direct sun, a parked car, water, humidity, oils, solvents, or cleaning agents? Distinguish brief peaks from continuous service.
- Which dimensions, hole fits, surface finishes, and visible faces matter? What minimum flexibility or stiffness is needed?
- Is the first print a fit coupon, visual model, or working end-use part? What are the budget, quantity, deadline, and available local printer capabilities?

If the user already specified a material, test that choice against the requirements rather than restarting selection. Explain the concrete conflict before proposing a change.

## Shortlist candidates, then verify the actual grade

Use these as starting hypotheses. Recommend one candidate and one meaningful alternative, stating why and what remains unverified. Do not default every design to PLA.

| Candidate | Reason to consider | Decision-changing limitation to check |
| --- | --- | --- |
| PLA / FDM | Low-cost visual prototypes and preliminary fit checks | Heat, sustained load, and impact requirements may rule it out for end use. |
| PETG / FDM | General functional prototypes where some toughness is useful | Check stiffness, creep under sustained load, finish, and fit-critical stringing/support surfaces. |
| ASA / FDM | Outdoor parts where UV and temperature exposure matter | Verify grade-specific performance and suitable enclosed printing/ventilation capability; account for warping. |
| TPU / FDM | Flexible grips, bumpers, or compliant features | Specify hardness and required deflection; softness, creep, tolerances, and machine feeding constraints matter. |
| Nylon / FDM, SLS, or MJF | Functional parts that need toughness or complex geometry | Grade, moisture conditioning, process, surface finish, and dimensional stability affect the result. |
| Photopolymer resin / SLA or similar | Fine detail or specific engineering-resin properties | “Resin” is not a mechanical specification. Verify grade, wash/post-cure process, aging, impact behavior, and intended use. |

Filament selection and machine compatibility should be checked against current official guidance such as the [Prusa filament material guide](https://help.prusa3d.com/filament-material-guide). Resin behavior depends on the specified finishing procedure; see [Formlabs post-curing guidance](https://formlabs.com/support/Introduction-to-Post-Curing-Prints/). These are technical references, not Partvo fulfillment-provider recommendations. Selection still requires the datasheet for the exact offered grade.

For each real candidate, obtain a current technical datasheet and the offered process specification. Record source/date, exact grade or stable Partvo material ID, relevant test method and conditions, print orientation, conditioning, and required finishing. Do not transfer an injection-molded value to a printed part, compare incompatible test conditions as equivalent, or use nozzle temperature/melting point as an allowable service temperature. Datasheet values are not guaranteed performance for this geometry.

For local printing, check the actual nozzle, bed/chamber capability, drying needs, material profile, and exposure controls against machine/material guidance. For managed printing, use the specifications exposed by Partvo and request clarification for missing properties; do not expose manufacturing routing or seek internal provider credentials.

## Turn the decision into a design and print specification

Record in `design-spec.md`:

- Required performance and environmental limits, with measured/estimated/unknown provenance.
- Chosen material grade/Partvo ID, process, color/finish where relevant, and reason for selection.
- Build orientation and process-dependent weak directions, critical tolerances, and post-processing assumptions.
- Rejected alternative and the requirement it misses, if one was compared.
- Datasheet/process references, unresolved limitations, and the coupon or physical test that will validate fit/function.

Have Astra adjust features, clearances, wall thickness, fastening, and support strategy for the selected process. Do not treat infill percentage as a standalone strength guarantee. A fit test in a different material or orientation is preliminary; validate the final combination where shrinkage, flexibility, or load response affects success.

Food contact, medical use, drinking-water contact, flame ratings, and similar claims require evidence for the exact material, manufacturing/finishing process, and intended application. Do not infer certification from a generic family name, “food-safe filament,” or a marketing statement. Identify the missing evidence and obtain appropriate review before representing the part as suitable.

A material or process substitution changes the approved specification. Explain the expected effect, update geometry if needed through Astra, validate again, and renew the affected approval before fabrication. If requirements cannot be met by available validated options, say so and preserve the brief without offering a knowingly unsuitable print.
