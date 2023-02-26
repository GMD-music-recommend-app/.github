# 🎧 지뭐듣(지금 뭐 듣지?)
#### '지뭐듣'은 위치 기반 사용자 간 음악 추천 어플입니다. <br><br><br>

## 🤔 <I>Why?</I> :: 프로젝트 개요
> 매일 다니는 골목 길을 걸을 때마다 듣는, 퇴근 길에, 여행지에서... 처럼 모두들 장소와 관련된 음악이 한 곡쯤은 있을 것 입니다.<br><br>
> <b><I>'지뭐듣'</I></b> 은 유저끼리 단순히 음악만을 추천하는 것을 넘어,  
> 위치와 음악을 <b>"감정"</b>으로, 유저와 유저를 <b>"공감"</b>으로 연결하기 위해 만들어졌습니다.

<br>

## 🏆 <I>What?</I> :: 화면 및 기능<br>

> ### 주요 기능
> * 위치를 기반으로 음악 추천<br>
> * 음악 정보 확인 및 음악 듣기<br>
> * 추천 음악 별 댓글 및 공감하기<br>
> * 지역 별 인기 차트 제공<br>
> ### 화면 및 기능 설명
> <details>
> <summary>1. 메인 화면</summary>
> <img src="https://user-images.githubusercontent.com/92194918/221408397-dd19e300-04d5-4979-80e2-f455bd79976e.gif" width="240"/><br>
> <ul> 
> <li><b>지도 위에 생성된 음악 핀을 통해 내 위치 주변에서 생성된 음악 정보를 확인할 수 있습니다.</b></li>
> <li>Splash에서 FusedLocation을 통해 유저의 현재 위치 정보를 가져와 MainActivity로 전달합니다.</li>
> <li>MainActivity에서 전달받은 위치 정보를 VieModel의 LiveData에 저장 후<br> ViewModel의 Observer를 통해 LiveData를 감지하여 해당 위치 정보를 기준으로 지도 화면을 표시합니다.</li>
> <li>LiveData에 저장 된 위치 정보를 기준으로 반경 5km 내에 생성 된 음악 핀 데이터를 Coroutine 통해 비동기적으로 가져옵니다.</li>
> </ul>
> </details>
> <details>
> <summary>2. 추천 음악 정보 화면</summary>
> <img src="https://user-images.githubusercontent.com/92194918/221409122-a93723d2-a67d-45e8-ae72-fd12e5a1b14a.gif" width="240">
> <img src="https://user-images.githubusercontent.com/92194918/221409319-3f15645a-815e-40f5-9d53-7316305259ec.gif" width="240"/><br>
> <ul>
> <li><b>지도 위에 생성된 음악 핀을 클릭하면 해당 장소에서 추천된 음악의 정보를 확인할 수 있습니다.</b></li>
> <li>'ReadMoreTextView' 라이브러리를 사용하여 사연이 2줄 이상일 경우 더보기 클릭 시 전체 텍스트가 표시되도록 구현했습니다.</li>
> <li>앨범 이미지의 유튜브 버튼을 클릭하면 해당 음악의 "가수 곡 제목"을 검색한 유튜브 화면으로 이동합니다.</li>
> <li>우측 상단의 아이콘은 본인 생성 여부, 공감하기, 공유하기 버튼이며 추후 구현 예정입니다.</li>
> </ul>
> </details>
> <details>
> <summary>3. 음악 추천하기</summary>
> <img src="https://user-images.githubusercontent.com/92194918/221411387-e3c4104b-7729-4e47-bf41-35e0b7a12249.gif" width="240">
> <img src="https://user-images.githubusercontent.com/92194918/221411240-71db16af-92db-4bc4-9e54-ee71f23884e5.gif" width="240">
> <img src="https://user-images.githubusercontent.com/92194918/221411662-3435fe31-6919-42c4-bbb7-fd782c771798.gif" width="240">
> <img src="https://user-images.githubusercontent.com/92194918/221412025-374e2740-3d11-49cc-891f-8fe732f10c2f.gif" width="240"/><br>
> <ul>
> <li><b>장소 선택부터 사연 입력까지 음악 추천하기 기능의 일련의 과정입니다.</b></li>
> <li>'다른 위치에서 추천하기' 클릭 시 첫 번째 화면부터 시작하며 현재 위치에서 추천하기 시 두 번째 화면에서 시작하게 됩니다.</li>
> <li>Fragment 전환 이후에도 추천 위치, 선택한 음악의 데이터를 보존하기 위해 'activityViewModels'를 사용하여 데이터를 유지하도록 했습니다. </li>
> <li>음악 검색화면에서 음악 데이터는 'ManiaDB API'를 사용하여 음악 정보를 가져오도록 했습니다.</li>
> </ul>
> </details>

<br>

## 🛠️ <I>How?</I> :: 기술 스택 <br>
<details>
  <summary>🤝  Communication</summary>
  <img src="https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white">
  <img src="https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=notion&logoColor=white">
  <img src="https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white">
  <img src="https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white">
</details>
<details>
  <summary>🖥️  Front End</summary>
  <img src="https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=Android&logoColor=white">
  <img src="https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=Kotlin&logoColor=white">
  <img src="https://img.shields.io/badge/Mac-FFFFFF?style=for-the-badge&logo=apple&logoColor=black">
  <img src="https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white">
  <br>
  <img src="https://img.shields.io/badge/Jetpack AAC-FF0000?style=for-the-badge&logo=&logoColor=white">
  <img src="https://img.shields.io/badge/MVVM-0F9D58?style=for-the-badge&logo=&logoColor=white">
  <img src="https://img.shields.io/badge/Coroutine-0F9D58?style=for-the-badge&logo=&logoColor=white">
  <img src="https://img.shields.io/badge/Retrofit-3E4348?style=for-the-badge&logo=Square&logoColor=white">
  <img src="https://img.shields.io/badge/OkHttp-3E4348?style=for-the-badge&logo=Square&logoColor=white">
  <img src="https://img.shields.io/badge/Glide4-008ED2?style=for-the-badge&logo=&logoColor=white">
  <img src="https://img.shields.io/badge/Google Maps-4285F4?style=for-the-badge&logo=googlemaps&logoColor=white">
  <img src="https://img.shields.io/badge/Mania DB-FF3366?style=for-the-badge&logo=music&logoColor=white">
</details>
<details>
  <summary>💾  Back End</summary>
  <img src="https://img.shields.io/badge/IntelliJ-000000?style=for-the-badge&logo=intellijidea&logoColor=white">
  <img src="https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white">
  <img src="https://img.shields.io/badge/Java-FFFFFF?style=for-the-badge&logo=openjdk&logoColor=red">
  <img src="https://img.shields.io/badge/Mac-FFFFFF?style=for-the-badge&logo=apple&logoColor=black">
  <img src="https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white">
  <br>
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white">
  <img src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white">
  <img src="https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=swagger&logoColor=black">
  <img src="https://img.shields.io/badge/MVC-0F9D58?style=for-the-badge&logo=&logoColor=white">
</details>

<br>

## 👩‍👩‍👦 <I>Who?</I> :: Members
* Android ([GitHub](https://github.com/GMD-music-recommend-app/GMD-FE))
  + [민세림](https://github.com/anonymousRecords) 
  + [조진수](https://github.com/jinsuCH0/) 
* Back ([GitHub](https://github.com/GMD-music-recommend-app/GMD-BE))
  + [박희원](https://github.com/hw130) 
  + [정조은](https://github.com/joeun-01)
* UX/UI
  + 유진아
