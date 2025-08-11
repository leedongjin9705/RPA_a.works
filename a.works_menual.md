인터페이스에 사용되는 RPA 툴인 a.works의 test에 대해 간략히 정리합니다.(까먹을 때 대비)

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

<img width="637" height="757" alt="96d2607f-667d-420c-b071-77462d595a4c" src="https://github.com/user-attachments/assets/55755f17-c792-445d-a9e5-8588d847f76c" />

Object Click을 사용하여 저장시 경로 찾아보기 클릭

<img width="655" height="688" alt="8d80d7be-f5b5-4de8-aa0e-a2f31a674695" src="https://github.com/user-attachments/assets/8b0f1449-9b3d-4bb5-ae40-701bef5eae44" />

Key Input을 사용하여 오늘의 파일 경로 입력.
다만 저장 팝업창의 초기 모습이 다를 수도 있음으로 
Selector에 들어가 제일 마지막 부분의 체크를 해제

<img width="628" height="648" alt="cd7c648a-caa9-46db-8d20-8f99f8a2577a" src="https://github.com/user-attachments/assets/af34354f-ae65-43a4-8927-a42a45cf1501" />

Selector에서 문서로 지정된 부분을 해제하면 다른 경로가 기본이어도 클릭을 한다.

<img width="661" height="609" alt="fb28724b-0fd4-47d7-bad4-5088d4bffadc" src="https://github.com/user-attachments/assets/35c4263b-a1ec-4cf2-92e4-d629ebb7ee40" />

Key Input을 사용하여 엔터. 해당 경로로 이동된다.

<img width="662" height="629" alt="a0e1ddd9-093e-4c8d-ae05-f247c6c9228e" src="https://github.com/user-attachments/assets/aa9f7f21-c97f-47ff-96bc-5dbdd767312e" />

Object Click을 사용하여 저장버튼 클릭

<img width="792" height="37" alt="1d9968bf-c4ea-4851-889f-e4f4730bfdff" src="https://github.com/user-attachments/assets/61ecc298-6639-412d-9db0-299fc0157d59" />

<img width="642" height="625" alt="6e12a9d7-e49c-412e-a54d-d106b3675e9c" src="https://github.com/user-attachments/assets/742342f9-0bdf-4f4a-a88a-8af316acf949" />

예외 처리를 위한 아이템.
만약 같은 이름의 파일을 저장하려고 한다면
다른 이름으로 저장 확인 팝업이 뜨는데
Object Match를 사용하면 해당 팝업이 있는지 없는지만 확인해서
boolean 변수에 참 거짓 값을 넣어준다.

<img width="632" height="330" alt="dc17dc5d-42bb-4e06-9740-9cd0950218f5" src="https://github.com/user-attachments/assets/68d8767b-e5a1-4daf-9d34-2e9f41cb7313" />

If 아이템을 사용. Condition에 boolean 변수를 넣어주면 참일 때와 거짓일 때의 행동을
정해줄 수 있다

<img width="470" height="189" alt="1dd53ec0-73d1-4c96-b3b8-e194591ab45f" src="https://github.com/user-attachments/assets/f4758d05-cf70-42b0-a9b0-327d7e8d17cb" />
<img width="653" height="705" alt="76e47f2c-6aa3-405e-b4a8-c0f00ebe2bc6" src="https://github.com/user-attachments/assets/4474d7ee-9819-4b56-98c1-fbe16840ee50" />=

Object Click을 사용하여 
참일시 같은 파일이 존재했다는 뜻이기에, 덮어쓰기로 결정

<img width="673" height="313" alt="868735bf-3b06-4bd7-a70f-c07c84408f5a" src="https://github.com/user-attachments/assets/d9827dbd-7395-4827-940c-6d79f39519d1" />

거짓이라면 새로운 파일의 저장이기에 그냥 If문을 나간다

<img width="638" height="492" alt="7aa3ec82-93c0-4d69-baf6-2331b6570ca8" src="https://github.com/user-attachments/assets/04cc89f0-6462-4fda-b632-6f1c083099c3" />

엑셀이 열려있으면 압축이 안돼서
Kill Process를 사용해 엑셀을 닫음.(Click Object로 닫으면 인식이 안됨.
Image Click도 좋지만 이 부분이 더 확실해 보임)



6. 해당 폴더 압축
   
<img width="214" height="88" alt="4daa88a5-59e3-4809-9313-b4634675bd0e" src="https://github.com/user-attachments/assets/efade4e1-5d19-4744-b3ea-69f7b19a9561" />

<img width="656" height="597" alt="96cc9adf-b082-4ba8-910e-a44ec893b242" src="https://github.com/user-attachments/assets/0607a102-bd61-4caa-9e92-ec81b65edbed" />

Zip 아이템을 사용하여 Source Path의 폴더를
Destination Path에 압축하여
File Name으로 저장한다.
Choice Type을 Directory로 설정해야 해당 폴더 자체를 압축한다.
확장자가 .zip이 아니지만 압축 풀기 아이템으로
잘 풀리니 신경은 쓰지 않아도 된다



7. 메일 전송
   
<img width="221" height="158" alt="d930a4f6-d4c3-4e79-8f37-34e6769b944f" src="https://github.com/user-attachments/assets/16715c6c-1cb4-4cfe-b452-83940b42d82d" />

<img width="776" height="22" alt="1edf214f-3736-427f-b0ac-ae477747dd2f" src="https://github.com/user-attachments/assets/e214dcc4-7dc8-4319-ad57-6d11b694047b" />

<img width="631" height="504" alt="4c7cf36b-3a01-42a3-869d-7f3d4cc07b10" src="https://github.com/user-attachments/assets/f2d32f96-df00-42f8-91c6-229de95e2c40" />

Assign을 사용해 압축 후 생성 될 압축파일의 경로를 새 변수에 할당한다.

<img width="649" height="874" alt="67b9389b-5854-42e4-bfaa-49ad2531419b" src="https://github.com/user-attachments/assets/8cd0a0fa-9679-4414-83c9-459435756007" />

Send Mail 아이템을 사용하여 
메일을 세팅하고, 수신인 및 내용을 정해줍니다.
Attach File에 첨부 파일의 경로를 넣어줍니다.



8. 압축해제

<img width="223" height="82" alt="62f231d8-ec76-4264-a6d2-62aa50512a8b" src="https://github.com/user-attachments/assets/8cd38a1e-ec0e-4c59-8575-132805398dbb" />

<img width="645" height="533" alt="cc26d2aa-97aa-4a34-b852-cf870daa1429" src="https://github.com/user-attachments/assets/9b0f4afd-c423-41de-bafe-cac1905d205e" />

Unzip을 사용하여 압축을 해제합니다.
Source Path에 압축 파일 경로를 넣어주고,
Destination Path에 압축을 해제 할 경로를 넣어줍니다.

