<div align="center">

# apps-in-toss-community

**The most convenient way to build Apps in Toss mini-apps.**

[Landing](https://apps-in-toss-community.github.io/) · [Web Demo](https://apps-in-toss-community.github.io/sdk-example/) · [한국어 →](./README.md)

</div>

---

## What we're building

An open-source toolchain that makes every step of Apps in Toss mini-app development smoother.

- 🛠️ **Develop** without the Toss app — run mocks in your browser
- 🧪 **Experiment** with every SDK API interactively
- 🌐 **Write** with standard Web APIs instead of the proprietary SDK
- 📚 **Learn** from clean, friendly docs
- 🤖 **Automate** your mini-app development with Claude Code

---

## Projects

### ✅ Available Now

| Project | Description |
|---|---|
| [**`@ait-co/devtools`**](https://github.com/apps-in-toss-community/devtools) | A mock library for `@apps-in-toss/web-framework`, a universal bundler plugin, and a floating DevTools panel. **Develop mini-apps in Chrome without the Toss app.** |
| [**`sdk-example`**](https://github.com/apps-in-toss-community/sdk-example) | A reference app to **run every SDK API interactively in your browser** and read the corresponding code side-by-side. → [Web Demo](https://apps-in-toss-community.github.io/sdk-example/) |

### 🚧 Coming Soon

| Project | Description |
|---|---|
| [**`@ait-co/polyfill`**](https://github.com/apps-in-toss-community/polyfill) | Build mini-apps using **standard Web APIs** (`navigator.clipboard`, `navigator.geolocation`, etc.) instead of the proprietary SDK. |
| [**`docs`**](https://github.com/apps-in-toss-community/docs) | A **cleaner, friendlier** guide and reference built on top of the official documentation. |
| [**`claude-code-plugin`**](https://github.com/apps-in-toss-community/claude-code-plugin) | Tie everything together and **build, test, and publish mini-apps from inside Claude Code**. |

---

## Quick start

If you are already developing a mini-app locally, add `@ait-co/devtools`:

```bash
pnpm add -D @ait-co/devtools
```

Adding the plugin to `vite.config.ts` swaps `@apps-in-toss/web-framework` imports for mocks at dev time:

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
