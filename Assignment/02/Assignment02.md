# 바닐라JS - 02. If, else, events


### 📚강의 분량
👉 #2.13 - # 3.8

### 🥅Assignment Goals
👉 제공된 코드를 활용해 아래의 예시와 동일하게 작동하는 애플리케이션 만들기

https://github.com/woogie01/javascript-vanillajs/assets/113490741/98f7a382-9865-41e4-b5d8-807bae2883aa

### 📕조건
* Use if/else etc


### 🍀힌트
1. if ... else : 조건식의 결과에 따라 {}로 묶인 블록의 실행 여부를 결정하는 조건문 [참고자료](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/if...else)
1. classList : 요소에 적용된 클래스들의 이름을 리스트 형태로 반환 [참고자료](https://developer.mozilla.org/ko/docs/Web/API/Element/classList)
1. remove : classList의 메서드, classList를 통해 반환된 리스트 중에서 원하는 클래스를 제거 [참고자료](https://developer.mozilla.org/ko/docs/Web/API/Element/classList)
1. add : classList의 메서드, classList의 리스트에 원하는 클래스를 추가 [참고자료](https://developer.mozilla.org/ko/docs/Web/API/Element/classList)
1. innerWidth : 브라우저의 가로 길이를 나타내는 Window 객체의 프로퍼티 [참고자료](https://developer.mozilla.org/ko/docs/Web/API/Window/innerWidth)

### 👨🏻‍💻CodeSandbox 링크 + 코드  
[CodeSandbox](https://codesandbox.io/p/sandbox/assignment-02-mylvg3?layout=%257B%2522sidebarPanel%2522%253A%2522EXPLORER%2522%252C%2522rootPanelGroup%2522%253A%257B%2522direction%2522%253A%2522horizontal%2522%252C%2522contentType%2522%253A%2522UNKNOWN%2522%252C%2522type%2522%253A%2522PANEL_GROUP%2522%252C%2522id%2522%253A%2522ROOT_LAYOUT%2522%252C%2522panels%2522%253A%255B%257B%2522type%2522%253A%2522PANEL_GROUP%2522%252C%2522contentType%2522%253A%2522UNKNOWN%2522%252C%2522direction%2522%253A%2522vertical%2522%252C%2522id%2522%253A%2522clucc4atv00063b6gel4ndvnf%2522%252C%2522sizes%2522%253A%255B100%252C0%255D%252C%2522panels%2522%253A%255B%257B%2522type%2522%253A%2522PANEL_GROUP%2522%252C%2522contentType%2522%253A%2522EDITOR%2522%252C%2522direction%2522%253A%2522horizontal%2522%252C%2522id%2522%253A%2522EDITOR%2522%252C%2522panels%2522%253A%255B%257B%2522type%2522%253A%2522PANEL%2522%252C%2522contentType%2522%253A%2522EDITOR%2522%252C%2522id%2522%253A%2522clucc4atv00023b6gjk0huqe5%2522%257D%255D%257D%252C%257B%2522type%2522%253A%2522PANEL_GROUP%2522%252C%2522contentType%2522%253A%2522SHELLS%2522%252C%2522direction%2522%253A%2522horizontal%2522%252C%2522id%2522%253A%2522SHELLS%2522%252C%2522panels%2522%253A%255B%257B%2522type%2522%253A%2522PANEL%2522%252C%2522contentType%2522%253A%2522SHELLS%2522%252C%2522id%2522%253A%2522clucc4atv00033b6g7xvotp15%2522%257D%255D%252C%2522sizes%2522%253A%255B100%255D%257D%255D%257D%252C%257B%2522type%2522%253A%2522PANEL_GROUP%2522%252C%2522contentType%2522%253A%2522DEVTOOLS%2522%252C%2522direction%2522%253A%2522vertical%2522%252C%2522id%2522%253A%2522DEVTOOLS%2522%252C%2522panels%2522%253A%255B%257B%2522type%2522%253A%2522PANEL%2522%252C%2522contentType%2522%253A%2522DEVTOOLS%2522%252C%2522id%2522%253A%2522clucc4atv00053b6gi7n3z09e%2522%257D%255D%252C%2522sizes%2522%253A%255B100%255D%257D%255D%252C%2522sizes%2522%253A%255B50%252C50%255D%257D%252C%2522tabbedPanels%2522%253A%257B%2522clucc4atv00023b6gjk0huqe5%2522%253A%257B%2522tabs%2522%253A%255B%257B%2522id%2522%253A%2522clucc4atu00013b6gcujs0exw%2522%252C%2522mode%2522%253A%2522permanent%2522%252C%2522type%2522%253A%2522FILE%2522%252C%2522filepath%2522%253A%2522%252Fsrc%252Findex.html%2522%252C%2522state%2522%253A%2522IDLE%2522%257D%255D%252C%2522id%2522%253A%2522clucc4atv00023b6gjk0huqe5%2522%252C%2522activeTabId%2522%253A%2522clucc4atu00013b6gcujs0exw%2522%257D%252C%2522clucc4atv00053b6gi7n3z09e%2522%253A%257B%2522tabs%2522%253A%255B%257B%2522id%2522%253A%2522clucc4atv00043b6g73gv6u98%2522%252C%2522mode%2522%253A%2522permanent%2522%252C%2522type%2522%253A%2522UNASSIGNED_PORT%2522%252C%2522port%2522%253A0%252C%2522path%2522%253A%2522%252F%2522%257D%255D%252C%2522id%2522%253A%2522clucc4atv00053b6gi7n3z09e%2522%252C%2522activeTabId%2522%253A%2522clucc4atv00043b6g73gv6u98%2522%257D%252C%2522clucc4atv00033b6g7xvotp15%2522%253A%257B%2522tabs%2522%253A%255B%255D%252C%2522id%2522%253A%2522clucc4atv00033b6g7xvotp15%2522%257D%257D%252C%2522showDevtools%2522%253Atrue%252C%2522showShells%2522%253Afalse%252C%2522showSidebar%2522%253Atrue%252C%2522sidebarPanelSize%2522%253A15%257D)
