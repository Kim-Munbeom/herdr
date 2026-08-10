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

**코딩 agent가 상주하는 런타임.**

- **항상 실행** — herdr는 백그라운드 서버로 동작하며, 터미널은 그 내부에서 실행됩니다. 노트북을 닫거나 네트워크가 끊기거나 머신을 재시작해도 agent는 작업을 계속하고 세션은 그대로 복원됩니다. 임의의 터미널에서, 또는 ssh를 통해 다시 연결할 수 있습니다.
- **멈춘 agent 즉시 식별** — 모든 pane에 working, blocked, idle 상태가 표시됩니다. agent가 작업을 멈추고 응답을 기다리면 herdr가 이를 알립니다.
- **agent 네이티브** — cli와 socket api는 agent가 직접 사용하는 것과 동일한 인터페이스입니다. pane을 생성하고, 서로에게 프롬프트를 전달하며, 다른 agent가 실제로 blocked 상태에 도달할 때까지 대기할 수 있습니다. [agent skill →](https://herdr.dev/docs/agent-skill/)
- **기존 도구 그대로 실행** — claude code, codex, cursor, opencode, grok 등을 지원합니다. herdr는 이들을 감싸거나 대체하지 않으며, 해당 터미널을 소유할 뿐입니다.
- **키보드와 마우스 모두 일급 지원** — tmux 방식의 prefix 키와 함께 클릭, 드래그, 분할을 제공합니다. 도구가 아니라 상황에 따라 선택할 수 있습니다.
- **플러그인** — pane과 워크플로를 확장합니다. [마켓플레이스 둘러보기 →](https://herdr.dev/plugins/)
- **rust 바이너리 하나, electron 없음** — 기존에 사용 중인 터미널에서 그대로 동작합니다.

---

## 설치

```bash
curl -fsSL https://herdr.dev/install.sh | sh
```

또는 `brew install herdr` · `mise use -g herdr` · windows 베타: `powershell -ExecutionPolicy Bypass -c "irm https://herdr.dev/install.ps1 | iex"` · [바이너리](https://github.com/herdrdev/herdr/releases)

설치 후 작업이 위치한 디렉터리에서 실행합니다.

```bash
herdr
```

agent를 실행하고 pane을 분할한 뒤 자리를 비워도 됩니다. `ctrl+b q`로 분리하고 `herdr`로 다시 연결합니다. [빠른 시작 →](https://herdr.dev/docs/quick-start/)

## 문서

모든 문서는 [herdr.dev/docs](https://herdr.dev/docs/)에서 확인할 수 있습니다. [빠른 시작](https://herdr.dev/docs/quick-start/) · [핵심 개념](https://herdr.dev/docs/concepts/) · [지원 agent](https://herdr.dev/docs/agents/) · [키보드](https://herdr.dev/docs/keyboard/) · [설정](https://herdr.dev/docs/configuration/) · [세션 상태](https://herdr.dev/docs/session-state/) · [원격 접속](https://herdr.dev/docs/persistence-remote/) · [통합](https://herdr.dev/docs/integrations/) · [플러그인](https://herdr.dev/docs/plugins/) · [socket api](https://herdr.dev/docs/socket-api/)

## 감사의 말

<a href="https://terminaltrove.com/"><img src="assets/sponsors/terminal-trove.png" alt="Terminal Trove" width="200" /></a>

[Terminal Trove](https://terminaltrove.com/)와 [SPONSORS.md](./SPONSORS.md)에 기재된 모든 후원자 여러분께 감사드립니다 🐑

기업 및 파트너십 문의: hey@herdr.dev

## agent 안내

이 저장소의 작업을 돕는 ai agent라면 코드를 변경하기 전에 [`AGENTS.md`](./AGENTS.md)를, issue나 PR을 열기 전에 [`CONTRIBUTING.md`](./CONTRIBUTING.md)를 읽어야 합니다.

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
