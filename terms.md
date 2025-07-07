# 기본 용어 Glossary

> 영화 정보 표시에 사용되는 기본 용어의 다국어 통일 가이드

## 업데이트 정보
- **최종 업데이트**: 2025-01-07
- **총 용어 수**: 25개

---

## 영화 정보 표시 용어

| Category | 한국어 | English | 中文简体 | Español |
|---|---|---|---|---|
| basic | 제목 | Title | 标题 | Título |
| basic | 감독 | Director | 导演 | Director |
| basic | 출연 | Starring | 主演 | Protagonista |
| basic | 각본 | Writers | 编剧 | Guionistas |
| basic | 제작 | Producer | 制片人 | Productor |
| basic | 상영시간 | Running Time | 时长 | Duración |
| basic | 개봉 | Release Date | 上映日期 | Fecha de estreno |
| basic | 등급 | Rating | 评级 | Clasificación |
| basic | 장르 | Genre | 类型 | Género |
| basic | 년도 | Year | 年 | Año |
| basic | 분 | minutes | 分钟 | minutos |

## 제작진 역할 용어

| Category | 한국어 | English | 中文简体 | Español |
|---|---|---|---|---|
| crew | 감독 | Director | 导演 | Director |
| crew | 각본 | Screenplay | 编剧 | Guión |
| crew | 제작 | Producer | 制片人 | Productor |
| crew | 촬영 | Cinematography | 摄影 | Cinematografía |
| crew | 편집 | Editing | 剪辑 | Montaje |
| crew | 음악 | Music | 音乐 | Música |
| crew | 미술 | Production Design | 美术 | Diseño de Producción |
| crew | 조명 | Lighting | 灯光 | Iluminación |
| crew | 의상 | Costume Design | 服装设计 | Diseño de Vestuario |
| crew | 분장 | Makeup | 化妆 | Maquillaje |
| crew | 특수효과 | Special Effects | 特效 | Efectos Especiales |
| crew | 시각효과 | Visual Effects | 视觉效果 | Efectos Visuales |
| crew | 무술 | Action Director | 动作指导 | Director de Acción |
| crew | 스턴트 | Stunt Coordinator | 特技协调员 | Coordinador de Dobles |

---

## 사용법

### 웹사이트 표시 예시
```html
<!-- 한국어 -->
<div class="movie-info">
  <h3>감독</h3>
  <p>류승완</p>
  <h3>상영시간</h3>
  <p>120분</p>
</div>

<!-- 영어 -->
<div class="movie-info">
  <h3>Director</h3>
  <p>Ryoo Seung-wan</p>
  <h3>Running Time</h3>
  <p>120 minutes</p>
</div>
```

### JSON API 구조
```json
{
  "movieInfo": {
    "ko": {
      "director": "감독",
      "runningTime": "상영시간",
      "minutes": "분"
    },
    "en": {
      "director": "Director", 
      "runningTime": "Running Time",
      "minutes": "minutes"
    }
  }
}
```