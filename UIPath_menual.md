목차

홈페이지 열기

페이지 로그인

팝업 닫기

특정 게시글 클릭

당일 날짜로 폴더 생성 후 파일 다운

당일 날짜 폴더의 모든 파일을 첨부한 뒤 outlook을 통한 메일 전송



1. 홈페이지 열기

UIPath 새로운 프로젝트 생성 후

ctrl + f 클릭하여 Use Application/Browser 액티비티 검색.

브라우저 URL에 산쿄 URL을 넣어주시면 됩니다.

<img width="570" height="183" alt="32ff1319-5dd3-4f62-8b01-bda38533826b" src="https://github.com/user-attachments/assets/4db46ee0-61eb-42f7-88da-6cceac67140a" />

이후 로그인 구현시 많은 팝업창이 뜨기 때문에 방지하기 위해 아래처럼 설정하여

시크릿 창을 열도록 설정했습니다.

<img width="544" height="621" alt="9d55de1d-11cb-48bc-a6ce-ffc124c83010" src="https://github.com/user-attachments/assets/65c73e92-13ba-47c8-9d37-04d41fbcaf8f" />

프로그램 왼쪽 상단을 보면 실행 버튼이 있는데, 실행 후 페이지가 잘 열리는 지 봅니다.

처음에는 안될텐데 깔라는 확장 프로그램 깔아주고, 

chrome://extensions 을 검색하여 UIPath 관련 확장성은 시크릿 모드에서도 사용 가능하게 설정 변경해줍니다.

<img width="222" height="155" alt="153a1c23-c29c-476c-a8ac-0c8a6f484ae6" src="https://github.com/user-attachments/assets/58a0ad22-c293-4cd3-92d4-d3612e513441" />

2. 페이지 로그인

위의 액티비티를 보면 내부에 +버튼이 있습니다.

+를 누른 후 Type Into 액티비티를 추가해 줍니다.

생성되면 위에 “표시할 애플리케이션“이라고 쓰여있는데 클릭하고

산쿄 처음 화면에서 아이디 옆 요소를 클릭해주면 자동으로 설정됩니다.

다음 입력에는 본인이 아이디 창에 뭘 입력할 지 “로 감싸서 적어주시면 됩니다.(변수는 다음 비밀번호에서 보여드릴게요)

<img width="341" height="229" alt="76212397-9ba8-4d90-996d-c76a1ec35b68" src="https://github.com/user-attachments/assets/17213715-a854-40d4-80b5-081ba270809a" />

다음은 비밀번호 입력인데요. 다른 부분은 같지만 

“다음 입력”에 password라고 적혀있습니다.

이건 “비밀번호“을 값으로 가지는 변수입니다.

<img width="357" height="236" alt="55f92a0b-5850-4cfa-ac74-389cf8f918ce" src="https://github.com/user-attachments/assets/c9c75989-7a93-4d31-93d3-09db86fc56c8" />

프로그램의 중간 하단을 봐주세요

아래의 빨간 네모에서 변수를 생성해서 데이터 형식, 변수의 사용 범위, 기본값을 설정할 수 있습니다.

이 변수를 사용해서 비밀번호 등의 입력도 가능합니다

마지막으로 click 액티비티 생성 후 로그인 요소를 클릭하게 지정해주면 끝입니다.

<img width="367" height="178" alt="c5be2b57-dd6b-4e33-821f-0c6954e001f9" src="https://github.com/user-attachments/assets/93fc0373-51b4-4ab0-9c1a-62a783fcd189" />

3. 팝업 닫기

click 액티비티를 사용해서 닫기를 눌러주시면 됩니다.

닫기 위에 1주일간 안보기 체크박스가 있는데요.

누르면 좋은거 아니야? 하실수 있지만

UIPath는 돌다가 특정 요소를 발견하지 못하면 멈춰버립니다..(물론 if 문으로 분개하거나,

오류가 나면 다음 작업으로 넘기는 설정이 있으나 오늘은 쓰지 않습니다,,)

그래서  닫기만 설정해줬습니다.

<img width="354" height="175" alt="bc0e6929-3b91-4eef-b856-eb4f0ce9746a" src="https://github.com/user-attachments/assets/be4b1cb2-03f9-4b35-bbaf-311771013d0c" />

4. 특정 게시글 클릭

이것도 마찬가지로 click 액티비티를 사용하여 다운받을 게시글을 눌러주시면 됩니다.

<img width="392" height="181" alt="001ab584-eea9-4004-85ce-fcd1959059f5" src="https://github.com/user-attachments/assets/6233e003-baae-4e4a-8510-25254cace51c" />

5. 당일 날짜로 폴더 생성 후 파일 다운

저는 특정 폴더에 당일 날짜 폴더를 만든 뒤 그곳에 파일을 저장하려고 합니다.

다음은 Invoke Method 액티비티를 추가해줍니다. 

이 액티비티로 당일 날짜 폴더를 생성할 예정입니다!

설정은 아래처럼 해주시고, todayFilePath는 변수입니다!

아래의 값을 가지고 있는데 RPA File 폴더에 오늘 날짜 폴더를 뜻합니다.

<img width="297" height="27" alt="7862324c-5b5f-47f6-8587-8853d8d6d492" src="https://github.com/user-attachments/assets/52bb4043-9aa0-47dd-800a-aad9e421d516" />

<img width="1024" height="413" alt="0eea0364-3534-405e-8c81-07630bfa2d08" src="https://github.com/user-attachments/assets/3049713a-e20f-477c-b6ed-bd24d5b23770" />

click 액티비티를 사용해 파일 다운을 클릭

<img width="354" height="161" alt="7f82bf9b-69c7-4416-8a3f-dc6b9fd4574d" src="https://github.com/user-attachments/assets/22241a70-f78c-42bf-b88e-ce661c35fc17" />

Type Into 액티비티를 사용하여 아까 변수라고 말씀드린 todayFilePath를 

파일 저장 주소에 입력.

참고로 아래 사진의 상단을 보시면 길쭉한 돋보기 모양이 있는데,

타겟 설정시 나오며, 특정 요소에서도 특정 부분을 클릭하게 해줍니다.

주소창의 글씨를 클릭하면 루틴이 잘라져서 오른쪽 끝을 누르게 해뒀습니다. 

<img width="354" height="259" alt="0048312e-c92d-4066-ad8c-52a28af5b9f7" src="https://github.com/user-attachments/assets/28f379f1-25d2-41de-ba47-288d96d24ed4" />

이후 파일 경로로 이동하게 click 이벤트로 설정

이 작업을 할 때 저 화살표가 보이지 않을텐데, 주소를 입력해야 화살 모양이 나옵니다.

그래도 한 번 더 막히실텐데 F2를 눌러보시면 해결됩니다. 잠시 설정을 중단하는 단축키입니다.

<img width="394" height="134" alt="50017c4a-cce6-42e6-b6fe-bb6209a280c1" src="https://github.com/user-attachments/assets/55014932-e9ab-4ae8-adb7-84598a2ed369" />

마지막으로 Wait for Download 액티비티를 추가합니다.

안에 click 액티비티로 저장 버튼을 누르도록 설정했습니다.

Wait for Download 액티비티는 파일이 다운로드 됐는지 확인 후 다운로드 완료시에만

다음 작업으로 넘어가게 해줍니다.

저는 이 작업이 마지막 작업인데, 따로 설정하지 않으면 창이 닫히게 됩니다.

다운로드중 창이 닫히지 않게 추가해준 액티비티입니다.

모니터링된 폴더에 오늘 파일의 경로 변수를 넣으면 

해당 폴더를 확인하고, 폴더가 쓰기중이 아니고 사이즈 변화가 없으면

다운로드 완료됐다고 보고 다음 작업으로 넘어갑니다. 

“다운로드된 파일” 항목은 비워두셔도 됩니다.

<img width="518" height="477" alt="e9431906-36d0-4179-b7da-5e77677d96bb" src="https://github.com/user-attachments/assets/921ab490-097b-408c-8b3f-6821cf91b7be" />

5. 당일 날짜 폴더의 모든 파일을 첨부한 뒤 outlook을 통한 메일 전송

Assign 액티비티를 추가해줍니다.

이 액티비티는 fileToSend에 값을 할당(Directory.GetFiles(todayFilePath))해줍니다.

(fileToSend는 스트링 배열이고, 아래에 첨부했습니다. UIPath는 복붙이 안됩니다..)

Q. 여기서 의문 fileToSend 변수를 생성할 때때 왜 직접 “저장할 값“을 넣으면 안될까?

A. UIPath는 실행전에 변수를 먼저 검사합니다. 여기서 todayFilePath는 변수인데

위의 과정에에서 당일 날짜로 폴더를 생성하지 않으면  todayFilePath가 없어서 오류가 나버립니다. 

실행 자체가 안됩니다.

그래서 따로 Assign 액티비티를 사용하여 파일 생성 과정 이후 값을 할당합니다.

<img width="421" height="110" alt="42942e74-1589-46ff-b2ed-f6a9f1097326" src="https://github.com/user-attachments/assets/e1cbaa45-3845-43cc-8f38-8b9e7eeccb50" />

<img width="1024" height="38" alt="c386c4db-046f-4193-aaf9-96e07029ebce" src="https://github.com/user-attachments/assets/49f8ae0d-1b29-45ad-8182-a32fe90989b0" />

마지막으로 Send Outlook Desktop Mail Message 액티비티를 추가해줍니다.

받는사람, 제목, 본문을 “로 감싸서 적어주시면 됩니다.

<img width="351" height="219" alt="8f7c4969-e7f0-463c-9b66-3592c9773156" src="https://github.com/user-attachments/assets/ecf99b05-411c-4590-9cfa-0d728bdb60e9" />

이후 Assign 액티비티로 값을 받은 fileToSend를 “파일 경로 첨부 파일 컬렉션”에 넣어주시면 됩니다.

이렇게 하면 해당 폴더 경로의 모든 파일을 첨부하여 받는 사람에게 보내게 됩니다.

<img width="1024" height="666" alt="1633c396-51f6-45db-b66c-ace55e1b8f36" src="https://github.com/user-attachments/assets/3654f265-3f64-4a2c-9e03-3ca306d6f58a" />

끝
