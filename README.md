# 🎵 음악 수업 슬라이드 시스템

## 폴더 구조
```
music-lessons/
├── viewer.html              ← 뷰어 쉘 (건드리지 않아도 됨)
├── index.html               ← 수업 목록 메인 페이지
├── lessons/
│   ├── 01-crescendo.json    ← 크레센도/디크레센도 수업
│   └── 02-다음수업.json      ← 앞으로 추가할 수업들
└── README.md
```

## 사용법

### GitHub Pages 배포
1. GitHub에 `music-lessons` 레포 생성
2. 이 폴더 전체를 push
3. Settings → Pages → main branch 선택
4. `https://soonhong99.github.io/music-lessons/` 로 접근

### 수업 시간 사용
- `index.html` 열면 수업 목록
- 각 카드 클릭하면 슬라이드 뷰어
- **F11**: 전체화면
- **← →**: 슬라이드 이동

### 새 수업 추가 (Claude에게 요청)
```
"다음 JSON 형식으로 [주제] 수업 만들어줘.
슬라이드 타입: intro / experience / compare / quiz"
```

Claude가 JSON만 뱉어주면:
1. `lessons/0X-주제.json` 으로 저장
2. `index.html`에 카드 한 줄 추가
3. push → 끝

## JSON 슬라이드 타입

| type | 설명 |
|------|------|
| `intro` | 개념 소개 + 비유 |
| `experience` | 소리 체험 (자동 재생) |
| `compare` | 두 개념 나란히 비교 |
| `quiz` | 퀴즈 |

## 색상 커스터마이징
`meta` 안의 `color_a`, `color_b` 등을 바꾸면
뷰어 전체 색상이 자동으로 바뀜.
