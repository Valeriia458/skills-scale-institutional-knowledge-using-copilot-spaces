# Release Checklist

Pre-release
- [ ] All acceptance criteria met and PRs merged
- [ ] Passing CI and security scans
- [ ] Release notes drafted and reviewed
- [ ] Migration steps identified (if applicable)
- [ ] Rollback and mitigation plan documented
- [ ] Stakeholders and support teams notified of release window
- [ ] Smoke tests identified and owners assigned

Deploy
- [ ] Backup/snapshot taken if applicable
- [ ] Deploy to staging and run smoke tests
- [ ] Validate telemetry and alerts are active
- [ ] Deploy to production (automated pipeline preferred)

Post-deploy
- [ ] Run post-deploy verification checklist
- [ ] Monitor dashboards for errors, latency, and user impact
- [ ] Confirm success metrics are being recorded
- [ ] Communicate release completion to stakeholders
- [ ] Capture any follow-up items as issues

Rollback (if needed)
- [ ] Execute rollback plan and notify stakeholders
- [ ] Triage the incident and capture action items
- [ ] Run a blameless post-incident review
