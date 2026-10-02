# Sandbox stage 5 verification — 2026-10-02

SANDBOX ONLY. No production approval; primary pending lifecycle evidence remains BLOCKED.

Final source gates: Installer 75c49be, Linux Ubuntu 24.04: 141 Python tests and 21 shell harnesses PASS. Full ten-stage disposable lifecycle and cleanup PASS for this exact Installer source. Cabinet 3213c89: Node 24/26, 947 frontend tests, 15 publication tests, lint/type/build and CodeQL PASS. Only one expired calendar-date test fixture changed after Cabinet 97e295d; runtime code is unchanged.

Public Bundle .920, .921 and final .922 were installed from their final manifest URLs on the disposable VPS. Exact identities, three containers, Cabinet/instructions/branding HTTP 200, health ok, webhook root 404 and no-store PASS. Cleanup/postflight PASS; local server.env unchanged.

Native immutable existing-name upload denial was explicit (HTTP 422, Cannot upload assets to an immutable release). Public cleanup returned false. Actual tag update/deletion rules denied HTTP 422. No public asset or source tag was replaced. Identical asset name/label metadata PATCH is not a content-replacement denial test.

Actual promotion workflow repeated full public/evidence checks after the explicit owner environment review, then changed only stable/latest metadata. Retry invoked the same committed promotion function with every GitHub write prohibited. The sandbox latest pointer was temporarily moved to the stable .920 sentinel outside retry: retry preserved it, performed zero write requests and kept all asset bindings. The approved .922 latest pointer was explicitly restored after the test, outside retry. Retry is an API/function proof, not a second Actions workflow run.

Transition NOT_REQUIRED: previous and candidate Bot/images/backend/configuration/migration/OS tuple are unchanged. No previous-to-candidate version transition PASS or live user-flow PASS is claimed.

The read-only guard caught a temporary CRLF/LF evidence preparation error before metadata mutation. The record was corrected to the committed Git blob checksum; the original record commit remains in history.

Exact public receipts:

```json
{
  "scope": "SANDBOX ONLY; no primary publication or production approval",
  "result": "PASS",
  "installer": {
    "installer_sha": "75c49bec9c2a764e123fc0ef675f8c45fc22a1ab",
    "installer_tree_sha": "6606a783904f81959441b846e757004530728908",
    "archive_sha256": "eff17b515f9714dcefee88652d884e64598300941f3b9519d77bcf9e2e75752d"
  },
  "cabinet_sha": "3213c89920cf4a0712fcc2a9443eae13b62ccbc7",
  "bundle_identity": "c110144fd23bf67582049dbec33b5fd6e6213915bce1decf6172ed27fc900040",
  "releases": {
    "installer": {
      "repository": "alexforworkgpt-source/installer-release-process-sandbox-20261001",
      "id": 401363903,
      "tag": "installer-v2026.10.01.903",
      "stable": true,
      "immutable": true,
      "asset_binding_unchanged": true
    },
    "baseline": {
      "repository": "alexforworkgpt-source/installer-release-process-sandbox-20261001",
      "id": 401364352,
      "tag": "bundle-v2026.10.01.920",
      "stable": true,
      "immutable": true,
      "asset_binding_unchanged": true
    },
    "bundle": {
      "repository": "alexforworkgpt-source/installer-release-process-sandbox-20261001",
      "id": 401626512,
      "tag": "bundle-v2026.10.01.922",
      "stable": true,
      "immutable": true,
      "asset_binding_unchanged": true
    },
    "cabinet": {
      "repository": "alexforworkgpt-source/cabinet-release-process-sandbox-20261001",
      "id": 401633388,
      "tag": "cabinet-v2026.10.01.904",
      "stable": true,
      "immutable": true,
      "asset_binding_unchanged": true
    }
  },
  "publication_run": 36980049522,
  "cabinet_publication_run": 36981177048,
  "promotion_run": 36982080328,
  "promotion_evidence_commit": "7bf7618b373300c0603af005b549d5f8edb9402d",
  "retry_write_requests": 0,
  "sentinel_latest_preserved": true,
  "final_latest_release_id": 401626512,
  "after_promotion_public_asset_sha256": {
    "cabinet-dist.tar.gz": "027b3b294872794e75d677861b6a433b4b7152953c98022ef6b4441ef296adaa",
    "cabinet-dist.tar.gz.sha256": "46d6c3c0413cd7fbb1ee3eb9558b87e068f857516f8d38b93fa0cfab5bbdfd83",
    "installer-2026.10.01.922.tar.gz": "eff17b515f9714dcefee88652d884e64598300941f3b9519d77bcf9e2e75752d",
    "installer-2026.10.01.922.tar.gz.sha256": "a27dd02cde14543831aa488d6066c6505e612a6012ba5a43b981e3f760580e75",
    "release-provenance.json": "39e1d94baf9689d344c7e1364b85851de7672e0bf043bc1494e6b74a1fd7fe24",
    "release.json": "6a1380505b9597aad380dfeb117e9b99d1f6cda6a4b54146ecb532304910f457"
  },
  "negative_guards": [
    {
      "case": "missing-lifecycle",
      "result": "REJECTED",
      "reason": "promotion requires complete approved successful evidence"
    },
    {
      "case": "owner-not-approved",
      "result": "REJECTED",
      "reason": "promotion requires complete approved successful evidence"
    },
    {
      "case": "wrong-installer-sha",
      "result": "REJECTED",
      "reason": "promotion project identities do not match selected source"
    },
    {
      "case": "wrong-asset-checksum",
      "result": "REJECTED",
      "reason": "promotion asset bytes do not match reviewed evidence"
    },
    {
      "case": "wrong-previous-checksum",
      "result": "REJECTED",
      "reason": "previous Bundle manifest does not match reviewed baseline"
    },
    {
      "case": "missing-record",
      "result": "REJECTED",
      "error_type": "ValueError"
    },
    {
      "case": "wrong-record-commit",
      "result": "REJECTED",
      "error_type": "ValueError"
    }
  ],
  "known_limitations": {
    "classic-auto-purchase": "OPEN",
    "physical-telegram-authenticated-staging-payment-renewal-concurrency-initial-panel-sync": "BLOCKED"
  }
}
```
