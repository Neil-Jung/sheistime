# 쉬는시간 오락실

쉬는 시간에 한 판씩 하기 좋은 브라우저 게임 모음이에요. 폰(터치)과 컴퓨터(키보드·마우스) 모두 지원해요.

| 게임 | 장르 | 폴더 |
| --- | --- | --- |
| 은하 합치기 | 물리 합치기 퍼즐 (수박게임 스타일) | `games/merge/` |
| 산성비 | 한글 타자 게임 | `games/typing/` |
| 조각보 | 블록 퍼즐 (블록블라스트 스타일) | `games/blocks/` |
| 기말고사 생존기 | 생존 액션 (뱀서라이크) | `games/survivor/` |
| 장단 | 4키 리듬 게임 (국악 비트) | `games/rhythm/` |

## 구조

- `index.html`: 게임 목록 페이지
- `games/<게임>/index.html`: 게임 하나가 HTML 파일 하나에 모두 들어 있어요. 그림은 캔버스로 그리고 소리는 Web Audio로 합성해서 이미지·음악 파일이 없어요.
- `assets/thumbs/`: 목록 페이지에 쓰는 게임 화면 미리보기

빌드 과정이 없는 정적 사이트예요. 외부에서 불러오는 건 Google Fonts와 은하 합치기의 물리 엔진(matter.js, cdnjs)뿐이에요.

## 로컬에서 실행

```bash
npx serve .
```

브라우저에서 `http://localhost:3000`을 열면 돼요.

## Vercel 배포

Vercel에서 이 저장소를 가져오고 Framework Preset을 **Other**로 두면 돼요. 빌드 명령과 출력 폴더는 비워 두세요.

## 최고 기록

최고 기록과 설정은 브라우저 localStorage에 `arcade.<게임>.` 키로 저장돼서 그 기기에서만 보여요.
