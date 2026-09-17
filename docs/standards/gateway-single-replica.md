---
type: observation
title: The platform agent gateway on robot-host runs one replica
tags: [robot-host, obtainability, declared-intent]
timestamp: 2026-09-16T00:00:00Z
declares:
  - check: single-replica
    cluster: robot-host
    namespace: kubeagents-system
    object: Deployment/platform-agent-gateway
---

# Gateway at one replica

One agent at a time uses `robot-host`, so its gateway runs one replica. Kept under
`docs/standards/` rather than `knowledge/` on purpose: this repository exercises a declaration
under a non-default path in a registered context repository, and `.kube-agents/intent.yaml` is
what tells the audit to look here.
