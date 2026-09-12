# ARCHIVE 1025 - 교사용 기록 저장(Firebase) 설정

게임은 Firebase 없이도 정상 작동합니다. Firebase를 연결하면 게임 완료 시 학생의 결과가 Cloud Firestore의 `archive1025_results` 컬렉션에 자동 저장됩니다.

## 저장 항목
- 학년도, 학번, 난이도
- 실제 플레이 시간
- 힌트 횟수와 보정 시간
- 비교 기록(실제 시간 + 보정 시간)
- 각 방 소요 시간
- 사용한 힌트 종류
- 완료 시각

이름은 수집하지 않습니다.

## 기록 보정 규칙
- 일반 힌트 최초 사용: +30초
- 오브젝트 위치 표시 최초 사용: +45초
- 같은 힌트를 다시 눌러도 추가 보정 없음

## Firebase 설정
1. Firebase Console에서 프로젝트 생성
2. Web App 등록
3. Authentication > Sign-in method에서 Anonymous 활성화
4. Firestore Database 생성
5. Firestore > Rules에 `firestore.rules.txt` 내용 게시
6. Web App의 `firebaseConfig` 값을 `config/firebase-config.js`에 붙여넣기
7. `window.ARCHIVE_FIREBASE_ENABLED = true;`로 변경
8. GitHub 커밋 → Vercel 재배포
9. 테스트 1회 완료 → Firestore > Data > `archive1025_results` 확인

## 보안
학생 클라이언트는 결과를 create만 할 수 있고, 다른 결과를 read/update/delete할 수 없도록 규칙을 구성했습니다. 교사는 Firebase Console에서 확인합니다.

학번도 학교 내부에서는 개인식별정보가 될 수 있으므로 학교의 개인정보 처리 기준에 맞춰 보관 기간과 접근 권한을 설정하세요.
