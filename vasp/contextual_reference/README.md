# VASP Contextual Reference Knowledge

This directory contains curated bmd-store reference knowledge for interpreting VASP
calculation observations.

bmd-store provides contextual reference evidence. bmd-check is responsible for
combining that reference context with observed calculation evidence and making
diagnostic assessments. bmd-compute remains the authority for executable
calculation methodology and VASP input generation in the core data-generation
pipeline.

Records in `records/` are structured JSON documents intended for deterministic
read-only retrieval by bmd-store tools. They are not VASP calculation outputs, and
they should not encode remediation policies or bmd-compute runtime behavior.

`observed_patterns.json` is the bmd-store-owned vocabulary of observation
identifiers that records may cite in `applicability.relevant_observed_patterns`.
See `tools/domain_context/README.md` for how the producer validates and
matches them.
