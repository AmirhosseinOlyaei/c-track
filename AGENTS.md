# Agent Guide

Cloudflare Workers port of career-tracker via vinext (foundation decision D5).

## Foundation

This repository is governed by the DevArts Lab foundation: `../devartslab-foundation`
(remote: `DevArtsLab/devartslab-foundation`). Adopted revision: 3a (2026-10-26).

- Applicable: D1-D15 broadly; this is the foundation-aligned track for the
  career-tracker product (career-tracker ADR-0016 keeps it as the deferred
  hosted-tier path). Also deploys a Response Store Worker - see README deploy
  note.
- Skills resolve by name from `~/.agents/skills/`; do not vendor copies.
- Docs platform status: `refining`. Do not publish to the documentation
  platform; LAB_INDEX is authoritative for readiness.

## Commands and safety

- `pnpm run dev` (vinext dev), `pnpm run build` (worker output), `pnpm run
  deploy` plus `pnpm run deploy:response-store` for the second Worker.
- Add `.cloudflare/types` to tsconfig include; run `cf workers types` before
  standalone typechecks. `pnpm approve-builds` then `pnpm install` if build
  scripts were blocked.
- Track work in the DevArts Lab Linear workspace.
