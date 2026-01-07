# Tony English — Design System (One-pager)

목표: “시험”이 아니라 “말하기”를 위한 학습 경험. UI는 따뜻하고 예측 가능하며, 학습자는 영어에만 집중한다.

---

## 1) Principles (지키는 이유)
- **Low Cognitive Load**: UI는 조용하게, 학습은 선명하게
- **Warm & Encouraging**: 경고보다 안내, 실패보다 다음 행동
- **Predictable Consistency**: 페이지마다 같은 규칙(복붙이 아니라 표준화)
- **Mobile-first**: 기본은 스마트폰(터치/스크롤 리듬 최우선)

---

## 2) Tokens (절대값: 바꾸려면 “토큰”부터)
### Colors (5개만 사용: 의미 없는 색 추가 금지)
- **Primary Yellow** `#FFC83D` : 핵심 CTA/환영/강조(감정)
- **Ink Black** `#1F2933` : 제목/본문(가독성)
- **Warm Background** `#FFFBEA` : 페이지 배경(눈 피로 감소)
- **Learning Blue** `#2563EB` : 링크/힌트/정보(신뢰)
- **Success Green** `#22C55E` : 정답/완료/성취

**Color rules**
- Primary는 “행동(CTA)”에만 사용(한 화면 1개 중심 권장)
- 정보/링크는 Blue로 고정
- 정답/완료는 Green + 텍스트(색만으로 의미 전달 금지)

### Typography
- Font: **Pretendard**
- Line-height: **1.6** (학습 UI 고정)
- Weight는 **2~3종**만 사용(예: 400/600/700)

### Spacing (4px rule)
- 4 / 8 / 12 / 16 / 24 / 32 / 48 만 사용  
→ 임의의 18px, 22px 같은 값 금지(일관성 붕괴)

### Radius
- Card: 16px
- Button: pill(999px) / 또는 12px(입력창)

---

## 3) Components (필수만)
### Buttons
- 높이 **44px 이상** (모바일 터치)
- 유형은 3개만:
  - **Primary**: 주요 행동 1개
  - **Secondary**: 보조 행동
  - **Ghost**: 덜 중요한 행동
- 문구는 동사형 권장(예: 시작하기, 다음 문장)

### Cards
- 정보 묶기 도구
- **카드 안 카드 중첩 금지**(복잡도 상승)

### Tables (스펙/규칙 문서화)
- 토큰/규칙은 표로 고정해 유지보수

---

## 4) Patterns (학습 흐름)
### Feedback (정답/오답)
- 정답: 짧게 칭찬 + 다음 행동(“다음 문장”)
- 오답: 비난 금지 + 힌트/재시도(“힌트 보기”, “다시 시도”)

### Progress (진행)
- 진행표시는 불안 감소용 정보(과하게 크지 않게 상단 배치)
- 예: 3/10

### Errors (오류)
- “문제”가 아니라 “해결”을 말한다  
  - ❌ 네트워크 오류  
  - ✅ 인터넷 연결을 확인하고 다시 시도하세요

---

## 5) Anti-patterns (절대 금지)
- 노랑 배경 위 **흰 글자**(가독성 급락)
- 페이지마다 버튼 스타일 제각각
- 새 색 즉흥 추가(의미 체계 붕괴)
- 색만으로 정답/오답 전달
- 클릭 영역 44px 미만
- 애니메이션 과다(학습 방해)
- 포커스 링 제거(접근성 붕괴)

---

## 6) Dev Checklist (페이지 만들 때 30초 점검)
- [ ] 색은 5개 토큰 안에서만 해결했나?
- [ ] Primary 버튼은 1개 중심인가?
- [ ] 텍스트 대비(특히 노랑 위)는 안전한가?
- [ ] 모바일 터치 44px 이상인가?
- [ ] spacing이 4px rule을 지키나?
- [ ] Anti-patterns 위반이 없는가?
