메나리니 인터페이스에 사용되는 RPA 툴인 a.works의 test에 대해 간략히 정리합니다.(까먹을 때 대비)


시작하기 전 Open Browser에서 구글 창이 열리지 않을 때

Win + R  →  chrome.exe --profile-directory="Default"  →  엔터
→ a.works에서 파일 → 설정 → 확장기능 → 크롬 확장팩 설치



작업 흐름(불필요한 행위가 있지만 연습을 위해 넣어둔 부분이 있습니다.)

1. 해당 날짜의 폴더를 만듬

2. 95번 서버의 특정 폴더의 특정 파일을 열음

3. 특정 내용을 더블 클릭 및 전체 선택 및 복사

4. 로컬 피씨에서 엑셀 열음

5. 내용 복붙 및 해당 날짜 폴더에 저장

6. 해당 폴더 압축

7. 메일 전송

8. 압축해제









1. 해당 날짜의 폴더를 만듬
<img width="239" height="163" alt="32b98473-560d-4b81-a9e7-f4074245eb30" src="https://github.com/user-attachments/assets/9d2a02aa-8a73-4d89-a850-7c366743dc39" />
<img width="914" height="38" alt="6ee2303b-fd0e-45d0-b81b-8d19c4dcef83" src="https://github.com/user-attachments/assets/6cc5197d-975a-4400-a239-262c7a0bc7b8" />

변수 생성
<img width="503" height="504" alt="f85baf9c-be98-4c8d-9bed-b2c1a0013a42" src="https://github.com/user-attachments/assets/f3b36c29-b6dd-42df-bbde-6a1356e17250" />
Get Date를 사용해서 오늘 날짜를 변수에 할당
<img width="490" height="479" alt="78c78a02-fb1a-4341-910f-c82816ceb7e6" src="https://github.com/user-attachments/assets/4952e776-a9b5-48b4-be97-f21918840732" />
Create Directory를 사용하여 특정 경로에 하위 폴더 생성

2. 95번 서버의 특정 폴더의 특정 파일을 열음
<img width="248" height="338" alt="e9cd79f7-d4f9-4657-b67d-3fb6543dc165" src="https://github.com/user-attachments/assets/7ad119cf-dfe6-4f9e-a59a-67e3c779adf9" />
<img width="649" height="916" alt="c644d5a3-ffa8-4e92-8b2b-775e56992290" src="https://github.com/user-attachments/assets/811c4a05-0a1c-4a7e-b052-0e12e6a4b65f" />
Image Click을 사용하여 특정 폴더 클릭.
가상환경에서는 Object Click 사용이 불가하여 이미지로 클릭.
Scale Invariant를 체크하면 어느정도 해상도 차이를 극복
Click Active를 DoubleClick으로 줌

<img width="655" height="902" alt="f700fd9e-9cbd-44a1-b4e9-132f818fd36e" src="https://github.com/user-attachments/assets/71683c7a-fc64-4067-b266-cfd1a221faa6" />
특정 파일을 열 때도 같은 방식으로 열음


3. 특정 내용을 더블 클릭 및 전체 선택 및 복사
<img width="654" height="937" alt="60fb1b52-72e3-4bf7-b912-35d731991d92" src="https://github.com/user-attachments/assets/f59f3e3b-3ae3-41e5-b9a9-adb0a4652ad5" />
파일 내부에서 특정 텍스트가 잘 눌리는 지 확인

<img width="646" height="758" alt="714f23d5-a7b8-4607-a404-4c552d989558" src="https://github.com/user-attachments/assets/9ce64308-f382-4133-ab4d-df9d24857111" />
Key Input을 사용하여 단축키로 전체선택 및 복사

4. 로컬 피씨에서 엑셀 열음
<img width="241" height="257" alt="f849ad03-7735-4df7-89c7-f354a7baa88f" src="https://github.com/user-attachments/assets/20ab7227-3079-4c10-97bc-1d603aba018f" />
<img width="647" height="917" alt="e99e9b02-9a4d-49b1-b456-67033413e297" src="https://github.com/user-attachments/assets/bd1421e2-0fe0-4dc6-9a67-2d8e9ee1f33a" />
Image Click을 사용하여 로컬 피씨의 검색을 클릭.
로컬피씨 하단 툴바는 Object Click이 안 돼서 Image Click으로 클릭.

<img width="671" height="658" alt="51221633-b3f9-4682-85a0-863befa29acf" src="https://github.com/user-attachments/assets/648e6111-d11e-4eec-8bfc-030ae545b095" />
Key Input을 사용하여 엑셀앱 검색 및 열기

<img width="677" height="933" alt="7bb042bc-1a44-4a1c-a0e3-dea57c7bfbe9" src="https://github.com/user-attachments/assets/fa3d6e69-ae7f-4daf-b77a-ec9fecfeea1b" />
로컬피씨에서는 Object Click 사용이 가능하기 때문에
해당 기능으로 새 통합 문서 열기


5. 내용 복붙 및 해당 날짜 폴더에 저장
<img width="245" height="668" alt="e18f5c4d-66cc-4d1e-bea0-87f337392fe7" src="https://github.com/user-attachments/assets/4c5daad0-0879-4aad-a73f-e7104ffde683" />
<img width="492" height="291" alt="9bcba71f-2910-4d97-8478-f2924aed3efc" src="https://github.com/user-attachments/assets/918457f8-4c45-4656-91ec-f124740ce3b9" />

<img width="669" height="677" alt="59ccd07a-cc45-4c51-8f75-fbb7261833c3" src="https://github.com/user-attachments/assets/c63372bc-2041-4ddd-baaa-d21861022a75" />
key Input을 사용해서 복사했던 내용 시트에 붙여넣기

<img width="671" height="606" alt="a173d14d-264f-42be-a8a7-6d0fa62992a7" src="https://github.com/user-attachments/assets/6a885736-1a42-4862-8694-11930a362db0" />
key Input을 사용해서 저장

<img width="802" height="27" alt="5335acc8-db31-4ff7-a783-739786bd3ecb" src="https://github.com/user-attachments/assets/a7896c7e-c7d1-4428-b1e0-a30085b15c21" />
<img width="673" height="533" alt="65267b7a-cbc4-4b62-9412-fc9761ec492f" src="https://github.com/user-attachments/assets/af7d6ae9-832d-4bab-8f7e-1bbd9db669c3" />
Assign을 사용하여 특정 폴더에 오늘 날짜 경로를 새로운 변수에 할당

Object Click을 사용하여 저장시 경로 찾아보기 클릭

Key Input을 사용하여 오늘의 파일 경로 입력.
다만 저장 팝업창의 초기 모습이 다를 수도 있음으로 
Selector에 들어가 제일 마지막 부분의 체크를 해제

Selector에서 문서로 지정된 부분을 해제하면 다른 경로가 기본이어도 클릭을 한다.

Key Input을 사용하여 엔터. 해당 경로로 이동된다.

Object Click을 사용하여 저장버튼 클릭



예외 처리를 위한 아이템.
만약 같은 이름의 파일을 저장하려고 한다면
다른 이름으로 저장 확인 팝업이 뜨는데
Object Match를 사용하면 해당 팝업이 있는지 없는지만 확인해서
boolean 변수에 참 거짓 값을 넣어준다.

If 아이템을 사용. Condition에 boolean 변수를 넣어주면 참일 때와 거짓일 때의 행동을
정해줄 수 있다



Object Click을 사용하여 
참일시 같은 파일이 존재했다는 뜻이기에, 덮어쓰기로 결정

거짓이라면 새로운 파일의 저장이기에 그냥 If문을 나간다

엑셀이 열려있으면 압축이 안돼서
Kill Process를 사용해 엑셀을 닫음.(Click Object로 닫으면 인식이 안됨.
Image Click도 좋지만 이 부분이 더 확실해 보임)



6. 해당 폴더 압축

Zip 아이템을 사용하여 Source Path의 폴더를
Destination Path에 압축하여
File Name으로 저장한다.
Choice Type을 Directory로 설정해야 해당 폴더 자체를 압축한다.
확장자가 .zip이 아니지만 압축 풀기 아이템으로
잘 풀리니 신경은 쓰지 않아도 된다



7. 메일 전송



Assign을 사용해 압축 후 생성 될 압축파일의 경로를 새 변수에 할당한다.

Send Mail 아이템을 사용하여 
메일을 세팅하고, 수신인 및 내용을 정해줍니다.
Attach File에 첨부 파일의 경로를 넣어줍니다.



8. 압축해제



Unzip을 사용하여 압축을 해제합니다.
Source Path에 압축 파일 경로를 넣어주고,
Destination Path에 압축을 해제 할 경로를 넣어줍니다.

