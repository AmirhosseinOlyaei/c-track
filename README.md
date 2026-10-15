# C-Track App

A Cloudflare Workers application for career tracking and resource management.

This project was created with create-vinext-app.

## Scripts

- `pnpm run dev` starts the vinext dev server.
- `pnpm run build` builds the Cloudflare Worker output.
- `pnpm run start` previews the built Worker locally.
- `pnpm run deploy` deploys the Cloudflare Worker.

---

Next steps:

> After `vinext build`, deploy the Response Store Worker explicitly (and repeat when its code/config changes):
>
> pnpm run deploy:response-store
>
> vinext-cloudflare deploy only deploys the application Worker.
> For TypeScript, add ".cloudflare/types" to the include list in tsconfig.json.
> Worker types are generated during dev/build; run `cf workers types` before standalone type-checks.
> Dependency installation is incomplete because pnpm blocked dependency build scripts:
>
> 1. Review and approve the required build scripts:
>    pnpm approve-builds
> 2. Finish installing dependencies:
>    pnpm install
