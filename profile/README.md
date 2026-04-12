<div align="center">

# apps-in-toss-community

**앱인토스 미니앱 개발을 가장 편하게.**

[Landing](https://apps-in-toss-community.github.io/) · [Web Demo](https://apps-in-toss-community.github.io/sdk-example/) · [English →](./README.en.md)

</div>

---

## 우리가 하려는 것

앱인토스 미니앱 개발의 모든 단계를 편하게 만드는 오픈소스 도구 모음을 만듭니다.

- 🛠️ **개발**: 토스 앱 없이 브라우저에서 mock으로 개발하기
- 🧪 **실험**: 모든 SDK API를 인터랙티브하게 테스트하기
- 🌐 **표준**: 독점 SDK 대신 웹 표준 API로 미니앱 작성하기
- 📚 **학습**: 친절하고 세련된 가이드로 배우기
- 🤖 **자동화**: Claude Code로 미니앱 만들고 배포하기

---

## Projects

### ✅ Available Now

| Project | Description |
|---|---|
| [**`@ait-co/devtools`**](https://github.com/apps-in-toss-community/devtools) | `@apps-in-toss/web-framework` SDK의 mock 라이브러리 + universal bundler plugin + floating DevTools panel. **토스 앱 없이 크롬에서 미니앱 개발**. |
| [**`sdk-example`**](https://github.com/apps-in-toss-community/sdk-example) | 실제 SDK API를 브라우저에서 **인터랙티브하게 실행해보고 코드를 함께 확인**할 수 있는 레퍼런스 앱. → [Web Demo](https://apps-in-toss-community.github.io/sdk-example/) |

### 🚧 Coming Soon

| Project | Description |
|---|---|
| [**`@ait-co/polyfill`**](https://github.com/apps-in-toss-community/polyfill) | 독점 SDK 대신 **웹 표준 API**(`navigator.clipboard`, `navigator.geolocation` 등)를 그대로 사용해 미니앱을 만들 수 있는 polyfill. |
| [**`docs`**](https://github.com/apps-in-toss-community/docs) | 공식 문서를 기반으로 더 **세련되고 친절하게 재구성한 가이드/레퍼런스**. |
| [**`claude-code-plugin`**](https://github.com/apps-in-toss-community/claude-code-plugin) | 위 모든 도구를 엮어 **Claude Code 안에서 미니앱을 생성·개발·테스트·배포**하는 공식 플러그인. |

---

## Quick start

로컬에서 미니앱을 개발 중이라면 `@ait-co/devtools`를 추가하세요:

```bash
pnpm add -D @ait-co/devtools
```

`vite.config.ts`에 플러그인을 추가하면 `@apps-in-toss/web-framework` import가 개발 중 자동으로 mock으로 swap됩니다:

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

- 📦 [`@apps-in-toss/web-framework`](https://www.npmjs.com/package/@apps-in-toss/web-framework) — 원본 SDK
- 🏠 [Landing page](https://apps-in-toss-community.github.io/) — 프로젝트 허브
- 🧪 [SDK Web Demo](https://apps-in-toss-community.github.io/sdk-example/) — 브라우저에서 모든 API 실행
