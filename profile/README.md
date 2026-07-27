<div align="center">

# apps-in-toss-community

**앱인토스 미니앱 개발을 가장 편하게.**

[Landing](https://aitc.dev/) · [Web Demo](https://sdk-example.aitc.dev/) · [English →](./README.en.md)

</div>

---

## 이런 것들을 할 수 있어요

- 🛠️ **배포도 샌드박스도 없이** — 브라우저에서 바로 미니앱을 구동합니다
- 🧪 **문서만 읽는 대신** — 모든 SDK API를 직접 눌러 확인합니다
- 🌐 **새 SDK를 배우는 대신** — 익숙한 웹 표준 API로 작성합니다
- 📚 **문서에서 헤매는 대신** — 잘 정리된 가이드로 바로 시작합니다
- 🤖 **수동 반복 대신** — Claude Code로 만들고 배포합니다

---

## 프로젝트

### ✅ 사용 가능

| 프로젝트 | 설명 |
|---|---|
| [**`@ait-co/devtools`**](https://github.com/apps-in-toss-community/devtools) | `@apps-in-toss/web-framework` SDK의 mock 라이브러리, 번들러 플러그인, floating DevTools 패널. **토스 앱 없이 웹 브라우저에서 미니앱을 구동·테스트**할 수 있습니다. → [Web Demo](https://devtools.aitc.dev/) |
| [**`sdk-example`**](https://github.com/apps-in-toss-community/sdk-example) | 모든 SDK API를 직접 실행해보면서 **JSON 결과와 실행 이력을 실시간으로 확인할 수 있는 인터랙티브 레퍼런스 앱**. → [Web Demo](https://sdk-example.aitc.dev/) |
| [**`@ait-co/polyfill`**](https://github.com/apps-in-toss-community/polyfill) | SDK를 직접 import하지 않고도 **웹 표준 API**(`navigator.clipboard`, `navigator.geolocation`, ...)를 그대로 써서 미니앱을 만들 수 있는 polyfill — 런타임에 SDK로 자동 라우팅됩니다. |
| [**`@ait-co/debugger`**](https://github.com/apps-in-toss-community/debugger) | 실기기 토스 앱 WebView를 **CDP relay로 붙여 에이전트가 직접 디버깅·테스트**하게 해주는 MCP 데몬 + test runner(`debugger`, `debugger-test` bin). devDependency로 설치하거나 `npx`로 바로 실행할 수 있고, 프로덕션 번들에는 절대 들어가지 않아요. |
| [**`@ait-co/debug-console`**](https://github.com/apps-in-toss-community/debugger) | 실기기 WebView 안에서 도는 **on-device attach 런타임 + eruda 인앱 콘솔**. `@ait-co/debugger`와 짝을 이루는 패키지 중 프로덕션 번들에 들어갈 수 있는 유일한 쪽으로, dependency는 `eruda` 하나뿐이에요. |
| [**`docs`**](https://github.com/apps-in-toss-community/docs) | 앱인토스 SDK 문서를 기반으로 더 **세련되고 친절하게** 재구성한 커뮤니티 가이드/레퍼런스. → [Web Demo](https://docs.aitc.dev/) |
| [**`oidc-bridge`**](https://github.com/apps-in-toss-community/oidc-bridge) | 토스 로그인을 **표준 OIDC**와 **Firebase Custom Token**으로 중계하는 오픈소스 서버. Supabase Auth, Firebase Auth, Auth0 등 어디든 바로 연결할 수 있어요. 공용 인스턴스는 `oidc-bridge.aitc.dev`에서 운영 중. → [Web Demo](https://oidc-bridge.aitc.dev/) |
| [**`console-cli`**](https://github.com/apps-in-toss-community/console-cli) | 앱인토스 콘솔을 **CLI**로 자동화. 최초 로그인만 브라우저로 하고, 이후엔 headless 브라우저로 빌드·배포·릴리스를 커맨드 한 줄로 처리할 수 있어요. |
| [**`agent-plugin`**](https://github.com/apps-in-toss-community/agent-plugin) | 위 도구들을 엮어 **Claude Code 안에서 미니앱을 생성·개발·테스트·배포**할 수 있게 해주는 커뮤니티 플러그인. `/ait new`로 scaffold부터 배포까지 에이전트 안에서 완주할 수 있어요. OpenAI Codex 배포는 스펙 확정 후 추가될 예정입니다. |

### 🚧 예정

| 프로젝트 | 설명 |
|---|---|


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

## 리소스

- 📦 [`@apps-in-toss/web-framework`](https://www.npmjs.com/package/@apps-in-toss/web-framework) — 원본 SDK
- 🏠 [Landing page](https://aitc.dev/) — 프로젝트 허브
- 🧪 [SDK Web Demo](https://sdk-example.aitc.dev/) — 브라우저에서 모든 API 실행

---

커뮤니티 오픈소스 프로젝트입니다.
