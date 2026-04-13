<div align="center">

# apps-in-toss-community

**The most convenient way to build Apps in Toss mini-apps.**

[Landing](https://apps-in-toss-community.github.io/) · [Web Demo](https://apps-in-toss-community.github.io/sdk-example/) · [한국어 →](./README.md)

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
| [**`sdk-example`**](https://github.com/apps-in-toss-community/sdk-example) | An **interactive reference app** — run any SDK API and read the matching code side by side. → [Web Demo](https://apps-in-toss-community.github.io/sdk-example/) |

### 🚧 Coming Soon

| Project | Description |
|---|---|
| [**`@ait-co/polyfill`**](https://github.com/apps-in-toss-community/polyfill) | A polyfill so you can build mini-apps with **standard Web APIs** (`navigator.clipboard`, `navigator.geolocation`, ...) instead of the proprietary SDK. |
| [**`docs`**](https://github.com/apps-in-toss-community/docs) | A **cleaner, friendlier** community-maintained set of guides and references, built on top of the Apps in Toss official documentation. |
| [**`claude-code-plugin`**](https://github.com/apps-in-toss-community/claude-code-plugin) | A community plugin that ties everything together — **scaffold, develop, test, and publish mini-apps from inside Claude Code**. |

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
- 🏠 [Landing page](https://apps-in-toss-community.github.io/) — project hub
- 🧪 [SDK Web Demo](https://apps-in-toss-community.github.io/sdk-example/) — every API in your browser
