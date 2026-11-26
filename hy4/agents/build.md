---
model: opencode/hy4-flash-free#high
mode: all
steps: 21
request:
  body:
    temperature: 0.8
    top_p: 1
permissions:
  - action: "*"
    resource: "*"
    effect: allow
  - action: shell
    resource: "*"
    effect: allow
  - action: edit
    resource: "*"
    effect: allow
  - action: read
    resource: "*"
    effect: allow
  - action: glob
    resource: "*"
    effect: allow
  - action: grep
    resource: "*"
    effect: allow
  - action: patch
    resource: "*"
    effect: allow
  - action: webfetch
    resource: "*"
    effect: allow
  - action: websearch
    resource: "*"
    effect: allow
  - action: skill
    resource: "*"
    effect: allow
  - action: subagent
    resource: "*"
    effect: allow
  - action: question
    resource: "*"
    effect: allow
  - action: external_directory
    resource: "*"
    effect: allow
  - action: openchamber
    resource: "*"
    effect: allow
  - action: openchamber_web
    resource: "*"
    effect: allow
  - action: openchamber_notify
    resource: "*"
    effect: allow
  - action: openchamber_memory
    resource: "*"
    effect: allow
  - action: filesystem_*
    resource: "*"
    effect: allow
  - action: memory_*
    resource: "*"
    effect: allow
  - action: sequential-thinking_*
    resource: "*"
    effect: allow
  - action: playwright_*
    resource: "*"
    effect: allow
  - action: github_*
    resource: "*"
    effect: allow
  - action: everything_*
    resource: "*"
    effect: allow
  - action: infinity
    resource: "*"
    effect: allow
---

software malfare hardware firewalls agen It agentsy