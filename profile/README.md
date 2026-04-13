<div align="center">

# apps-in-toss-community

**앱인토스 미니앱 개발을 가장 편하게.**

[Landing](https://apps-in-toss-community.github.io/) · [Web Demo](https://apps-in-toss-community.github.io/sdk-example/) · [English →](./README.en.md)

</div>

---

## 이런 것들을 할 수 있어요

- 🛠️ **배포도 샌드박스도 없이** — 브라우저에서 바로 미니앱을 구동합니다
- 🧪 **문서만 읽는 대신** — 모든 SDK API를 직접 눌러 확인합니다
- 🌐 **새 SDK를 배우는 대신** — 익숙한 웹 표준 API로 작성합니다
- 📚 **문서에서 헤매는 대신** — 잘 정리된 가이드로 바로 시작합니다
- 🤖 **수동 반복 대신** — Claude Code로 만들고 배포합니다

---

## Projects

### ✅ Available Now

| Project | Description |
|---|---|
| [**`@ait-co/devtools`**](https://github.com/apps-in-toss-community/devtools) | `@apps-in-toss/web-framework` SDK의 mock 라이브러리, 번들러 플러그인, floating DevTools 패널. **토스 앱 없이 웹 브라우저에서 미니앱을 구동·테스트**할 수 있습니다. |
| [**`sdk-example`**](https://github.com/apps-in-toss-community/sdk-example) | 모든 SDK API를 직접 실행해보면서 해당 코드를 **나란히 확인할 수 있는 인터랙티브 레퍼런스 앱**. → [Web Demo](https://apps-in-toss-community.github.io/sdk-example/) |

### 🚧 Coming Soon

| Project | Description |
|---|---|
| [**`@ait-co/polyfill`**](https://github.com/apps-in-toss-community/polyfill) | 독점 SDK 대신 **웹 표준 API**(`navigator.clipboard`, `navigator.geolocation`, ...)를 그대로 사용해 미니앱을 만들 수 있는 polyfill. |
| [**`docs`**](https://github.com/apps-in-toss-community/docs) | 앱인토스 공식 문서를 기반으로 더 **세련되고 친절하게** 재구성한 커뮤니티 가이드/레퍼런스. |
| [**`claude-code-plugin`**](https://github.com/apps-in-toss-community/claude-code-plugin) | 위 도구들을 엮어 **Claude Code 안에서 미니앱을 생성·개발·테스트·배포**할 수 있게 해주는 커뮤니티 플러그인. |

---

## devtools로 시작하기

개발 중인 미니앱에 `@ait-co/devtools`를 추가합니다:

```bash
pnpm add -D @ait-co/devtools
```

`vite.config.ts`에 플러그인을 추가하면, 개발 중에는 SDK import가 자동으로 mock으로 대체되어 브라우저에서 바로 실행할 수 있습니다:

```ts
import { defineConfig } from 'vite';
import aitDevtools from '@ait-co/devtools/unplugin';

export default defineConfig({
  plugins: [aitDevtools.vite({ panel: true })],
});
```

실제 배포에서는 원본 SDK가 그대로 사용됩니다.

---

## Resources

- 📦 [`@apps-in-toss/web-framework`](https://www.npmjs.com/package/@apps-in-toss/web-framework) — 원본 SDK
- 🏠 [Landing page](https://apps-in-toss-community.github.io/) — 프로젝트 허브
- 🧪 [SDK Web Demo](https://apps-in-toss-community.github.io/sdk-example/) — 브라우저에서 모든 API 실행
