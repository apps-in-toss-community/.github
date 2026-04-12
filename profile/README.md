<div align="center">

# apps-in-toss-community

**앱인토스 미니앱 개발을 위한 오픈소스 프로젝트 모음**

[Web Demo](https://apps-in-toss-community.github.io/sdk-example/) · [Landing](https://apps-in-toss-community.github.io/) · [@apps-in-toss/web-framework](https://www.npmjs.com/package/@apps-in-toss/web-framework)

</div>

---

## Projects

### [`@ait-co/devtools`](https://github.com/apps-in-toss-community/devtools)

`@apps-in-toss/web-framework` SDK의 **mock 라이브러리**. 앱인토스 미니앱을 **토스 앱 없이 일반 크롬 브라우저에서 개발/테스트**할 수 있게 해준다.

- Universal bundler plugin (Vite / Webpack / Rollup / esbuild / Rspack)
- Floating DevTools panel (vanilla DOM)
- 100% type-compatible mocks (compile-time verified)

### [`sdk-example`](https://github.com/apps-in-toss-community/sdk-example)

SDK의 모든 public API를 **인터랙티브하게 테스트**할 수 있는 레퍼런스 앱.

- 16개 도메인 페이지 (Auth / Storage / IAP / Ads / ...)
- 워크플로우 기반 UI (IAP 구매 flow, Ads load→show)
- React 19 + Vite + Tailwind CSS

**[👉 Open Web Demo](https://apps-in-toss-community.github.io/sdk-example/)**

---

## Getting started

로컬에서 미니앱을 개발 중이라면 `@ait-co/devtools`를 추가하세요:

```bash
pnpm add -D @ait-co/devtools
```

`vite.config.ts`에 플러그인을 추가하면 `@apps-in-toss/web-framework` import가 개발 중에는 자동으로 mock으로 swap됩니다:

```ts
import { defineConfig } from 'vite';
import aitDevtools from '@ait-co/devtools/unplugin';

export default defineConfig({
  plugins: [aitDevtools.vite({ panel: true })],
});
```

실제 배포 시에는 원본 SDK가 그대로 사용됩니다.

---

## Resources

- 📦 [@apps-in-toss/web-framework](https://www.npmjs.com/package/@apps-in-toss/web-framework) — 원본 SDK
- 🌐 [Community Landing](https://apps-in-toss-community.github.io/) — 프로젝트 허브
- 🧪 [SDK Example (Web Demo)](https://apps-in-toss-community.github.io/sdk-example/) — 모든 API를 브라우저에서
