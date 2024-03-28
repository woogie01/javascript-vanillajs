# 바닐라JS - 01. Objects, Arrays and Events

### 📚강의 분량
👉 #3.0 - # 3.5

### 🥅Assignment Goals
👉 제공된 코드를 활용해 아래의 예시와 동일하게 작동하는 애플리케이션 만들기

https://github.com/woogie01/javascript-vanillajs/assets/113490741/ec6fa91f-13df-43b1-86d0-c14cde806ac8

### 📕조건
1. 마우스가 title위로 올라가면 텍스트가 변경되어야 합니다.
1. 마우스가 title을 벗어나면 텍스트가 변경되어야 합니다.
1. 브라우저 창의 사이즈가 변하면 title이 바뀌어야 합니다.
1. 마우스를 우 클릭하면 title이 바뀌어야 합니다.
1. title의 색상은 colors 배열에 있는 색을 사용해야 합니다.
1. .css 와 .html 파일은 수정하지 마세요.
1. 모든 함수 핸들러는 superEventHandler내부에 작성해야 합니다.
1. 모든 조건이 충족되지 못하면 ❌를 받습니다.

### 🍀힌트
1. Window : 현재 스크립트가 작동 중인 창을 나타내는 객체입니다. [참고 자료](https://developer.mozilla.org/ko/docs/Web/API/Window)
1. mouseenter : 마우스가 위로 올라갔을 때 발생하는 이벤트입니다. [참고 자료](https://developer.mozilla.org/en-US/docs/Web/API/Element/mouseenter_event)
1. mouseleave : 마우스가 떠났을 때 발생하는 이벤트입니다. [참고 자료](https://developer.mozilla.org/en-US/docs/Web/API/Element/mouseleave_event)
1. contextmenu : 사용자가 요소를 마우스 우 클릭해 메뉴를 열 때 발생하는 이벤트입니다. [참고 자료](https://developer.mozilla.org/en-US/docs/Web/API/Element/contextmenu_event)
1. resize : 브라우저 창의 사이즈가 변할 때 발생하는 이벤트입니다. [참고 자료](https://developer.mozilla.org/ko/docs/Web/API/Window/resize_event)

<img width="583" alt="image" src="https://github.com/woogie01/javascript-vanillajs/assets/113490741/cbd20c52-2bed-46e4-aa96-016baaed0d9a">

### 👨🏻‍💻CodeSandbox 링크 + 코드  
[CodeSandbox](https://codesandbox.io/p/sandbox/javascript-01-6ghmnv?layout=%257B%2522sidebarPanel%2522%253A%2522EXPLORER%2522%252C%2522rootPanelGroup%2522%253A%257B%2522direction%2522%253A%2522horizontal%2522%252C%2522contentType%2522%253A%2522UNKNOWN%2522%252C%2522type%2522%253A%2522PANEL_GROUP%2522%252C%2522id%2522%253A%2522ROOT_LAYOUT%2522%252C%2522panels%2522%253A%255B%257B%2522type%2522%253A%2522PANEL_GROUP%2522%252C%2522contentType%2522%253A%2522UNKNOWN%2522%252C%2522direction%2522%253A%2522vertical%2522%252C%2522id%2522%253A%2522cluaojuj900063b6ghrqiqprx%2522%252C%2522sizes%2522%253A%255B100%252C0%255D%252C%2522panels%2522%253A%255B%257B%2522type%2522%253A%2522PANEL_GROUP%2522%252C%2522contentType%2522%253A%2522EDITOR%2522%252C%2522direction%2522%253A%2522horizontal%2522%252C%2522id%2522%253A%2522EDITOR%2522%252C%2522panels%2522%253A%255B%257B%2522type%2522%253A%2522PANEL%2522%252C%2522contentType%2522%253A%2522EDITOR%2522%252C%2522id%2522%253A%2522cluaojuj800023b6g8hg20ju8%2522%257D%255D%257D%252C%257B%2522type%2522%253A%2522PANEL_GROUP%2522%252C%2522contentType%2522%253A%2522SHELLS%2522%252C%2522direction%2522%253A%2522horizontal%2522%252C%2522id%2522%253A%2522SHELLS%2522%252C%2522panels%2522%253A%255B%257B%2522type%2522%253A%2522PANEL%2522%252C%2522contentType%2522%253A%2522SHELLS%2522%252C%2522id%2522%253A%2522cluaojuj800033b6gpmqzvmdk%2522%257D%255D%252C%2522sizes%2522%253A%255B100%255D%257D%255D%257D%252C%257B%2522type%2522%253A%2522PANEL_GROUP%2522%252C%2522contentType%2522%253A%2522DEVTOOLS%2522%252C%2522direction%2522%253A%2522vertical%2522%252C%2522id%2522%253A%2522DEVTOOLS%2522%252C%2522panels%2522%253A%255B%257B%2522type%2522%253A%2522PANEL%2522%252C%2522contentType%2522%253A%2522DEVTOOLS%2522%252C%2522id%2522%253A%2522cluaojuj800053b6g9jjycqh9%2522%257D%255D%252C%2522sizes%2522%253A%255B100%255D%257D%255D%252C%2522sizes%2522%253A%255B60.67634802762164%252C39.32365197237836%255D%257D%252C%2522tabbedPanels%2522%253A%257B%2522cluaojuj800023b6g8hg20ju8%2522%253A%257B%2522tabs%2522%253A%255B%257B%2522id%2522%253A%2522cluaojuj800013b6gjik668ih%2522%252C%2522mode%2522%253A%2522permanent%2522%252C%2522type%2522%253A%2522FILE%2522%252C%2522filepath%2522%253A%2522%252Fsrc%252Findex.html%2522%252C%2522state%2522%253A%2522IDLE%2522%257D%255D%252C%2522id%2522%253A%2522cluaojuj800023b6g8hg20ju8%2522%252C%2522activeTabId%2522%253A%2522cluaojuj800013b6gjik668ih%2522%257D%252C%2522cluaojuj800053b6g9jjycqh9%2522%253A%257B%2522tabs%2522%253A%255B%257B%2522id%2522%253A%2522cluaojuj800043b6g86zvs03b%2522%252C%2522mode%2522%253A%2522permanent%2522%252C%2522type%2522%253A%2522UNASSIGNED_PORT%2522%252C%2522port%2522%253A0%252C%2522path%2522%253A%2522%252F%2522%257D%255D%252C%2522id%2522%253A%2522cluaojuj800053b6g9jjycqh9%2522%252C%2522activeTabId%2522%253A%2522cluaojuj800043b6g86zvs03b%2522%257D%252C%2522cluaojuj800033b6gpmqzvmdk%2522%253A%257B%2522tabs%2522%253A%255B%255D%252C%2522id%2522%253A%2522cluaojuj800033b6gpmqzvmdk%2522%257D%257D%252C%2522showDevtools%2522%253Atrue%252C%2522showShells%2522%253Afalse%252C%2522showSidebar%2522%253Atrue%252C%2522sidebarPanelSize%2522%253A15%257D)
