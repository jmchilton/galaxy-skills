# galaxy-ui-driver

Drive a live Galaxy web UI through Galaxy's own Selenium/Playwright test vocabulary with the `gxui`
CLI: verbs are `NavigatesGalaxy` methods, components come from `navigation.yml`, and playwright-cli on
the same browser is the escape hatch. Use it to work through a GTN tutorial or IWC workflow as a user
would, or to reproduce a UI behaviour.

**Status: experimental.** `gxui` is not in a Galaxy release yet. It lives on the `galaxy_ui_driver`
branch of [jmchilton/galaxy](https://github.com/jmchilton/galaxy/tree/galaxy_ui_driver)
(`lib/galaxy/selenium/gxui/`, the `gxui` script of `galaxy-selenium`), stacked on the Galaxy
fixes it needs.

## Requirements

- A Galaxy checkout of that branch and a Python environment with Galaxy's dependencies and
  Playwright's Chromium (`playwright install chromium`).
- `gxui` on `PATH`, run from that environment.
- A login for the Galaxy: a `gxui config` profile with credentials or a saved session (`gxui login
  --save`, or `--interactive` for SSO). See `packages/selenium/README.rst` on that branch.
- Optional: [playwright-cli](https://www.npmjs.com/package/@playwright/cli) for the escape hatch.

## Files

- `SKILL.md` - the skill: verbs, components, escape hatch, observing, failures.
