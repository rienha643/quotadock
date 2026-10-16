# QuotaDock 무료 베타

여러 AI의 남은 한도, 다음 결제일, 마지막으로 확인한 초기화 일정을 한곳에서 보는 Mac 앱입니다. 구독을 잠시 쉬어도 저장된 초기화 일정을 확인해 다시 시작할 시점을 검토할 수 있습니다.

공개 베타는 무료입니다. Apple Silicon과 macOS 14 이상을 대상으로 하며, 사용하는 Codex CLI·Claude Code·Grok Build의 설치·로그인이 필요합니다. 앱은 임시 서명본으로 Developer ID 서명·Apple 공증이 없습니다. 다른 Mac에서 첫 실행할 때 보안 경고나 설치 제한이 나타날 수 있습니다.

## 시작하기

**0.6.10 수정:** Grok 주간 초기화 후 사용률 0%가 응답에서 생략되면 잔여량이 미제공으로 보이던 문제를 고쳤습니다. 유효한 현재 기간이 확인되는 경우에만 잔여 100%로 표시합니다.

[무료 베타 ZIP 다운로드](https://github.com/rienha643/quotadock/releases/download/v0.6.10-beta.1/QuotaDock-0.6.10-beta1-macOS-arm64.zip) · [SHA-256](https://github.com/rienha643/quotadock/releases/download/v0.6.10-beta.1/QuotaDock-0.6.10-beta1-macOS-arm64.sha256) · [릴리스 안내](https://github.com/rienha643/quotadock/releases/tag/v0.6.10-beta.1)

SHA-256을 확인하고 ZIP을 푼 뒤 [시작 안내](docs/START_HERE.md)를 읽어 주세요. 보안 기능 전체를 끄는 설치 방법은 요구하지 않습니다.

앱에는 계정·사용량·개인 기록을 포함하지 않습니다. [개인정보 안내](docs/PRIVACY.md)와 [베타 범위](docs/BETA_INFO.md)를 확인할 수 있습니다. 이 저장소는 베타 패키지·문서·피드백을 공유하는 공간입니다.

## 주요 기능

- 연결한 AI의 잔여량과 선택한 한도를 메뉴 막대에 표시합니다.
- 결제일과 주간 초기화 일정을 함께 확인하고, 연결 해제 후에도 마지막 일정은 보관합니다.
- 한도 회복·결제 전 검토 알림과 제공된 초기화권 보유량·만료 내역을 확인합니다.
- 성공한 한도 관측과 선택적인 로컬 토큰 집계를 표시합니다.
- 한국어·영어와 일정·기록 내보내기를 지원합니다.

Claude 초기화권과 구독 날짜는 공식 웹 창을 열어 확인하는 기능입니다. 모든 혜택이 백그라운드 자동 조회되는 것은 아닙니다. 토큰 합계는 이 Mac에서 확인한 도구 기록의 부분 집계일 수 있습니다. 구독 해지·결제·재구독·초기화권 사용은 공식 서비스에서 사용자가 결정합니다. 공식 서비스와 관계없는 독립 앱입니다.

## 피드백

[피드백 양식](https://github.com/rienha643/quotadock/issues/new/choose)에서 설치·조회 문제를 알려 주세요. 계정 ID·이메일·토큰·쿠키·결제 내역·대화·백업·원본 CLI 로그는 첨부하지 마세요. 사용 7일·14일 뒤 [짧은 후기](docs/FEEDBACK.md)도 부탁드립니다. 긍정적 반응뿐 아니라 현재 도구로 충분하다는 의견도 환영합니다.

## English

**Fixed in 0.6.10:** Grok can omit the percentage field at zero usage after a reset. QuotaDock now shows 100% remaining when a complete, valid current billing period confirms this case; incomplete responses remain unknown.

QuotaDock brings remaining AI quotas, renewal dates and saved reset schedules together on macOS. The free beta targets Apple Silicon and macOS 14+, using your installed, signed-in official Codex CLI, Claude Code or Grok Build.

[Download free beta](https://github.com/rienha643/quotadock/releases/download/v0.6.10-beta.1/QuotaDock-0.6.10-beta1-macOS-arm64.zip) · [SHA-256](https://github.com/rienha643/quotadock/releases/download/v0.6.10-beta.1/QuotaDock-0.6.10-beta1-macOS-arm64.sha256) · [Report an issue or share feedback](https://github.com/rienha643/quotadock/issues/new/choose)

This is an ad-hoc signed beta, without Developer ID or Apple notarization. Installation on another Mac may require an app-specific security exception or may be unavailable under managed policy. [Getting started](docs/QUICK_START_EN.md) · [Privacy](docs/PRIVACY_EN.md) · [Feedback](docs/FEEDBACK_EN.md)

Claude reset-pass inventory and billing dates are on-demand official web reads; local token totals may be partial. The app never purchases, cancels or consumes passes. No personal settings or login data ship in the package. This is an independent app, unaffiliated with the providers.
