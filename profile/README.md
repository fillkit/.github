# FillKit

<!-- cspell:ignore signup waitlist -->

<div align="center">

**Intelligent form autofill for developers, QA teams, and demos**

[![npm version](https://badge.fury.io/js/@fillkit%2Fcore.svg)](https://www.npmjs.com/package/@fillkit/core)
[![TypeScript](https://img.shields.io/badge/TypeScript-Ready-blue.svg)](https://www.typescriptlang.org/)
[![License](https://img.shields.io/badge/License-Source%20Available-yellow.svg)](./LICENSE)

[Website](https://fillkit.dev) • [Documentation](https://fillkit.dev/docs) • [Dashboard](https://fillkit.dev) • [Demo](https://fillkit.dev/demo)

</div>

---

## 🎯 What is FillKit?

FillKit is a comprehensive form autofill solution designed for developers, QA engineers, and product teams. It intelligently detects and fills form fields with realistic, context-aware data—making form testing, demos, and development faster and more reliable.

**No more manual data entry. No more copy-pasting test credentials. Just instant, intelligent form filling.**

---

## ✨ Key Features

### 🧠 Smart Field Detection
Automatically recognizes 100+ field types using multi-signal analysis:
- Input types, names, IDs, placeholders
- Label text and ARIA attributes
- Pattern matching across 20+ languages
- Confidence scoring for accurate mapping

### 🎭 Dual Mode Generation
- **Valid Mode**: Generates data that passes validation (emails, phone numbers, dates, etc.)
- **Invalid Mode**: Intentionally creates invalid data for edge case testing

### 🌍 Multi-Language Support
Built-in support for 20+ locales with locale-aware data generation:
- English, Spanish, French, German, Italian, Portuguese
- Japanese, Korean, Chinese, Arabic
- Russian, Polish, Turkish, Thai, Ukrainian
- And more...

### ⚡ Flexible Data Providers

#### Local Provider (Offline)
- Zero network dependencies
- Powered by Faker.js
- Instant generation
- Perfect for development and testing

#### Cloud Provider (Pro)
- AI-powered context-aware datasets
- Team collaboration and dataset management
- Custom industry-specific data
- Background sync with offline fallback

### 🔄 Watch Mode
Automatically detects and fills new form elements as they appear:
- SPA-friendly (React, Vue, Angular)
- Dynamic form support
- MutationObserver-based
- Debounced for performance

### 🎨 Customizable UI Widget
Optional floating widget with:
- Multiple positioning options (9 placements)
- Theme customization (colors, density, appearance)
- Keyboard shortcuts (Ctrl+Shift+F, Ctrl+Shift+C)
- Shadow DOM isolation

### 📦 Framework Agnostic
Works seamlessly with:
- React, Vue, Angular, Svelte
- Vanilla JavaScript/TypeScript
- Next.js, Nuxt, Remix, SvelteKit
- Any JavaScript environment

---

## 🚀 Quick Start

```bash
npm install @fillkit/core
```

```typescript
import { FillKit } from '@fillkit/core';

const fk = new FillKit({
  mode: 'valid',      // 'valid' | 'invalid'
  locale: 'en',       // 20+ locales supported
  provider: 'local',  // 'local' | 'cloud'
  watchMode: true,    // Auto-fill dynamic forms
});

await fk.autofillAll(); // Fill all forms
```

---

## 💡 Advanced Usage

```typescript
// Event monitoring
fk.on('fieldFilled', ({ semanticType, value }) => {
  console.log(`Filled ${semanticType}: ${value}`);
});

// Custom overrides
await fk.autofillAll({
  overrides: { email: 'custom@example.com' },
});

// Selective filling
await fk.autofillAll({
  includeSelectors: ['.payment-form'],
  excludeSelectors: ['.readonly-field'],
});
```

---

## ☁️ FillKit Cloud

**AI-Powered Datasets** • **Team Collaboration** • **Real-Time Sync**

```typescript
const fk = new FillKit({
  provider: 'cloud',
  providerConfig: {
    projectId: 'prj_abc123',
    token: 'fk_live_xyz789',
  },
});

await fk.syncDatasets(); // Sync from cloud
```

[Get Started →](https://fillkit.dev)


## 🧪 Testing & QA

```typescript
// E2E tests with Playwright/Cypress
test('registration flow', async () => {
  await page.goto('/signup');
  await page.evaluate(() => new FillKit().autofillAll());
  await page.click('[type="submit"]');
  await expect(page).toHaveURL('/dashboard');
});
```

**Manual Testing**: Keyboard shortcuts • Valid/invalid toggle • Instant filling
**Demo Mode**: Pre-fill environments • Realistic previews • Faster onboarding


## 🌐 Browser Extension

**Status**: Coming Soon

The FillKit browser extension will provide:
- Universal form filling without code
- Cross-site autofill with saved profiles
- Privacy-focused local storage
- Sync with FillKit Cloud (optional)

[Join the waitlist →](https://fillkit.dev/extension)

---

## 🤝 Use Cases

| Role | Benefits |
|------|----------|
| **👨‍💻 Developers** | Speed up local development • Test validation logic • Generate realistic preview data |
| **🧪 QA Engineers** | Automate repetitive filling • Test edge cases with invalid data • Reproduce bugs consistently |
| **🎭 Product Demos** | Pre-fill demo environments • Create realistic scenarios • Impress prospects instantly |
| **🤖 Test Automation** | Integrate into E2E suites • Reduce test flakiness • Maintain data consistency |

---

## 📄 License

**FillKit Source Available License**

| Usage Type | Allowed |
|------------|---------|
| Personal projects | ✅ Yes |
| Testing & QA automation | ✅ Yes |
| Educational purposes | ✅ Yes |
| Internal tooling | ✅ Yes |
| Commercial embedding | ❌ Requires license |
| Creating competing services | ❌ No |
| Redistribution | ❌ No |

**Commercial licensing**: justin@claviscore.com • [View full terms →](./LICENSE)

---

## 🔗 Links

**Website**: [fillkit.dev](https://fillkit.dev) • **Docs**: [fillkit.dev/docs](https://fillkit.dev/docs) • **Demo**: [fillkit.dev/demo](https://fillkit.dev/demo) • **NPM**: [@fillkit/core](https://www.npmjs.com/package/@fillkit/core) • **Support**: justin@claviscore.com

---


<div align="center">

[⭐ Star on GitHub](https://github.com/fillkit/sdk) • [📖 Read the Docs](https://fillkit.dev/docs) • [🚀 Get Started](https://fillkit.dev)

</div>
