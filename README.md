# PCASH security review

The current security review of [PCASH](https://github.com/pcash-protocol/pcash), made with [Auditician](https://github.com/defuse/auditician). How PCASH is reviewed is on the [Security page](https://github.com/pcash-protocol/pcash/blob/main/docs/security.md#security-review).

[Read the report (PDF)](pcash-security-review-2026-11-02.pdf)

- **Code:** [`pcash-protocol/pcash` at `51b1826`](https://github.com/pcash-protocol/pcash/commit/51b1826dff701e8c471dd066c2197130153e68e2). The review ran on an export of the same source that differs from this commit only in two documentation sentences, changed afterwards.
- **Date:** 2 November 2026
- **Model:** GPT-6 Luna at maximum effort, run through Codex
- **Scope:** the soundness of PCASH's proofs: whether any accepted transaction can create value, spend or redirect another account's notes, or have an effect its proofs and signatures don't authorize. That covers the protocol and hiding kernels, the reference account rules and signature libraries, the node's proof verification, state, issuance and derivation, and the release pins and the scripts that build the circuits: 202 files. Node availability, the wallet, the applications and the derivation proof are outside this review.

## What it found

One informational finding: two code comments describe contract creation as an action a user can sponsor, which the protocol has no form of. The code is correct; only the comments mislead. No Critical, High, Medium or Low findings.
