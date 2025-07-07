# 외유내강 다국어 Glossary

> 외유내강 영화제작사의 다국어 웹사이트를 위한 통합 번역 가이드

## 📁 파일 구조

```
glossary/
├── README.md              # 이 파일 - 전체 가이드
├── movies.md              # 영화 제목 (37편)
├── people.md              # 배우 및 스태프 (89명) 
├── terms.md               # 기본 용어 (25개)
├── genres-ratings.md      # 장르 및 등급
└── roles-works.md         # 배역 및 기타 작품
```

## 🌍 지원 언어

| 언어 | 코드 | 마크다운 컬럼명 | 비고 |
|---|---|---|---|
| 한국어 | ko | 한국어 | 기준 언어 |
| 영어 | en | English | 필수 번역 |
| 중국어 간체 | zh-CN | 中文简体 | 필수 번역 |
| 스페인어 | es | Español | 영어와 동일한 경우 생략 가능 |

## 📊 현재 상태

| 카테고리 | 항목 수 | 완성도 | 비고 |
|---|---|---|---|
| 영화 제목 | 37편 | 100% | ✅ 완료 |
| 인물 정보 | 89명 | 100% | ✅ 완료 |
| 기본 용어 | 25개 | 100% | ✅ 완료 |
| 장르/등급 | 20개 | 100% | ✅ 완료 |
| 배역/작품 | 15개 | 100% | ✅ 완료 |

## 🎯 번역 가이드라인

### 1. 일관성 원칙
- 동일한 인물/작품은 모든 곳에서 같은 번역 사용
- ID 기반으로 통일성 유지
- 업데이트 시 모든 관련 파일 동시 수정

### 2. 언어별 규칙

#### 한국어 (기준)
- 원본 제목 및 이름 사용
- 공식 표기법 준수

#### 영어
- 국제적으로 통용되는 로마자 표기
- 인명: 성-이름 순서 (Hwang Jung-min)
- 영화: 공식 영문 제목 우선

#### 중국어 간체
- 한자 음차 또는 의역
- 간체 표기 사용
- 문화적 맥락 고려한 번역

#### 스페인어  
- 영어와 동일한 경우 생략 (마크다운에서 영어 사용)
- 독특한 번역이 있는 경우만 별도 표기
- 문법적 성별 고려 (Sr./Sra. 등)

### 3. 표기 규칙

#### 날짜
- 한국어: `2024.10.28`
- 영어: `Oct. 28, 2024`  
- 중국어: `2024年10月28日`
- 스페인어: `28 oct. 2024`

#### 등급
- 한국 등급 기준으로 통일
- 해외 등급과 매핑 테이블 제공

#### 장르
- 단수형 사용
- 다중 장르는 쉼표로 구분

## 🔧 사용법

### 1. 번역 추가/수정
```markdown
1. 해당 .md 파일 편집
2. 마크다운 테이블에 항목 추가/수정
3. 커밋 → 자동으로 JSON 생성
4. 웹사이트에서 업데이트된 JSON 사용
```

### 2. 새 영화 추가 예시
```markdown
<!-- movies.md에 추가 -->
| new_movie | 새 영화 | New Movie | 新电影 | Nueva Película | 2025 |
```

### 3. 새 인물 추가 예시
```markdown  
<!-- people.md의 적절한 섹션에 추가 -->
| new_actor | 신배우 | New Actor | 新演员 | New Actor | 배우 |
```

### 4. API 사용법
```javascript
// JSON 로드
const glossary = await fetch('/api/glossary.json').then(r => r.json());

// 영화 제목 조회
const getMovieTitle = (movieId, lang) => {
  const movie = glossary.movies.find(m => m.ID === movieId);
  return movie ? movie[langMap[lang]] : movieId;
};

// 인물 이름 조회  
const getPersonName = (personId, lang) => {
  const person = glossary.people.find(p => p.ID === personId);
  return person ? person[langMap[lang]] : personId;
};
```

## 🤖 자동화

### GitHub Actions
- **커밋 시**: 자동 검증 및 JSON 생성
- **PR 시**: 번역 누락 검사  
- **배포 시**: API 서버 업데이트

### 검증 스크립트
```bash
# 번역 누락 검사
python scripts/validate_glossary.py

# JSON 생성
python scripts/export_json.py

# 통계 업데이트
python scripts/update_stats.py
```

## 📈 확장 계획

### 단기 (1개월)
- [ ] 수상 내역 번역 추가
- [ ] 영화제 정보 다국어화  
- [ ] 인물 프로필 상세 정보

### 중기 (3개월)
- [ ] 일본어 지원 추가
- [ ] 프랑스어 지원 추가
- [ ] 자동 번역 검증 도구

### 장기 (6개월)
- [ ] 웹 기반 편집 도구
- [ ] 번역 품질 관리 시스템
- [ ] AI 번역 보조 도구

## 🔍 문제 해결

### 자주 묻는 질문

**Q: 스페인어 번역이 없는데 어떻게 하나요?**
A: 영어 번역을 그대로 사용합니다. 마크다운에서는 빈 칸으로 두면 됩니다.

**Q: 새로운 언어를 추가하려면?**
A: 1) 마크다운 테이블에 컬럼 추가, 2) export 스크립트 수정, 3) 웹사이트 언어 설정 추가

**Q: 인물 이름이 바뀌었는데 어떻게 업데이트하나요?**
A: people.md에서 해당 인물 정보 수정 후 커밋하면 자동으로 모든 곳에 반영됩니다.

### 연락처
- **담당자**: 웹사이트 관리팀
- **이슈 리포트**: GitHub Issues 사용
- **긴급 수정**: Pull Request 생성

---

*최종 업데이트: 2025-01-07*