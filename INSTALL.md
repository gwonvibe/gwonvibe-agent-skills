# Gwonvibe Agent Skills 설치안내

이 안내는 배포본 `v1.0.0`을 기준으로 합니다.

저장소를 복제하거나 Release의 ZIP을 푼 폴더에서 시작합니다. `skills` 아래의 18개 폴더를 그대로 복사하며, 각 폴더 안의 `references`, `agents` 같은 부속 폴더도 함께 유지해야 합니다.

```bash
git clone https://github.com/gwonvibe/gwonvibe-agent-skills.git
cd gwonvibe-agent-skills
```

## 설치 위치 선택

| 사용 환경 | 모든 프로젝트에서 사용 | 한 프로젝트에서만 사용 |
|---|---|---|
| Codex | `~/.codex/skills/` | 프로젝트의 `.codex/skills/` |
| Claude Code | `~/.claude/skills/` | 프로젝트의 `.claude/skills/` |

처음에는 **모든 프로젝트에서 사용**하는 설치가 가장 간단합니다. 기존에 같은 이름의 스킬이 있다면 덮어쓰지 말고 먼저 다른 곳에 백업하거나 프로젝트 전용으로 설치하세요.

## 가장 쉬운 설치

Codex나 Claude Code에서 저장소 또는 압축을 푼 폴더를 연 뒤 다음처럼 요청합니다.

```text
이 폴더의 skills 안에 있는 18개 스킬을 내 개인 스킬 폴더에 설치해줘.
같은 이름의 폴더가 이미 있으면 덮어쓰지 말고 목록만 알려줘.
설치 뒤 각 폴더에 SKILL.md가 있는지 확인해줘.
```

에이전트가 제안한 대상 경로가 위 표와 같은지 확인한 다음 설치를 승인합니다.

## 직접 설치 — macOS·Linux

아래 명령은 압축을 푼 스킬팩의 최상위 폴더에서 실행합니다.

### Codex 개인 설치

```bash
mkdir -p ~/.codex/skills
cp -R skills/. ~/.codex/skills/
```

### Claude Code 개인 설치

```bash
mkdir -p ~/.claude/skills
cp -R skills/. ~/.claude/skills/
```

같은 이름의 폴더가 이미 있다면 `cp`를 실행하기 전에 해당 폴더를 백업하세요.

## 직접 설치 — Windows PowerShell

아래 명령은 압축을 푼 스킬팩의 최상위 폴더에서 실행합니다.

### Codex 개인 설치

```powershell
$target = Join-Path $HOME ".codex\skills"
New-Item -ItemType Directory -Force $target | Out-Null
Copy-Item -Recurse ".\skills\*" $target
```

### Claude Code 개인 설치

```powershell
$target = Join-Path $HOME ".claude\skills"
New-Item -ItemType Directory -Force $target | Out-Null
Copy-Item -Recurse ".\skills\*" $target
```

같은 이름의 폴더가 이미 있다면 `Copy-Item`을 실행하기 전에 해당 폴더를 백업하세요.

## 프로젝트 전용 설치

특정 프로젝트에서만 쓰고 싶다면 프로젝트 최상위 폴더에서 설치합니다.

### Codex

```bash
mkdir -p .codex/skills
cp -R /압축을-푼-경로/skills/. .codex/skills/
```

### Claude Code

```bash
mkdir -p .claude/skills
cp -R /압축을-푼-경로/skills/. .claude/skills/
```

Windows에서는 파일 탐색기로 `skills` 안의 18개 폴더를 프로젝트의 `.codex\skills` 또는 `.claude\skills` 안에 복사해도 됩니다.

## 설치 확인

1. Codex 또는 Claude Code를 완전히 종료한 뒤 다시 시작합니다.
2. 새 채팅에서 아래 요청을 입력합니다.

Codex:

```text
$branding을 사용해 브랜드 약속을 점검할 때 먼저 확인할 자료를 알려줘.
```

Claude Code:

```text
/branding 브랜드 약속을 점검할 때 먼저 확인할 자료를 알려줘.
```

3. 스킬의 입력 자료와 작업 순서를 설명하면 설치된 것입니다.

## 삭제

설치했던 위치에서 해당 스킬 폴더를 삭제한 뒤 새 세션을 시작합니다. 다른 스킬까지 함께 지우지 않도록 `skills` 상위 폴더 전체가 아니라 삭제할 스킬 이름의 폴더만 선택하세요.

## 공식 문서

- [Codex 스킬 구조와 설치 위치](https://developers.openai.com/blog/eval-skills)
- [Claude Code 스킬 위치와 사용법](https://code.claude.com/docs/en/skills)
