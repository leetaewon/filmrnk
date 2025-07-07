# 장르 및 등급 Glossary

> 영화 장르와 관람등급의 다국어 통일 가이드

## 업데이트 정보
- **최종 업데이트**: 2025-01-07

---

## 영화 장르

| ID | 한국어 | English | 中文简体 | Español |
|---|---|---|---|---|
| action | 액션 | Action | 动作 | Acción |
| comedy | 코미디 | Comedy | 喜剧 | Comedia |
| crime | 범죄 | Crime | 犯罪 | Crimen |
| drama | 드라마 | Drama | 剧情 | Drama |
| fantasy | 판타지 | Fantasy | 奇幻 | Fantasía |
| mystery | 미스터리 | Mystery | 悬疑 | Misterio |
| romance | 로맨스 | Romance | 爱情 | Romance |
| thriller | 스릴러 | Thriller | 惊悚 | Suspense |
| horror | 공포 | Horror | 恐怖 | Terror |
| sci-fi | SF | Sci-Fi | 科幻 | Ciencia Ficción |
| war | 전쟁 | War | 战争 | Bélica |
| historical | 사극 | Historical | 历史 | Histórica |
| noir | 느와르 | Noir | 黑色电影 | Noir |
| family | 가족 | Family | 家庭 | Familiar |
| animation | 애니메이션 | Animation | 动画 | Animación |

---

## 관람 등급

### 한국 영화진흥위원회 등급

| ID | 한국어 | English | 中文简体 | Español | Age |
|---|---|---|---|---|---|
| all | 전체 관람가 | G | 全年龄适宜 | TP | 0+ |
| 12plus | 12세이상 관람가 | PG | 12岁以下不宜 | 12 | 12+ |
| 15plus | 15세이상 관람가 | PG-13 | 15岁以下不宜 | 16 | 15+ |
| 18plus | 청소년 관람불가 | R | 18岁以下不宜 | 18 | 18+ |
| restricted | 제한상영가 | NC-17 | 限制级 | X | 21+ |

### 등급별 설명

| 등급 | 한국어 설명 | English Description |
|---|---|---|
| 전체 관람가 | 모든 연령층이 관람할 수 있는 영화 | Suitable for all ages |
| 12세이상 관람가 | 12세 미만 어린이는 부모 동반 시 관람 가능 | Parental guidance suggested for children under 12 |
| 15세이상 관람가 | 15세 미만 청소년 관람불가 | Not suitable for children under 15 |
| 청소년 관람불가 | 18세 미만 청소년 관람불가 | Adults only - not suitable for minors |
| 제한상영가 | 특별한 상영관에서만 상영 가능 | Restricted screening in designated theaters |

---

## 날짜 표기 형식

| Language | Format | Example |
|---|---|---|
| 한국어 | YYYY.MM.DD | 2024.10.28 |
| English | MMM. DD, YYYY | Oct. 28, 2024 |
| 中文简体 | YYYY年MM月DD日 | 2024年10月28日 |
| Español | DD mmm. YYYY | 28 oct. 2024 |

### 월 약어 (영어)
| 월 | 약어 | 월 | 약어 |
|---|---|---|---|
| January | Jan. | July | Jul. |
| February | Feb. | August | Aug. |
| March | Mar. | September | Sep. |
| April | Apr. | October | Oct. |
| May | May | November | Nov. |
| June | Jun. | December | Dec. |

### 월 약어 (스페인어)
| 월 | 약어 | 월 | 약어 |
|---|---|---|---|
| enero | ene. | julio | jul. |
| febrero | feb. | agosto | ago. |
| marzo | mar. | septiembre | sep. |
| abril | abr. | octubre | oct. |
| mayo | may. | noviembre | nov. |
| junio | jun. | diciembre | dic. |

---

## 사용법

### 장르 표시 예시
```javascript
// 다중 장르 표시
const genres = ['action', 'crime', 'thriller'];
const displayGenres = (genres, language) => {
  return genres.map(genre => getGenreName(genre, language)).join(', ');
};

// 결과: "액션, 범죄, 스릴러" (한국어)
// 결과: "Action, Crime, Thriller" (영어)
```

### 등급 아이콘 표시
```css
.rating-badge {
  display: inline-block;
  padding: 2px 8px;
  border-radius: 4px;
  font-size: 12px;
  font-weight: bold;
}

.rating-all { background: #4CAF50; color: white; }
.rating-12plus { background: #2196F3; color: white; }
.rating-15plus { background: #FF9800; color: white; }
.rating-18plus { background: #F44336; color: white; }
```

### 날짜 형식 변환
```javascript
const formatDate = (dateString, language) => {
  const date = new Date(dateString);
  const formats = {
    'ko': 'YYYY.MM.DD',
    'en': 'MMM. DD, YYYY', 
    'zh-CN': 'YYYY年MM月DD日',
    'es': 'DD mmm. YYYY'
  };
  return formatDateByPattern(date, formats[language]);
};
```