# Prod-deployment Checklist (프로덕션 배포 체크리스트)

## Testing on Staging (스테이징 환경 테스트)

- [ ]  Before creating the release PR, I have tested on staging. (릴리스 PR을 생성하기 전에 스테이징 환경에서 테스트했습니다.)
    - [ ]  iphone (아이폰)
    - [ ]  android phone (안드로이드 폰)
- [ ]  I understand this is especially critical when third-party dependencies are involved. The following third-party dependencies are included in this PR: (서드 파티 의존성이 포함된 경우 특히 중요하다는 것을 이해합니다. 이 PR에 포함된 서드 파티 의존성:)
    - [ ]  …

## Coordination (배포 조율)

- [ ]  This release requires **simultaneous deployment across multiple repositories**, not just a single repo: (이 릴리스는 단일 저장소가 아닌 **여러 저장소의 동시 배포**가 필요합니다:)
    - [ ]  pwa (PWA)
    - [ ]  key-manager (키 매니저)
    - [ ]  foundation-api (파운데이션 API)
    - [ ]  infrastructure (인프라스트럭처)
    - [ ]  pow (POW)
- [ ]  I have carefully planned the deployment order; the order is as follows: (배포 순서를 신중하게 계획했습니다. 순서는 다음과 같습니다:)
    - …

## Load Management (부하 관리)

- [ ]  If notifications will be sent after deployment, concurrent user traffic may increase. I have performed appropriate load tests and taken any necessary actions. (배포 후 알림이 전송될 경우 동시 사용자 트래픽이 증가할 수 있으므로, 적절한 부하 테스트를 수행하고 필요한 조치를 완료했습니다.)

## PWA (PWA)

- [ ]  I acknowledge that I must press the **Prod Manual Deploy** trigger in GitHub Actions to deploy to production. (**Prod Manual Deploy** 트리거를 GitHub Actions에서 눌러야 프로덕션 배포가 진행된다는 것을 알고 있습니다.)
- [ ]  Before pressing the **Prod Manual Deploy** trigger in GitHub Actions, I will run tests on staging. (GitHub Actions의 **Prod Manual Deploy** 트리거를 누르기 전에 스테이징 환경에서 테스트를 진행하겠습니다.)
- **CSP changes** (CSP 변경 사항)
    - [ ]  I have thought very carefully about every asset (image, media, sound, font), script, and network call (RPCs, APIs) and I know that no CSP changes are necessary. (모든 에셋(이미지, 미디어, 사운드, 폰트), 스크립트, 네트워크 호출(RPC, API)을 신중히 검토한 결과 CSP 변경이 필요하지 않음을 확인했습니다.)
    - [ ]  The following CSP changes are necessary: (필요한 CSP 변경 사항:)
        - …
        - [ ]  If CSP changes are needed, I understand that a terraform apply must be run in the **infrastructure** by kerberos or pan. (CSP 변경이 필요할 경우, kerberos 또는 pan이 **infrastructure** 저장소에서 terraform apply를 실행해야 함을 이해합니다.)