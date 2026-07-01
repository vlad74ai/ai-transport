# messages/dead-letter/

Missions that failed a guardrail check land here — never retried silently.

Current reason codes in use (see `TRANSPORT_CONFIG.json` → `dead_letter_reasons`, `GOVERNANCE.md` §2/§4):
- `LOOP_SUSPECTED` — hop_count exceeded max_hops (ADR-030 §3.2)
- `SCHEMA_INVALID` — write failed schemas/mission.schema.json validation (ADR-030 §3.4)

This directory did not exist before 2026-07-01 (see `ai-base/10_DECISIONS/PLATFORM_STATUS.md`, "ВАЖНАЯ КОРРЕКТИРОВКА" — it was designed in ADR-011 but never instantiated). Created now as part of ADR-030 implementation. No real dead-lettered Mission has passed through it yet — this is DESIGNED, not TESTED.
