# This PR is a production release - please review with extra care.

## Prod-release Checklist

### Testing on Staging

- [ ]  Before creating the release PR, I have tested on staging.
    - [ ]  iphone
    - [ ]  android phone
- [ ]  I understand this is especially critical when third-party dependencies are involved. The following third-party dependencies are included in this PR:
    - [ ]  …

### Coordination

- [ ]  This release requires **simultaneous deployment across multiple repositories**, not just a single repo:
    - [ ]  pwa
    - [ ]  key-manager
    - [ ]  foundation-api
    - [ ]  infrastructure
    - [ ]  pow
- [ ]  I have carefully planned the deployment order; the order is as follows:
    - …

### Load Management

- [ ]  If notifications will be sent after deployment, concurrent user traffic may increase. I have performed appropriate load tests and taken any necessary actions.

### PWA

- [ ]  I acknowledge that I must press the **Prod Manual Deploy** trigger in GitHub Actions to deploy to production.
- [ ]  Before pressing the **Prod Manual Deploy** trigger in GitHub Actions, I will run tests on staging.
- **CSP changes**
    - [ ]  I have thought very carefully about the following items and I know that no CSP changes are necessary.
        - every asset (image, media, sound, font)
        - script
        - iframe
        - network call (RPCs, APIs)
    - [ ]  If CSP changes are needed, I understand that a terraform apply must be run in the **infrastructure** by kerberos or pan.