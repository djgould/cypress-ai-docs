---
title: Installation
nextjs:
  metadata:
    title: Installation
    description: 2 minute installation
---

Quick and easy installation to any Cypress 10+ project in just a few minutes.

---

## Install Dependency

First install cypress ai with the package manager of your choice:

```bash
npm i -D @djgould/cypress-ai
```

### Configure `cypress.config.ts`

Configure `cypress-ai` to run after each test run in your `cypress.config.ts`. Adding it to `setupNodeEvents`.

```js
import { defineConfig } from 'cypress'
import { cypressAI } from '@djgould/cypress-ai'

export default defineConfig({
  e2e: {
    setupNodeEvents(on, config) {
      cypressAI(on, config, { apiKey: process.env.OPENAI_API_KEY })
    },
  },
})
```

Thats it! You should be see the AI debugging after test failures!
