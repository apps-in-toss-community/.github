<div align="center">

# apps-in-toss-community

**The most convenient way to build Apps in Toss mini-apps.**

[Landing](https://aitc.dev/) · [Web Demo](https://apps-in-toss-community.github.io/sdk-example/) · [한국어 →](./README.md)

</div>

---

## What we offer

- 🛠️ **No deploys, no sandbox** — run your mini-app right in the browser
- 🧪 **No guessing from docs** — call every SDK API and see the result
- 🌐 **No new SDK to learn** — write with Web APIs you already know
- 📚 **No hunting through docs** — friendly, curated guides
- 🤖 **No manual grunt work** — build and ship with Claude Code

---

## Projects

### ✅ Available Now

| Project | Description |
|---|---|
| [**`@ait-co/devtools`**](https://github.com/apps-in-toss-community/devtools) | A mock library for `@apps-in-toss/web-framework` with a bundler plugin and a floating DevTools panel. **Run and test your mini-app in any web browser** without the Toss app. |
| [**`sdk-example`**](https://github.com/apps-in-toss-community/sdk-example) | An **interactive reference app** — run any SDK API and inspect the JSON result and execution history in real time. → [Web Demo](https://apps-in-toss-community.github.io/sdk-example/) |
| [**`@ait-co/polyfill`**](https://github.com/apps-in-toss-community/polyfill) | A polyfill so you can build mini-apps with **standard Web APIs** (`navigator.clipboard`, `navigator.geolocation`, ...) instead of the proprietary SDK. |
| [**`console-cli`**](https://github.com/apps-in-toss-community/console-cli) | CLI for the Apps in Toss console — log in once in a browser, then drive builds, deploys, and releases from your shell via headless automation. |

### 🚧 Coming Soon

| Project | Description |
|---|---|
| [**`docs`**](https://github.com/apps-in-toss-community/docs) | A **cleaner, friendlier** community-maintained set of guides and references, built on top of the Apps in Toss official documentation. |
| [**`oidc-bridge`**](https://github.com/apps-in-toss-community/oidc-bridge) | An open-source server that bridges Toss login into **standard OIDC** and **Firebase Custom Tokens** — plug straight into Supabase Auth, Firebase Auth, Auth0, or any OIDC-compatible IdP. Public instance planned. |
| [**`agent-plugin`**](https://github.com/apps-in-toss-community/agent-plugin) | A community plugin that ties everything together — **scaffold, develop, test, and publish mini-apps from inside Claude Code and OpenAI Codex**. Planned dual-distribution to both marketplaces from a single repo. |

---

## Getting started with devtools

Add `@ait-co/devtools` to your mini-app project:

```bash
pnpm add -D @ait-co/devtools
```

Add the plugin to `vite.config.ts` and SDK imports are automatically swapped for mocks at dev time, so your app runs straight in the browser:

```ts
import { defineConfig } from 'vite';
import aitDevtools from '@ait-co/devtools/unplugin';

export default defineConfig({
  plugins: [aitDevtools.vite({ panel: true })],
});
```

The real SDK is used as-is in production.

---

## Resources

- 📦 [`@apps-in-toss/web-framework`](https://www.npmjs.com/package/@apps-in-toss/web-framework) — the underlying SDK
- 🏠 [Landing page](https://aitc.dev/) — project hub
- 🧪 [SDK Web Demo](https://apps-in-toss-community.github.io/sdk-example/) — every API in your browser
