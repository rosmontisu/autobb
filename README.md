# 메모장    
훈련소땜에 만들어둔거   
!!! 연동버젼 프라이빗으로 다시 만드는즁 !!!

https://mkblog.co.kr/android-adb-input-command/
adb shell input 커맨드 참조한 곳

## 오토 작동 방식
1. adb client device 객체 생성
2. 현재 에뮬레이터의 스크린을 캡쳐
   - adb shell screencap 방식
   - win32api 로 핸들 가져오는 방식(후킹)
3. cv/ocr로 스크린에서 탐색 후 좌표 추출
4. 만들어둔 루틴 확인
5. 루틴에 맞는 좌표로 adb를 통해 입력(클릭)
   - adb touch 
   - android miniTouch 

## 기타 구현 아이디어
1. 카페에서 애들 어떻게 찾을거임?   
   - 선물 선택 상태에서 말풍선 찾기
   - 처음 입장시 뜨는 방문 학생 목록으로 sd대조해서 찾기
   - 처음에 뜨는 특유의 연출로 좌표 서치
정도 생각하는중

2. 업무 태우는건 뭐로?
   - 진행중인 이벤트랑 동기화 시켜서 ap를 태우는 방식으로 생각중
   - 스케쥴 관련 api 있으면 그걸로 긁어와서 루틴 수정하는 방식
   - 없으면..

3. 주요 라이브러리
   - ppadb
   - openCV
   - pyautogui
   - PPOCR, easyOcr
  
## 고려중, 구현중 
- wpf환경인 vpet과 결합 -> openai 키 발급받은거랑 vpet에 정상적으로 연결됨
- 웹은 구글 centos7 클라우드로 돌리는 중. (전에 아파치로 열어두던거)
- 디스코드 봇은 글리치로 하나 열어둠
- ai보이스로 디코봇에 보이스 넣는건 안되려나? 시리같은 느낌으로?
