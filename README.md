Where to run automated end-to-end tests in the pipeline

Preferred option: Within a GitHub Action that runs whenever code is pushed

Why: Running tests in CI on each push ensures fast, consistent feedback across environments, catches regressions before merging, and enforces quality gates for pull requests. Automated CI tests are reproducible and run in a controlled environment, avoiding reliance on manual local runs and reducing the chance of shipping broken code. They complement local testing by providing an enforced, shared safety net for the whole team.

Alternative: Developers should still run key tests locally before pushing for quicker iteration and debugging, but CI should be the authoritative gate.

## Lighthouse Audit Results

### Question 3: Difference between Navigation and Snapshot Mode

**Navigation mode:** Analyzes a page right after it loads and provides overall performance metrics. Cannot analyze interactions or dynamic content changes.

**Snapshot mode:** Analyzes a page in its current static state and is best for finding accessibility issues. Cannot analyze JavaScript performance or DOM tree changes.

### Question 4: Three Improvements for CSE 110 Shop

Based on actual Lighthouse audit results:
1. **Reduce unused JavaScript** – Eliminate 2,079 KiB of unused JavaScript through code splitting or tree-shaking to reduce bundle size and improve load time
2. **Avoid long main-thread tasks** – Break up the 3 long-running tasks identified into smaller chunks to prevent blocking user interactions
3. **Add missing metadata** – Add `lang` attribute to the `<html>` element and include a meta description tag for better SEO and accessibility






