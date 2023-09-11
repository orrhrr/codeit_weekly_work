# 이승연님 1주차 Weekly mission 리뷰 내용

# 체크리스트

- [x] PC사이즈만 고려해 주어진 디자인을 구현합니다.
- [ ] Linkbrary 아이콘은 `cursor: pointer` 가 돼야 하고, 클릭 시 루트 페이지(‘/’)로 이동 합니다.
- [x] “로그인”은 `cursor: pointer` 가 돼야 하고, 클릭 시 로그인 페이지(‘/signin’)로 이동 합니다.
- [x] “링크 추가하기”는 `cursor: pointer` 가 돼야 합니다.
- [ ] “Privacy Policy”, “FAQ”는 `cursor: pointer` 가 돼야 하고 , 클릭 시 각각 개인정보보호 페이지(‘/privacy’), FAQ 페이지(‘/faq’)로 이동 합니다.
- [x] 페이스북, 트위터, 유튜브, 인스타그램 아이콘은 `cursor: pointer` 가 돼야 하고, 클릭 시 각각의 홈페이지로 이동 합니다.
- [x] 브라우저 너비가 1920px을 넘어갈 경우 하늘색 배경색은 너비를 꽉 채우도록 채워지고, 내부 요소들의 위치는 고정되고, 여백만 커지도록 해주세요.
- [x] PC 사이즈에서 기기의 width가 1920px 보다 작아질 때, “Linkbrary” 로고의 왼쪽 여백 `200px` “로그인" 버튼의 오른쪽 여백 `200px`이 유지되고, 화면의 너비가 작아질수록 두 요소간 거리가 가까워져야 합니다.
- [x] PC 사이즈에서 기기의 width가 1920px 이상이면 내부에 있는 요소의 위치는 landing/pc 와 동일한 간격을 유지하며 가운데 정렬해야 합니다.
- [x] 브라우저 너비가 1920px 보다 작아질 때, 최하단에 있는 “codeit-2023”의 왼쪽 여백 `104px`과 SNS 아이콘들의 오른쪽 여백 `104px`을 유지하면서 가운데 있는 “Privacy Policy”, “FAQ” 요소와 각각 동일한 간격을 유지하며 가까워져야 합니다.
- [x] HTML, CSS 파일을 Netlify로 배포해 주세요. (참고: https://www.codeit.kr/learn/5309)

# 전반적인 리뷰

- 재사용성을 고려해 custom css variables를 사용하신 점 아주 좋게 봤습니다! 다만 css variables는 문법적으로 선언할때와 사용할때가 좀 다른데요, 관련하여 [mdn문서](https://developer.mozilla.org/ko/docs/Web/CSS/Using_CSS_custom_properties) 참고해주시면 될 것 같습니다 :)
- semantic elements를 써주셨네요, 잘하셨습니다! semantic markup은 검색엔진최적화(SEO)에 도움이 되기때문에, 지금처럼 적극 활용해주시면 좋을 것 같습니다 :)
- 디렉토리 내에서 쓰이지않는 불필요한 소스들은 지워주세요! (weeklyWork.zip파일이 들어가있네요)
- `<a href="/privancy">` 오타가 났네요! privacy로 바꿔주세요. 오타가 자주 나는 편이라면 [code spell check를 도와주는 vscode extension](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)사용을 추천드려요.
- 1920px 아래로 화면 가로 사이즈가 작아질때 .section-container 아래에 있는 자손 엘리먼트들이 디자인 시안대로 구현되지않는 모습을 확인할 수 있어요. 형제 요소끼리는 위아래 50px padding값을 가지게끔하고, 가장 첫번째와 가장 마지막 요소의 위아래 padding값을 없애고 양옆으로 마진이 자동적용될 수 있도록 `margin: 0 auto`을 주게끔 바꿨다면 어땠을까요? 그리고 부모 컨테이너에서 위아래로 필요한 마진값을 주는게 맞아보입니다 :)
- 위에서 이야기한 형제 요소끼리의 여백은 50px인데 이 여백이 디자인대로 구현되어있지않네요, 시안대로 고쳐주세요 :)
- .main-section에 현재 `justify-content: flex-end;` 가 적용되어있는데, 박스 영역 내에서 맨아래로 정렬해야하는 등의 특별한 의도가 아니라면 가운데 정렬하는게 맞아보입니다 :)
- .wanted-link-section, folder-management-section, link-share-section, link-search-section에서 같은 스타일링이 반복되고있지않나요? 동일한 스타일을 가졌다면 같은 클래스이름을 가질 수 있도록 묶어줘도 될 것 같습니다 :)
