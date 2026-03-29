---
schema_version: "1.0"
---

# Agent Manifest: intelastart.com

```yaml
repo: intelastart.com
type: static-site
description: "Static HTML marketing site — services, pricing, blog pages for IntelaStart"
owner: migar-git
```

## Authority

```yaml
authority:
  max_auto_level: 1
  always_open_pr: true
  protected_paths:
    - .env*
  notify_on: [2, 3]
  allowed_machines: []
```

## Commands

```yaml
commands:
  test:   ""
  lint:   ""
  format: ""
  build:  ""
  deploy: ""
```

## LLM Routing

```yaml
llm:
  local_model: "qwen2.5-coder:7b"
  escalate_on:
    - cross_repo_change
    - architecture_decision
    - security_related
    - confidence_below: 0.75
```

## Dependencies

```yaml
dependencies: []
```

## CI / Analytics

```yaml
ci:
  push_results: false
  min_pass_rate: 1.0
  track:
    - lint_errors
```

## Notes

```yaml
notes: |
  - Static HTML marketing site for IntelaStart brand
  - Pages: services, pricing, blog
  - No build system — pure HTML/CSS/JS
```
