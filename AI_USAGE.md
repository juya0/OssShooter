# 생성형 AI 사용 기록

이 과제에서 생성형 AI 를 사용한 내용을 아래 표에 기록합니다.

| 날짜 | 도구 | 관련 기능 | 무엇을 물었나 | 결과를 어떻게 반영/수정했나 |
|---|---|---|---|---|
| 2026-11-18 | Claude | F1 | 방향키를 누르는 동안 좌우로 움직이고 화면 끝 밖으로 나가지 않게 하는 Player.update 구현 | Claude 가 작성한 코드를 검토 후 사용. rect.left/right 비교로 경계를 제한하는 방식을 이해하고 반영 |
| 2026-11-18 | Claude | F2 | Bullet.update, Player.shoot, SPACE 발사 입력(게임 오버 중 제외) 구현 | Claude 가 작성한 코드를 사용. 화면 위로 완전히 나가면 kill() 하는 조건(rect.bottom < 0)을 확인하고 반영 |
| 2026-11-18 | Claude | F3 | groupcollide 로 총알·적 충돌 처리와 점수 가산, SCORE HUD 표시 구현 | Claude 가 작성한 코드를 사용. groupcollide 의 dokill 인자 두 개를 True 로 둔 이유를 확인 |
| 2026-11-18 | Claude | F4 | spritecollide 로 피격 처리, 아래로 지난 적 처리, 생명 0 이하일 때 end_game, GAME OVER 화면 구현 | Claude 가 작성한 코드를 사용. 생명이 음수로 표시되지 않도록 0 으로 고정하는 부분을 확인 |
| 2026-11-18 | Claude | F5 | highscore.txt 읽기·저장(예외 처리 포함), 최고 점수 갱신, R 키 재시작, 게임 오버 화면 표시 구현 | Claude 가 작성한 코드를 사용. 파일이 없거나 숫자가 아닐 때 0 을 반환하는지 확인 |
| 2026-11-18 | Claude | 기타 | README 구현 항목 목록, .gitignore, 브랜치·커밋 단위 계획 작성 도움 | Claude 의 초안을 바탕으로 사용. 커밋·브랜치·머지·push 는 직접 수행 |
