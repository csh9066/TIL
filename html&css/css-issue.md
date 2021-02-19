# CSS IUSSE

- 파비콘
  - 기본적인 설정법은 헤더에 `<link rel="icon" href="./favicon.png">`
  - 인터넷 익스플로러에서는 ico 파일을 사용해야함
  - root 경로에 favicon.ico 파일이 있으면 브라우저에서는 자동적으로 가져옴
  - ios에서는 `<link rel="apple-touch-icon" href="./favicon.png">` 으로 터치 아이콘 설정 가능
- input **폰트**에 대한 정보는 상속되지 않음
- input **placedhode**r 설정은 밴더 프리픽스 `::[brower]-input-placeholder`을 직접 설정해줘야 함

  ex) -webkit-input-placeholder, -ms-input-placeholder, -moz-input-placeholder

- 브라우저마다 컬러 이름에 대한 코드값이 다 다르기때문에 헥사값이나, rgba값을 지정
  - 예를 들어 `color: tomato`를 설정했으면 브라우저마다 설정값이 다르기 때문 원하는 색상이 안나올 수 있음
- 인라인 요소는 width, height 지정 하지 못함 컨텐츠에 따라 정됨 또한 margin, hegiht도 양옆만 지정할 수 있고 위아래 지정 못함
  - 네비게이션 `a` 를 사용할 떄 `display:inline-block` 을 설정하고 패딩을 주면 클릭 영역을 넓힐 수 있음
- 인라인 요소는 두개 이상 만들경우 둘 사이에 띄어쓰기 영역이 들어가있어 브라우저마다 여백이 다를 수 있음
- 대체 텍스트를 이용할때 css 속성 `text-indent: -9999px` 를 사용하면 됨
- `float` 속성은 요소를 부유해버려 부모 요소가 인식하지 못하고 부모요소 높이가 `auto` 가 되버림
  - `float` 속성으로 지정된 요소 옆에 `clear: |both|left|right` 을 이용해 해제 해주거나
  - 부모요소에 가상 요소 설정 `.clearfix::after { content: ""; display: block; clear: both}`
- `line-height` 블록 요소에서 텍스트 줄 사이의 거리(행간)을 설정함
  - `line-height: 1.5` 속성 값에 숫자를 지정하면 폰트 기준 으로 높이를 측정함 요소의 `font-size: 16px` 이면 텍스트당 행간(높이)는 `24px` 임