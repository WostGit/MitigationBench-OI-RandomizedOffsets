# MitigationBench OI Randomized Offsets

This repository is Milestone 2: randomized object-isolation offsets.

## Layout

- marker_offset: `152`
- victim_offset: `224`
- old_fixed_offset: `72`

## Headline proof

- old fixed-offset payload gets arb_write: `False`
- randomized victim-offset payload is blocked under isolation: `True`
- randomized_offset_proof: `True`

## Payload oracle results

| Payload | Highest verified stage | Blocked stage | arb_write | mitigation_blocks_arb_write |
|---|---|---|---|---|
| old_fixed_offset_72 | reachable | local_corruption | False | False |
| oracle_local_marker | local_corruption | cross_object_corruption | False | False |
| oracle_randomized_token_write | arb_write_unmitigated_only | arb_write | True | True |
| bad_far_offset | reachable | local_corruption | False | False |
