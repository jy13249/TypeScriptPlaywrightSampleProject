# TypeScript Playwright Sample Project

This repository demonstrates how to use [Playwright](https://playwright.dev/) with [TypeScript](https://www.typescriptlang.org/) for end-to-end testing.

## Prerequisites

- [Node.js](https://nodejs.org/) (v16+ recommended)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)

## Getting Started

1. **Install dependencies**

   ```cmd
   npm install
   ```

2. **Run Playwright install** (to download browsers)

   ```cmd
   npx playwright install
   ```

3. **Run tests**

   ```cmd
   npx playwright test
   ```

## Project Structure

- `tests/` - Contains your test files (TypeScript)
- `playwright.config.ts` - Playwright configuration file
- `package.json` - Project metadata and scripts

## Writing Tests

Create your test files in the `tests/` directory using TypeScript. Example:

```typescript
import { test, expect } from '@playwright/test';

test('homepage has title', async ({ page }) => {
  await page.goto('https://playwright.dev/');
  await expect(page).toHaveTitle(/Playwright/);
});
```

## Useful Commands

- Run all tests:
  ```cmd
  npx playwright test
  ```
- Run tests in headed mode:
  ```cmd
  npx playwright test --headed
  ```
- Generate test report:
  ```cmd
  npx playwright show-report
  ```

## Resources

- [Playwright Documentation](https://playwright.dev/docs/intro)
- [TypeScript Documentation](https://www.typescriptlang.org/docs/)

## License

MIT
