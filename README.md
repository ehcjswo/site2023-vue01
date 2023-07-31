Vue를 활용한 모던 아트 사이트
<img src="https://raw.githubusercontent.com/ehcjswo/site2023-vue01/main/src/assets/images/intro/gitImg01.jpg" />
<br><br>

View Site : https://dh2023-vue01.netlify.app/
<br>


👋 소개<br>
Vue.js를 활용하여 개발된 현대 미술 작품들을 감상하고 소개하는 플랫폼입니다. 이 사이트는 Vue.js의 강력한 기능과 유연성을 활용하여 사용자들에게 뛰어난 사용자 경험을 제공합니다. Restful API 활용하여 다양한 현대 미술 작품과 아티스트 정보를 외부 API로부터 불러와서 동적으로 표시합니다.(Youtube API, Unsplash API, Movie API 등등) 이 프로젝트에서 Component 기반의 모듈, 그리고 axios 라이브러리를 활용하여 API와 통신, 비동기 처리를 통해 데이터를 불러오는 것을 학습하였습니다.<br><br>


🔧 사용 스택<br>
-Vue.js: Vue.js는 현대적이고 유연한 JavaScript 프레임워크로, 사용자 인터페이스(UI)를 구축하기 위해 사용됩니다. 이 코드에서는 Vue.js를 사용하여 웹 페이지의 컴포넌트 기반 렌더링을 구현하고, 각 컴포넌트를 효율적으로 재사용합니다.<br>
-Vue의 단일 파일 컴포넌트 구조 : Vue에서는 컴포넌트를 단일 파일 컴포넌트(Single-File Components)라는 형태로 구성할 수 있습니다. 이는 HTML, JavaScript, CSS 등의 코드를 한 파일에 모두 작성하는 방식으로, 개발자들이 컴포넌트를 보다 구조적으로 관리할 수 있게 해줍니다.<br>
-Vue 템플릿 : 태그 내에서 Vue 컴포넌트의 템플릿을 작성합니다. 템플릿은 사용자에게 보여지는 UI의 구조와 내용을 정의하는데 사용됩니다.<br>
-Vue Router : 는 Vue.js의 공식 라우터인 Vue Router를 사용한 것입니다. Vue Router는 클라이언트 사이드 라우팅을 구현하여 SPA(Single Page Application)처럼 동작하도록 해줍니다. 는 라우터에 의해 매칭된 컴포넌트를 렌더링하는 데 사용됩니다.<br>
-SCSS: style 태그 내에서 사용된 lang="scss" 속성은 해당 스타일이 SCSS(Sass)로 작성되었다는 것을 나타냅니다. SCSS는 CSS의 확장 문법으로, 보다 간결하고 효율적인 스타일 코드를 작성할 수 있도록 해줍니다.<br>
-fetch : JavaScript의 fetch 함수를 사용하여 외부 API에 HTTP 요청을 보냅니다. API를 사용하여 자료들 검색하고 가져옵니다.<br>
-비동기 처리 : await과 async 키워드를 사용하여 비동기 함수를 구현합니다. 이를 통해 비동기적으로 API 호출을 처리하고, 결과가 도착하면 해당 데이터를 Vue 컴포넌트의 상태에 업데이트합니다.<br><br>

📞 React와 vue.js의 차이점?<br>
-문법 및 템플릿 : React는 JSX라는 자체 문법을 사용합니다. JSX는 JavaScript와 유사한 XML 기반의 문법으로 컴포넌트를 작성합니다. Vue는 템플릿 문법을 사용합니다. 이는 보다 직관적이고 일반적인 HTML과 비슷하며, 따라서 기존의 웹 개발 지식을 가진 개발자들에게 더 익숙할 수 있습니다.<br>
-상태 관리 : React에서는 주로 외부 라이브러리인 Redux 또는 MobX와 함께 사용하여 상태 관리를 합니다. Vue는 상태 관리를 위한 기본적인 도구인 Vuex를 내장하고 있습니다. 이를 통해 상태 관리를 더 쉽게 구현할 수 있습니다.
-생태계 및 커뮤니티 : React는 Facebook과 개발자 커뮤니티에서 매우 큰 지원을 받고 있습니다. 따라서 많은 개발자들과 다양한 라이브러리, 플러그인 등이 존재합니다. Vue는 최근 몇 년간 인기가 급증하고 있으며, 커뮤니티가 지속적으로 성장하고 있습니다. React만큼은 아니지만 여전히 활발한 생태계를 가지고 있습니다.<br><br>



✍️ 구현 내역<br>
-swiper를 활용한 이미지 슬라이드<br>
-router기능을 활용한 페이지<br>
-탭 메뉴로 구성된 시대별 유명 작품<br>
-Youtube 검색, 태그 기능<br>
-Unsplash 랜덤 이미지 슬라이드, 검색, 태그 기능<br>
-Movie 이미지 슬라이드, 검색, 태그 기능<br>
