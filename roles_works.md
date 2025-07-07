# 배역 및 기타 작품 Glossary

> 영화 내 배역과 영화 외 작품의 다국어 통일 가이드

## 업데이트 정보
- **최진 업데이트**: 2025-01-07

---

## 영화 배역

### 일반 배역

| ID | 한국어 | English | 中文简体 | Español |
|---|---|---|---|---|
| music_store_clerk | 악기점 점원 | Music Store Clerk | 乐器店店员 | Empleado de Tienda de Música |
| delivery_person | 중국집 배달원 | Chinese Food Delivery Person | 中餐馆送餐员 | Repartidor de Comida China |
| passerby | 지나가는 행인 | Passerby | 路人 | Transeúnte |
| narrator | 변사 목소리 | Narrator | 解说员 | Narrador |
| self | 본인 | Self | 本人 | Él mismo / Ella misma |
| special_forces_1 | 특공대 장수1 | Special Forces Officer 1 | 特种部队长1 | Comandante de Fuerzas Especiales 1 |
| musical_director | 뮤지컬 감독 | Musical Director | 音乐剧导演 | Director Musical |
| festival_vip | 전주영화제 VIP 역 | Jeonju Film Festival VIP | 全州电影节贵宾 | VIP del Festival de Cine de Jeonju |

### 캐릭터명 (고유 배역)

| Character ID | 한국어 | English | 中文简体 | Español |
|---|---|---|---|---|
| hong_jong_sae | 홍종세 | Hong Jong-sae | 洪钟世 | Hong Jong-sae |
| yu_seok_hwan | 유석환 | Yu Seok-hwan | 柳石焕 | Yu Seok-hwan |
| mr_kang | 강선생 | Mr. Kang | 姜老师 | Sr. Kang |

---

## 영화 외 작품

### 뮤직비디오

| ID | 한국어 | English | 中文简体 | Español | Artist |
|---|---|---|---|---|---|
| dragonfly_photograph | 드래곤플라이 - 사진 | Dragonfly - Photograph | 蜻蜓 - 照片 | Dragonfly - Photograph | 드래곤플라이 |
| leessang_ballerino | 리쌍 - 발레리노 | Leessang - Ballerino | 李双 - 芭蕾舞者 | Leessang - Ballerino | 리쌍 |
| leessang_breakup | 리쌍 - 헤어지지 못하는 여자, 떠나가지 못하는 남자 | Leessang - A Woman Who Can't Break Up, A Man Who Can't Leave | 李双 - 无法分手的女人，无法离开的男人 | Leessang - A Woman Who Can't Break Up, A Man Who Can't Leave | 리쌍 |

### 다큐멘터리

| ID | 한국어 | English | 中文简体 | Español | Year |
|---|---|---|---|---|---|
| mbc_time_spy | MBC 창사 50주년 특별기획 [타임] - "간첩을 찾아서" | MBC 50th Anniversary Special Project [Time] - "In Search of a Spy" | MBC建台50周年特别企划 [时间] - "寻找间谍" | MBC 50th Anniversary Special Project [Time] - "In Search of a Spy" | 2011 |

### 에세이/도서

| ID | 한국어 | English | 中文简体 | Español | Author |
|---|---|---|---|---|---|
| ryoo_true_colors | 류승완의 본색 | Ryoo Seung-wan's True Colors | 柳升完的本色 | Ryoo Seung-wan's True Colors | 류승완 |
| ryoo_stance | 류승완의 자세 | Ryoo Seung-wan's Stance | 柳升完的姿态 | Ryoo Seung-wan's Stance | 류승완 |

---

## 작품 카테고리

| Category | 한국어 | English | 中文简体 | Español |
|---|---|---|---|---|
| feature_film | 장편영화 | Feature Film | 长篇电影 | Largometraje |
| short_film | 단편영화 | Short Film | 短片 | Cortometraje |
| music_video | 뮤직비디오 | Music Video | 音乐视频 | Video Musical |
| documentary | 다큐멘터리 | Documentary | 纪录片 | Documental |
| tv_special | TV 특집 | TV Special | 电视特辑 | Especial de TV |
| essay | 에세이 | Essay | 散文 | Ensayo |
| book | 도서 | Book | 书籍 | Libro |
| web_series | 웹시리즈 | Web Series | 网络剧 | Serie Web |

---

## 배역 유형

| Role Type | 한국어 | English | 中文简体 | Español |
|---|---|---|---|---|
| lead | 주연 | Lead Role | 主角 | Papel Principal |
| supporting | 조연 | Supporting Role | 配角 | Papel Secundario |
| cameo | 카메오 | Cameo | 客串 | Cameo |
| voice | 성우 | Voice Actor | 配音演员 | Actor de Voz |
| narrator | 내레이션 | Narrator | 旁白 | Narrador |
| special_appearance | 특별출연 | Special Appearance | 特别出演 | Aparición Especial |

---

## 사용법

### 배역 정보 표시
```html
<!-- 한국어 -->
<div class="cast-info">
  <h4>황정민</h4>
  <p class="role">주연</p>
  <p class="character">서도철 역</p>
</div>

<!-- 영어 -->
<div class="cast-info">
  <h4>Hwang Jung-min</h4>
  <p class="role">Lead Role</p>
  <p class="character">as Seo Do-cheol</p>
</div>
```

### 작품 목록 표시
```javascript
const getWorksByCategory = (category, language) => {
  return works
    .filter(work => work.category === category)
    .map(work => ({
      title: work.translations[language],
      year: work.year
    }));
};

// 뮤직비디오 목록 조회
const musicVideos = getWorksByCategory('music_video', 'ko');
```

### 배역 검색
```javascript
const findRoleTranslation = (roleId, language) => {
  const role = roles.find(r => r.id === roleId);
  return role ? role.translations[language] : roleId;
};

// 사용 예
const roleName = findRoleTranslation('music_store_clerk', 'es'); 
// 결과: "Empleado de Tienda de Música"
```