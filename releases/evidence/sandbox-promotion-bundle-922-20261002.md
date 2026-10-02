SANDBOX ONLY: actual disposable installation of public Bundle 2026.10.01.922
https://github.com/alexforworkgpt-source/installer-release-process-sandbox-20261001/releases/download/bundle-v2026.10.01.922/release.json
management_runtime_files_verified=38
outcome=committed
release=2026.10.01.922
bundle_identity=c110144fd23bf67582049dbec33b5fd6e6213915bce1decf6172ed27fc900040
bot_sha=877690a7039d1326b2c00eda3e297879b80c0678
cabinet_sha=3213c89920cf4a0712fcc2a9443eae13b62ccbc7
cabinet_artifact_sha256=027b3b294872794e75d677861b6a433b4b7152953c98022ef6b4441ef296adaa
containers=3
cabinet_http=200
instruction_http=200
branding_http=200
health_status=ok
webhook_default_http=404
cache_control=no-store
cleanup project=absent caddy=absent env=absent containers=0 volumes=0
management launcher=executable current=executable log=600
Remote integration cleanup verified.
postflight=PASS
targeted_smoke=PASS
local_server_env_unchanged=true
Live Telegram/payment/renewal/concurrency and initial panel sync remain BLOCKED; classic-auto-purchase remains OPEN.

SANDBOX promotion scope and exact public identities
{
  "candidate_release_id": 401626512,
  "candidate_tag": "bundle-v2026.10.01.922",
  "candidate_assets": {
    "cabinet-dist.tar.gz": "027b3b294872794e75d677861b6a433b4b7152953c98022ef6b4441ef296adaa",
    "cabinet-dist.tar.gz.sha256": "46d6c3c0413cd7fbb1ee3eb9558b87e068f857516f8d38b93fa0cfab5bbdfd83",
    "installer-2026.10.01.922.tar.gz": "eff17b515f9714dcefee88652d884e64598300941f3b9519d77bcf9e2e75752d",
    "installer-2026.10.01.922.tar.gz.sha256": "a27dd02cde14543831aa488d6066c6505e612a6012ba5a43b981e3f760580e75",
    "release-provenance.json": "39e1d94baf9689d344c7e1364b85851de7672e0bf043bc1494e6b74a1fd7fe24",
    "release.json": "6a1380505b9597aad380dfeb117e9b99d1f6cda6a4b54146ecb532304910f457"
  },
  "publication_run_id": 36980049522,
  "publication_attempt": 1,
  "installer": {
    "installer_sha": "75c49bec9c2a764e123fc0ef675f8c45fc22a1ab",
    "installer_tree_sha": "6606a783904f81959441b846e757004530728908",
    "archive_sha256": "eff17b515f9714dcefee88652d884e64598300941f3b9519d77bcf9e2e75752d"
  },
  "cabinet_sha": "3213c89920cf4a0712fcc2a9443eae13b62ccbc7",
  "previous_stable_release_id": 401364352,
  "previous_bundle_identity": "419a22e0c4579d7f9d13750feb97cfe92992cd9daf9e89dcc4a235d0526537e9",
  "previous_manifest_sha256": "8c9aa7a3619a3f6f9fa338cbb72a20d68dc74da39dc1f2b307bab7d3d0be3783",
  "lifecycle_commit": "dd303a3d4fadaca4d993db67063dd72efcf181a5",
  "lifecycle_path": "releases/evidence/sandbox-lifecycle-final-75c49be-20261002.json",
  "protected": {
    "bot_repository": "https://github.com/BEDOLAGA-DEV/remnawave-bedolaga-telegram-bot.git",
    "bot_sha": "877690a7039d1326b2c00eda3e297879b80c0678",
    "postgres_image": "postgres@sha256:4006528dcbdd9be8c1aaa50389caea4e93c46d6f54c3533bcd3253725e526e23",
    "redis_image": "redis@sha256:e7723ff73d963f5cc6d9c4643ea3d989527a402a319239054e9472a7fb9219a2",
    "backend_contract": "1",
    "bot_backend_contract": "1",
    "cabinet_backend_contract": "1",
    "configuration_schema": 1,
    "manifest_schema": 2,
    "migration_policy": "rollback-compatible",
    "target_os": "ubuntu-24.04",
    "target_platform": "linux/amd64"
  },
  "transition": "NOT_REQUIRED: previous and candidate Bot/images/backend/configuration/migration fields are identical; same OS/platform; Cabinet-only test fixture source change. This is not a previous-to-candidate version transition PASS."
}
