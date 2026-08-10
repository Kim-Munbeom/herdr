# herdr


<p align="center">
  <img src="assets/logo.png" alt="herdr" width="100" />
</p>

<p align="center">
  <a href="https://herdr.dev">herdr.dev</a> · <a href="#설치">설치</a> · <a href="https://herdr.dev/docs/quick-start/">빠른 시작</a> · <a href="https://herdr.dev/docs/">문서</a>
</p>

<p align="center">
  <a href="README.md">English</a> · <a href="README.zh-CN.md">简体中文</a> · 한국어
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-Apache--2.0-666666?labelColor=333333" alt="Apache 2.0 license" /></a>
  <a href="https://github.com/herdrdev/herdr/releases"><img src="https://img.shields.io/github/downloads/herdrdev/herdr/total?labelColor=333333&color=666666" alt="total GitHub release downloads" /></a>
  <a href="https://github.com/herdrdev/herdr/stargazers"><img src="https://img.shields.io/github/stars/herdrdev/herdr?labelColor=333333&color=666666&logo=github" alt="GitHub stars" /></a>
  <a href="https://github.com/herdrdev/herdr/releases/latest"><img src="https://img.shields.io/github/v/release/herdrdev/herdr?label=release&labelColor=333333&color=666666" alt="latest stable release" /></a>
  <a href="https://formulae.brew.sh/formula/herdr"><img src="https://img.shields.io/homebrew/v/herdr?label=homebrew&labelColor=333333&color=666666" alt="Homebrew version" /></a>
  <a href="https://x.com/herdrdev"><img src="https://img.shields.io/badge/follow-%40herdrdev-000000?logo=x&logoColor=white" alt="follow @herdrdev on X" /></a>
</p>

---

https://github.com/user-attachments/assets/043ec09f-4bdd-41d5-aee0-8fda6b83e267

**코딩 agent가 살아가는 런타임.**

- **항상 실행 중** — herdr는 백그라운드 서버이고, 터미널이 그 안에서 삽니다. 노트북을 덮거나, 네트워크가 끊기거나, 머신을 재시작해도 — agent는 계속 일하고 세션은 그대로 돌아옵니다. 아무 터미널에서나, 또는 ssh로 다시 붙으세요.
- **막힌 agent를 찾아 헤매지 않습니다** — 모든 pane에 working, blocked, idle이 표시됩니다. agent가 멈춰서 답을 기다리면 herdr가 알려줍니다.
- **agent 네이티브** — cli와 socket api는 agent가 직접 다루는 것과 같은 표면입니다. pane을 띄우고, 서로에게 프롬프트를 보내고, 다른 agent가 실제로 blocked 상태가 될 때까지 기다릴 수 있습니다. [agent skill →](https://herdr.dev/docs/agent-skill/)
- **이미 쓰던 것을 그대로 실행합니다** — claude code, codex, cursor, opencode, grok 등등. herdr는 이들을 감싸거나 대체하지 않고, 그 터미널만 소유합니다.
- **키보드와 마우스 모두 일급 시민** — tmux 스타일 prefix 키, *그리고* 클릭·드래그·분할. 도구에 묶이지 말고 순간마다 편한 쪽을 고르세요.
- **플러그인** — pane과 워크플로를 확장합니다. [마켓플레이스 둘러보기 →](https://herdr.dev/plugins/)
- **rust 바이너리 하나, electron 없음** — 이미 쓰고 있는 아무 터미널에서나 돌아갑니다.

---

## 설치

```bash
curl -fsSL https://herdr.dev/install.sh | sh
```

또는 `brew install herdr` · `mise use -g herdr` · windows 베타: `powershell -ExecutionPolicy Bypass -c "irm https://herdr.dev/install.ps1 | iex"` · [바이너리](https://github.com/herdrdev/herdr/releases)

그런 다음 작업이 있는 곳에서 실행하세요:

```bash
herdr
```

agent를 실행하고, pane을 분할하고, 자리를 비우세요. `ctrl+b q`로 분리하고, `herdr`로 다시 붙습니다. [빠른 시작 →](https://herdr.dev/docs/quick-start/)

## 문서

모든 문서는 [herdr.dev/docs](https://herdr.dev/docs/)에 있습니다: [빠른 시작](https://herdr.dev/docs/quick-start/) · [핵심 개념](https://herdr.dev/docs/concepts/) · [지원 agent](https://herdr.dev/docs/agents/) · [키보드](https://herdr.dev/docs/keyboard/) · [설정](https://herdr.dev/docs/configuration/) · [세션 상태](https://herdr.dev/docs/session-state/) · [원격 접속](https://herdr.dev/docs/persistence-remote/) · [통합](https://herdr.dev/docs/integrations/) · [플러그인](https://herdr.dev/docs/plugins/) · [socket api](https://herdr.dev/docs/socket-api/)

## 감사의 말

<a href="https://terminaltrove.com/"><img src="assets/sponsors/terminal-trove.png" alt="Terminal Trove" width="200" /></a>

[Terminal Trove](https://terminaltrove.com/), 그리고 [SPONSORS.md](./SPONSORS.md)에 이름을 올린 모든 후원자분들 — 감사합니다 🐑

기업 / 파트너십 문의: hey@herdr.dev

## agent 안내

이 저장소를 돕는 ai agent라면, 코드를 변경하기 전에 [`AGENTS.md`](./AGENTS.md)를 읽고, issue나 PR을 열기 전에 [`CONTRIBUTING.md`](./CONTRIBUTING.md)를 읽으세요.

## 개발

```bash
git clone https://github.com/herdrdev/herdr
cd herdr
cargo build --release

just test        # 단위 테스트
just check       # 포매팅, 테스트, 유지보수 검사
```

## 라이선스

Herdr는 [Apache License 2.0](LICENSE) 라이선스로 배포됩니다.
