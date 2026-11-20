# Vertical Shooter (S/W engineering proj 1)

화면 아래쪽 플레이어 비행기를 좌우로 움직이며 총알을 쏘아, 위에서 내려오는 적을 맞히는 종스크롤 슈팅 게임.

## 실행 방법

- Python 3.10–3.13, pygame 2.x
  - Python 3.14 에서는 pygame 2.6.1 이 설치되지 않으니, 3.10–3.13 중 하나를 사용할 것.

```bash
pip install pygame
python main.py
```

## 조작

| 키 | 동작 |
|---|---|
| ← / → | 좌우 이동 |
| Space | 시작 화면에서 게임 시작 / 게임 중 총알 발사 |
| R | 게임 오버 후 다시 시작 |
| Esc | 종료 (시작 화면에서도) |

## 파일 구성

| 파일 | 내용 |
|---|---|
| `main.py` | 게임 루프 — 입력 처리, 갱신, 그리기, 점수·생명·게임 오버 |
| `entities.py` | 그림 불러오기(`load_frame`), 배경(`Background`), 스프라이트 클래스 — `Player`, `Bullet`, `Enemy` |
| `settings.py` | 화면 크기·속도·색 같은 상수 |
| `assets/` | 그림 — ansimuz CC0 픽셀 아트 (출처: `assets/CREDITS.md`) |
| `AI_USAGE.md` | 생성형 AI 사용 기록 |

## 구현한 기능

- [x] F1 플레이어 이동 — ←/→ 를 누르는 동안 이동, 화면 좌우 끝 밖으로 나가지 않음
- [x] F2 총알 발사 — SPACE 로 플레이어 위쪽 가운데에서 발사, 화면 밖으로 나가면 제거
- [x] F3 적 명중과 점수 — 총알과 적이 함께 사라지고 적 하나당 10점, 왼쪽 위에 SCORE 표시
- [x] F4 피격과 게임 오버 — 적과 충돌하거나 놓치면 생명 -1, 0 이하면 GAME OVER 와 점수 표시
- [x] F5 재시작과 최고 점수 — R 로 재시작, highscore.txt 에 최고 점수 저장·표시
