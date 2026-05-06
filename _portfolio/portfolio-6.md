---
title: "Capstone: Healthcare Documentation Automation"
excerpt: "Capstone with a 4-person team building an AI-assisted clinical documentation tool for a healthcare startup. Owned the persistence layer migration from an in-memory store to PostgreSQL with asyncpg, and designed a provenance tracking system end-to-end (REST endpoint plus a React ring-chart frontend) because clinicians need to audit which inputs drove which AI-generated outputs. The provenance work was the part that actually mattered — auditability is non-negotiable in healthcare."
collection: portfolio
date_range: "Jan 2025 – Jun 2025"
header:
  teaser: kivo.jpg
---

## Overview

A 4-person UW capstone team partnered with a healthcare startup to automate a piece of clinical documentation that providers were spending significant time writing by hand. The project explored how a structured AI pipeline could generate reviewable drafts from existing intake data.

## My Contributions

**Persistence Layer**

The early system kept job state in memory, which didn't survive restarts. I migrated state management to PostgreSQL using async Python tooling and integrated it into the existing backend so jobs could be tracked reliably across runs.

**Provenance Tracking**

In healthcare AI, you need to be able to show how an output was produced. I designed and implemented an audit trail covering pipeline-level inputs, outputs, and metadata, exposed it through a REST endpoint, and built a React frontend component (with a ring-chart visualization) to make the trail readable to non-engineers.

## Takeaways

- Async database work demands more intentional design than ORM-based approaches, especially around connection pooling and error handling.
- Owning infrastructure that teammates depend on is a different kind of pressure than working on isolated features.
- Translating technical tradeoffs into business terms during sponsor meetings is harder than it sounds.

*Project details have been generalized to respect the sponsor's confidentiality.*
