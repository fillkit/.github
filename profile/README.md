
<div align="center">

![FillKit](https://raw.githubusercontent.com/fillkit/sdk/main/media/logo-rect.svg)

**Context-aware form autofill with realistic data**

[![npm version](https://badge.fury.io/js/@fillkit%2Fcore.svg)](https://www.npmjs.com/package/@fillkit/core)
[![Chrome Web Store](https://img.shields.io/badge/Chrome-Extension-4285F4?logo=googlechrome&logoColor=white)](https://chrome.google.com/webstore/detail/fillkit/)
[![Firefox Add-on](https://img.shields.io/badge/Firefox-Add--on-FF7139?logo=firefox&logoColor=white)](https://addons.mozilla.org/en-US/firefox/addon/fillkit/)
[![Live Demo](https://img.shields.io/badge/Live-demo.fillkit.dev-blue)](https://demo.fillkit.dev)

</div>

---

FillKit reads page structure, labels, and surrounding context to detect what each field expects — then fills it with realistic, coherent data. A checkout form gets a valid card number, matching expiry, and billing address in the same city. A signup form gets a real-looking name, email, and strong password. It recognizes 150+ field types across 50+ languages and generates both valid and intentionally invalid values for edge-case testing.

Use it as a **browser extension** for instant one-click filling, or **embed the SDK** into your app for programmatic control in tests, demos, and development workflows.

<div align="center">

<a href="https://chrome.google.com/webstore/detail/fillkit/"><img src="https://raw.githubusercontent.com/fillkit/sdk/main/media/chrome.svg" width="28" alt="Chrome">&nbsp;&nbsp;Chrome Extension</a>&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://addons.mozilla.org/en-US/firefox/addon/fillkit/"><img src="https://raw.githubusercontent.com/fillkit/sdk/main/media/firefox.svg" width="28" alt="Firefox">&nbsp;&nbsp;Firefox Add-on</a>

</div>

## Repositories

| Repo | Description |
| ---- | ----------- |
| [**sdk**](https://github.com/fillkit/sdk) | Core SDK — `@fillkit/core` and `@fillkit/browser`. TypeScript, 150+ field strategies, 50+ locales, nanostores state, Faker.js-powered local generation. |
| [**in-browser**](https://github.com/fillkit/in-browser) | Chrome MV3 and Firefox browser extensions. Shared codebase, plain JS, esbuild. Zero config — install and fill. |
| [**demo**](https://github.com/fillkit/demo) | Live demos across HTML, React, Vue, and Angular. Try it at [demo.fillkit.dev](https://demo.fillkit.dev). |

## Quick Start

### SDK

```bash
npm install @fillkit/core
```

```typescript
import { FillKit } from '@fillkit/core';

const fk = await FillKit.init({ mode: 'valid', ui: { enabled: true } });
await fk.autofillAll();
```

### Browser Extension

Install from the [Chrome Web Store](https://chrome.google.com/webstore/detail/fillkit/) or [Firefox Add-ons](https://addons.mozilla.org/en-US/firefox/addon/fillkit/), then press `Ctrl+Shift+K` on any page with forms.

| Shortcut | Action |
| -------- | ------ |
| `Ctrl+Shift+K` | Fill all forms on page |
| `Alt+K` | Fill current form |
| `Ctrl+Shift+L` | Clear all filled data |
| `Alt+H` | Show/hide widget |

## Docs

Full API reference, configuration options, and framework guides at [fillkit.dev/docs](https://fillkit.dev/docs) (coming soon).

## Intended Use

FillKit is designed exclusively for **development**, **QA testing**, and **demo environments**. All generated data is synthetic — realistic but entirely fake. FillKit is not intended for filling real forms with real personal information.

## Privacy

FillKit operates entirely on your device by default. No form data is collected or transmitted. See our [Privacy Policy](https://fillkit.dev/privacy) and [Terms of Service](https://fillkit.dev/terms) for full details.

## License

[MIT](https://github.com/fillkit/sdk/blob/main/LICENSE)
