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

### pwa

- [ ]  I acknowledge that I must press the **Prod Manual Deploy** trigger in GitHub Actions to deploy to production.
- [ ]  Before pressing the **Prod Manual Deploy** trigger in GitHub Actions, I will run tests on staging.
- **CSP changes**
    - [ ]  I have thought very carefully about every asset (image, media, sound, font), script, and network call (RPCs, APIs) and I know that no CSP changes are necessary.
    - [ ]  The following CSP changes are necessary:
        - …
        - [ ]  If CSP changes are needed, I understand that a `terraform apply` must be run in the **infrastructure** by kerberos or pan.
