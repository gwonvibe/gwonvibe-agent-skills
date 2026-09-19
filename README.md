# Gwonvibe Business Skills

사업 판단, 브랜딩, 콘텐츠 설계를 위한 한국어 AI 에이전트 스킬 8개입니다.

## 포함된 스킬

| 스킬 | 용도 |
|---|---|
| `behavioral-science` | 고객 행동과 선택 가설 분석 |
| `bi-solo` | 1인 사업 후보 비교와 검증 실험 설계 |
| `branding` | 브랜드 방향·포지셔닝·약속 점검 |
| `business-os` | 사업 병목 진단과 다음 행동 선택 |
| `concept-design` | 브랜드·상품·서비스 컨셉 설계 |
| `content-psychology` | 콘텐츠 목표 행동에 맞는 심리 원리와 구조 선택 |
| `growth-marketing` | 제안·채널·리드·전환·측정 설계 |
| `pricing-decision-7steps` | 가격 조사와 가격 후보 판단 |

## 설치

저장소를 복제한 뒤 원하는 스킬 폴더를 사용하는 에이전트의 스킬 경로로 복사합니다.

```bash
git clone https://github.com/gwonvibe/gwonvibe-business-skills.git
```

Claude Code 예시:

```bash
cp -R gwonvibe-business-skills/skills/behavioral-science ~/.claude/skills/
```

Codex 예시:

```bash
cp -R gwonvibe-business-skills/skills/behavioral-science ~/.codex/skills/
```

기존에 같은 이름의 스킬이 있다면 덮어쓰기 전에 내용을 비교하세요. 설치 후 새 대화에서 사용할 수 있습니다.

## 참고

- 실제 고객 반응·수요·매출·전환은 자료 없이 확정하지 않습니다.
- 책과 공개 자료에서 정리한 개념은 원문 전체나 성과 보장을 대신하지 않습니다.
- 외부 발송·게시·지출·가격 변경은 별도 승인이 필요합니다.

## 라이선스

MIT. 참고한 제3자 개념과 상표의 권리는 각 권리자에게 있습니다.
