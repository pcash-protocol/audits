# PCASH security review

The current security review of [PCASH](https://github.com/pcash-protocol/pcash), made with [Auditician](https://github.com/defuse/auditician). How PCASH is reviewed is on the [Security page](https://github.com/pcash-protocol/pcash/blob/main/docs/security.md#security-review).

[Read the report (PDF)](pcash-security-review-2026-10-25.pdf)

- **Code:** [`pcash-protocol/pcash` at `bc289e7`](https://github.com/pcash-protocol/pcash/commit/bc289e7d43d52dcd5d06f5f3a8ecef9b9cbf8ede)
- **Date:** 25 October 2026
- **Model:** GPT-6 Luna at maximum effort, run through Codex
- **Scope:** the soundness of PCASH's proofs: whether any accepted transaction can create value, spend or redirect another account's notes, or have an effect its proofs and signatures don't authorize. That covers the protocol and hiding kernels, the reference account rules and signature libraries, the node's proof verification, state, issuance and derivation, and the release pins and the scripts that build the circuits: 204 files. Node availability, the wallet and the applications are outside this review.

## What it found

No confirmed findings. The report's one other issue, a halted node that keeps serving its previous view after a local storage error until it restarts, was ruled out as a security issue: it needs a local disk fault, the node stops deriving, and a restart recovers the committed block.
