UIPath, a.works와 달리 윈도우를 사용중이라면 PAD(Power Automate Desktop)가 이미 설치되어 있습니다.

해당 툴의 사용법을 익혀두면 반복 작업에서 쓰임새가 많으니 알아두시면 좋을 것 같습니다!

 
상황 : 특정 시간까지 화면 꺼짐을 방지하다가 if문 작업 수행. 

전체 작업 미리보기
 
<img width="683" height="126" alt="4f463489-<img width="646" height="402" alt="6741afcd-b559-421b-afee-d2c409093d0e" src="https://github.com/user-attachments/assets/44945285-95b7-4612-ac84-0390d4d16821" />
7e66-430a-8d91-3aee774da68f" src="https://github.com/user-attachments/assets/bccac79b-f0c0-48a1-bcab-15aae157a215" />

현재 시간을 가져와 FormattedDateTime에 특정 형식으로 수정해 저장해줍니다.
 
 <img width="648" height="318" alt="727afab4-b99a-4df6-9058-3a1d4c6735f4" src="https://github.com/user-attachments/assets/c7fa7145-0eb4-4bbd-9a3a-fe3720b0f137" />

반복 조건을 1=1로 주면 직접 or 간접적으로 작업을 종료하기 전까지 무한 반복됩니다.

<img width="642" height="365" alt="a77b7258-db63-4b30-ba30-82d71021636d" src="https://github.com/user-attachments/assets/cc0d803e-cc1f-4fdf-88b5-65a2270f2a46" />

현재 시간이 두 번째 피연산자와 같으면 if문 안의 작업이 실행됩니다.

<img width="647" height="496" alt="cfb0e756-1185-4770-ba4c-b3b214bba853" src="https://github.com/user-attachments/assets/bc540a5f-a1df-4743-a459-eda188d46f1c" />

if문 안의 작업은 “블록 오류 시“ 로 감싸져 있는데, 위처럼 설정시 
블록 안의 어떤 작업에서 에러가 발생하면 “블록 오류시“ 안에 작업을 뛰어 넘고
(아래 사진에서 계속 설명)

<img width="1061" height="140" alt="923cd78a-3963-4255-ac00-88d77fb212d4" src="https://github.com/user-attachments/assets/45345453-55dd-4477-a1e8-9c859927ff8f" />

“End 끝” 밖으로 이동해 관련련자에게 메일로 알림을 주게 됩니다.
재시도도 가능하지만 의미가 없을 듯 합니다.
 

해당 작업은 계속 돌아야하기 때문에 if문 안에 작업이 끝나도 화면이 꺼지면 안됩니다.

<img width="1101" height="363" alt="9da0bf75-7247-4169-8767-2e14b95cd63d" src="https://github.com/user-attachments/assets/900d3b40-81c1-483f-ae00-b92ce843bc3a" />

다시 현재 시간을 체크하고 특정 요소를 우클릭하고 30초 대기, 반복문에 의해 다시 상단으로 돌아가기를 반복하며
 if문을 만족하는 다음 작업 시간까지 대기합니다.
 

 
if문 안의 작업은 상황마다 아예 다를 수 밖에 없으니, 제일 아래에 정리해보겠습니다.

if문 안의 내용 먼저 정리해 드리겠습니다.

 

크롬 → 개인 노트북 원격 접속 → 장표 구글 스프레드 시트 접속 → 특정 시트의 내용 복사 → 

로컬 PC 엑셀 열기 → 내용 붙여넣기 및 서식 맞추기(헤더 넣기, 시트명/파일명 변경) → 압축하기 → 

파일 첨부하여 메일 보내기

 <img width="1020" height="314" alt="ac58c227-a3c5-40e7-8a1c-3967a4fc1199" src="https://github.com/user-attachments/assets/1bbba60d-1b71-4b07-86c4-e02e17edb053" />

크롬을 시작하여 검색창에 원격 데스크탑 검색 및 해당 pc 접속

<img width="1017" height="311" alt="a9d1bd95-7a0a-42ff-b870-781cfdafa6bc" src="https://github.com/user-attachments/assets/74ab42a3-572e-4077-8966-caf2b6da8ef4" />

가상 환경에서는 UI인식이 불가능하여 이미지를 통해 검색해야 합니다.
클릭할 부분이 너무 작은 이미지라면 주변까지 지정해줘야 인식률이 높습니다..
이후 클릭 위치를 조정해서 클릭해주는 게 더 정확합니다.
주의 : 이미지가 조금이라도 바뀌면(사이즈, 색) 인식 불가능합니다.
바탕화면이 바뀐다던지, 화면을 확대하면 이미지도 다시 바꿔줘야합니다.

<img width="1007" height="227" alt="09b71882-e5c1-45b5-a242-e8cb15197d31" src="https://github.com/user-attachments/assets/7cef49c5-278b-4490-b633-788a16fdb4c0" />

키 보내기를 사용하면 키보드 입력과 같은 효과를 낼 수가 있습니다.
화면에 없는 요소를 찾을 때 사용하면 좋습니다.
저는 이 행위로 화면에 나오지 않는 제일 끝 시트로 이동했습니다.
위의 작업을 보면 1~2번 작업에서 의문이 드실수도 있습니다.
특정 이미지를 찾아서 Y축을 20px 만큼 내린 곳을 클릭했습니다.
이유는 변화하지 않는 특정 이미지(헤더)를 찾은 뒤 
매번 변하는 내용을 가져오기 위함입니다.(이미지가 바뀌면 찾지 못하기 때문에)
이후 컨트롤 a 컨트롤 c를 사용해서 내용을 복사합니다.
 
<img width="1009" height="133" alt="b45924f2-b30e-4cec-8d84-572ff643edbc" src="https://github.com/user-attachments/assets/7cf3331d-6f79-476a-b4bd-8f298a99719e" />

엑셀 저장시 파일명에 현재 날짜를 넣어주기 위해 다시 날짜를 가져옵니다.

<img width="1012" height="438" alt="ec9bae7e-2068-424f-9bf1-5c82f5af11dd" src="https://github.com/user-attachments/assets/578fbced-9e9a-448d-a31e-6bef6cc45078" />

엑셀을 시작 후 복사한 내용을 붙여넣습니다
워크시트의 이름을 내용에 맞게 변경해줍니다.
내용의 제일 상단에 새 행을 추가합니다.
새 데이터 테이블 만들기를 사용해서 사용할 헤더를 미리 지정해줍니다.
”Excel 워크시트에 쓰기”를 사용하여 지정된 헤더를 삽입해줍니다.
엑셀을 특정 폴더에 해당 날싸를 넣어 저장하고 닫아줍니다.

<img width="1005" height="120" alt="8b15444c-c562-4f7d-b356-a3ca714331a6" src="https://github.com/user-attachments/assets/2cde41ec-51f4-4d32-a809-f0f708e20853" />

파일을 압축한 뒤 첨부하여 특정 인원에게 전달합니다.
 
만약 if문 작업이 1분보다 적게 걸린다면 if문 작업이 2번 돌 수도 있습니다.

테스트 해본 뒤 아슬아슬하면 마지막에 대기를 걸어두는 것도 좋은 방법일 듯 합니다.

 

감사합니다.
