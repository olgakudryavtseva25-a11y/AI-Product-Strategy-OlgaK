# Compounding System Design

## Feedback Loops

| Loop | Input | Output | Compounds? | Status |
|------|-------|--------|-----------|--------|
| Recursive Learning — corrections improve future ride guidance | Rider feedback, thumbs-down ratings, unsafe pickup reports, confusing route explanations, support tickets, and golden-dataset failures | Updated prompts, safer pickup rules, improved route explanations, and failed cases added to the evaluation dataset so the same mistake does not ship twice | Y | active |
| Rider Preference Learning — repeated usage improves personalization | Frequent routes, preferred pickup spots, comfort preferences, wait-time tolerance, accessibility needs, and post-ride feedback | More personalized pickup recommendations, better default ride options, saved rider preferences, and higher booking confidence | Y | active |
| City Context Transfer — one city improves the next launch | City-specific driving patterns, road layouts, construction zones, traffic rules, airport pickup behavior, and local regulatory constraints | Better launch playbooks, safer pickup/dropoff recommendations, improved city-specific routing guidance, and faster expansion into new markets | Y | active |
| Network Intelligence — more riders improve fleet efficiency | Rider demand patterns, popular pickup/dropoff zones, peak travel times, vehicle availability, and cancellation behavior | Better vehicle placement, reduced wait times, improved utilization, and stronger supply-demand matching across the service area | Y | active |
| Safety Escalation Loop — serious issues improve guardrails | Scary ride reports, near-miss complaints, unsafe pickup concerns, emergency language, and low-confidence AI answers | Human review, safety-case updates, stricter refusal rules, better escalation triggers, and stronger reliability contract thresholds | Y | active |

**Broken loop identified by partner:**
**Fix plan:**

## Context Connectivity
<!-- How does knowledge flow across teams and domains? Where does it silo? -->

## Governance Policy

**Scope:**
**Autonomy boundaries:**
**Escalation triggers:**
**Audit cadence:**
**Regulatory exposure (EU AI Act / other):**

## Agent Topology
<!-- If using agents: what can each agent do? What can't it do? Who approves what? -->

## Shadow AI Audit

| Tool | Owner | Risk Level | Decision |
|------|-------|-----------|----------|
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |

**Total tools found:**
**Tools after triage:**
**Estimated hidden spend:**
