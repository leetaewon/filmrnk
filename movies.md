# 영화 제목 Glossary

> 외유내강 제작 영화 및 관련 작품의 다국어 제목 통일 가이드

## 업데이트 정보
- **최종 업데이트**: 2025-01-07
- **총 영화 수**: 37편

---

## 영화 목록

| ID | 한국어 | English | 中文简体 | Español | Year |
|---|---|---|---|---|---|
| devil_moved_in | 악마가 이사왔다 | The Devil Moved In | 恶魔搬来了 | El Diablo se Mudó | 2025 |
| veteran2 | 베테랑2 | I, The Executioner | 老手2 | Por encima de la ley 2 | 2024 |
| dr_cheon | 천박사 퇴마 연구소: 설경의 비밀 | Dr. Cheon And The Lost Talisman | 千博士驱魔研究所 | El Dr. Cheon y el Talismán Perdido | 2023 |
| smugglers | 밀수 | Smugglers | 走私 | Smugglers | 2023 |
| hostage | 인질 | Hostage: Missing Celebrity | 人质 | Hostage: Missing Celebrity | 2021 |
| mogadishu | 모가디슈 | Escape from Mogadishu | 摩加迪沙 | Huida de Mogadiscio | 2021 |
| startup | 시동 | Start-Up | 始动 | Start-Up | 2019 |
| exit | 엑시트 | EXIT | 极限逃生 | Exit: Escape de Seúl | 2019 |
| svaha | 사바하 | Svaha: The Sixth Finger | 娑婆诃 | Svaha: The Sixth Finger | 2019 |
| wedding_day | 너의 결혼식 | On Your Wedding Day | 你的婚礼 | El día de tu boda | 2018 |
| battleship_island | 군함도 | The Battleship Island | 军舰岛 | Battleship Island | 2017 |
| misbehavior | 여교사 | Misbehavior | 女教师 | Misbehavior | 2016 |
| veteran | 베테랑 | Veteran | 老手 | Por Encima De La Ley | 2015 |
| one_summer_night | 인생은 새옹지마 | One Summer Night | 人生如塞翁失马 | Una noche de verano | 2014 |
| mad_sad_bad | [신촌좀비만화] 유령 | Mad Sad Bad | 新村丧尸漫画 | Mad Sad Bad | 2014 |
| berlin_file | 베를린 | The Berlin File | 柏林 | The Berlin File | 2013 |
| unjust | 부당거래 | The Unjust | 不当交易 | The Unjust | 2010 |
| troubleshooter | 해결사 | Troubleshooter | 解决士 | Troubleshooter | 2010 |
| timeless | 타임리스 | Timeless | 时间租赁 | Timeless | 2009 |
| dachimawa_lee2 | 다찌마와 리 : 악인이여 지옥행 급행열차를 타라! | Dachimawa Lee | Dachimawa Lee : 恶人啊，乘上通往地狱的特快列车吧！ | Dachimawa Lee | 2008 |
| city_of_violence | 짝패 | The City of Violence | 暴力城市 | The City of Violence | 2006 |
| hey_man | [다섯개의 시선] 남자니까 아시잖아요? | Hey Man | [五个视角] 因为是男人，你懂的，对吧？ | Hey Man | 2006 |
| crying_fist | 주먹이 운다 | Crying Fist | 哭泣的拳头 | Crying Fist | 2005 |
| arahan | 아라한 장풍대작전 | Arahan | 阿罗汉掌风大作战 | Arahan | 2004 |
| no_blood_no_tears | 피도 눈물도 없이 | No Blood No Tears | 无血无泪 | No Blood No Tears | 2002 |
| dachimawa_lee | 다찌마와 리 | Dachimawa Lee | Dachimawa Lee | Dachimawa Lee | 2000 |
| die_bad | 죽거나 혹은 나쁘거나 | Die Bad | 没好死 | Die Bad | 2000 |
| transmutated_head | 변질헤드 | Transmutated Head | 变质头 | Transmutated Head | 1999 |
| gang_fight | 패싸움 | Gang Fight | 群殴 | Gang Fight | 1999 |
| modern_man | 현대인 | Modern Man | 现代人 | Modern Man | 1999 |
| trio | 3인조 | Trio | 三人组 | Trio | 1997 |
| sympathy_mr_vengeance | 복수는 나의 것 | Sympathy for Mr. Vengeance | 我要复仇 | Sympathy for Mr. Vengeance | 2002 |
| oasis | 오아시스 | Oasis | 绿洲 | Oasis | 2002 |
| lady_vengeance | 친절한 금자씨 | Lady Vengeance | 亲切的金子 | Sympathy for Lady Vengeance | 2005 |
| battlefield_heroes | 평양성 | Battlefield Heroes | 平壤城 | Battlefield Heroes | 2011 |
| mama | 마마 | Mama | Mama | Mama | 2022 |
| rough_play | 배우는 배우다 | Rough Play | 演员就是演员 | Rough Play | 2013 |
| gyeongju | 경주 | Gyeongju | 庆州 | Gyeongju | 2014 |

---

## 사용법

### 번역 규칙
1. **스페인어 번역이 없는 경우**: 영어 제목을 그대로 사용
2. **특수 기호**: 대괄호 `[]`, 콜론 `:` 등은 언어별 관례에 따라 조정
3. **고유명사**: 인명, 지명은 해당 언어권 표기법 준수

### API 사용 예시
```javascript
// 영화 ID로 다국어 제목 조회
const getMovieTitle = (movieId, language) => {
  // movies.json에서 해당 데이터 조회
  return movieTitles[movieId][language];
};

// 사용 예
getMovieTitle('veteran2', 'es'); // "Por encima de la ley 2"
```