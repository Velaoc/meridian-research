<!-- foundation:identity -->
# Meridian Research

An AI research agent app where a signed-in user submits a research question, the agent runs a sequence of steps, and each step's activity and result is recorded and shown as a timeline, ending in a sy

- Site: https://meridian-research.api.holode.xyz
- Support: support@meridian-research.api.holode.xyz
<!-- /foundation:identity -->

## What this is

An AI research agent app where a signed-in user submits a research question, the agent runs a sequence of steps, and each step's activity and result is recorded and shown as a timeline, ending in a synthesized answer.

## Who it is for

- Researcher (signed-in user)
- Research Agent (runs steps via a provider adapter)

## Main features

- **Sign in and start a research project** — User submits a research question from the new-research form.
- **Run the agent** — Agent executes steps in order; each step's status and result is persisted as it completes.
- **View the timeline** — Research show page renders the recorded steps as a timeline plus the final synthesis.
- **Review past runs** — User's research index lists previous questions, dates, and statuses.

## Core entities

- User
- Research
- Step

## Run locally

```bash
bundle install
bin/rails db:prepare
bin/dev
```

Requires Ruby, PostgreSQL, and the usual Rails toolchain. See `bin/setup` if present.

## Demo

A demo user with one completed research run ("The history of espresso") showing a full timeline of completed steps and a final synthesis, so the timeline UI is visible immediately.

## Deploy notes

Production `config.hosts` is derived from `domain` in `config/foundation.yml`. Keep that value aligned with the real host or every request will 403.
