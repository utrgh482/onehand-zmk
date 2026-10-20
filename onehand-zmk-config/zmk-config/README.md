# 한손 키보드 1호 — ZMK 펌웨어 설정

## 올리는 법
1. 이 폴더 내용을 GitHub 저장소(공개, public)에 그대로 올립니다.
2. 저장소의 Actions 탭에서 빌드가 끝나기를 기다립니다 (처음은 5~10분).
3. 완료된 빌드를 열어 맨 아래 Artifacts의 `firmware`를 내려받아 압축을 풉니다.
4. 컨트롤러를 USB로 연결하고 리셋 버튼을 빠르게 두 번 누르면 `NICENANO` 드라이브가 뜹니다.
5. `onehand-nice_nano_v2-zmk.uf2` 파일을 그 드라이브에 복사합니다. 자동으로 재시작됩니다.

## 키 배치 바꾸기
- 간단한 변경: ZMK Studio (https://zmk.studio) 에 USB로 연결해 바로 바꿉니다. 기능층의 Tab 자리(`&studio_unlock`)를 눌러 잠금을 풀어야 합니다.
- 영구 변경: `config/onehand.keymap`을 고쳐 올리면 다시 빌드됩니다.

## 블루투스
- 기능층(둘째+숫자 동시에 누른 채) 줄0: 왼쪽부터 연결 전체 지우기, 기기 1, 기기 2, 기기 3, USB/블루투스 전환
- 처음 연결: 기기 1을 선택한 뒤 컴퓨터의 블루투스 설정에서 `OneHand`를 찾아 연결

## 문제가 생기면
- `settings_reset-nice_nano_v2-zmk.uf2`를 먼저 올렸다가 다시 `onehand` 펌웨어를 올리면 저장된 설정이 초기화됩니다.
