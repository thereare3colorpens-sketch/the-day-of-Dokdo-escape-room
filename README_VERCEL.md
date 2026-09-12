# ARCHIVE 1025 V16 — GitHub / Vercel 배포

이 폴더의 구조를 그대로 GitHub 저장소 루트에 올리면 됩니다.
Vercel에서는 Framework Preset을 `Other`로 두고 별도 Build Command 없이 정적 사이트로 배포하세요.

## 필수 구조
- index.html
- vercel.json
- assets/rooms/room01_closed.webp
- assets/rooms/room01_open.webp
- assets/rooms/room02_closed.webp
- assets/rooms/room02_open.webp
- assets/rooms/room03_closed.webp
- assets/rooms/room03_open.webp

## 역사 이미지 권장 파일명
- assets/history/dokdo_map_ko.png
- assets/history/taejeonggwan.png
- assets/history/decree41.jpg

로컬 역사 이미지가 없으면 HTTPS/Vercel 환경에서는 Wikimedia Commons 원본을 마지막 fallback으로 시도합니다.
학교 행사에서는 안정성을 위해 세 역사 이미지도 저장소에 직접 넣는 것을 권장합니다.

## V16 플레이 난이도 차이
- 입문자: CASE 02에서 숫자/선 보조가 보이고, FINAL CASE 6개 장치 중 3개만 작동합니다.
- 도전자: CASE 02 침입자 메모에 숫자가 보이지 않으며, 입력 시 화살표 기록만 표시됩니다. FINAL CASE 6개 장치를 모두 조작합니다.

## 수정 시 주의
- 방 배경 파일명은 유지하는 것이 가장 안전합니다.
- 방 배경은 1600×893 또는 동일 비율을 권장합니다.
- 핫스팟 좌표는 현재 배경 6장에 맞춰 세밀하게 조정되어 있습니다.
