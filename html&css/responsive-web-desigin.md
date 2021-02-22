# 반응형 웹 디자인

예전에는 데스크탑을 대상으로 페이지를 설계했지만 오늘날에는 스마트폰, 태블릿등 환경이 다양해졌다 다양한 화면 너비, 해상도에 맞춰 유동적으로 변화는 웹 페이지 디자인을 반응형 웹 디자인 (Responsive Web Design)이라고 한다.

## viewport meta tag

- **뷰포트**란 사용자가 보이는 웹페이지의 영역을 말함
- 뷰포트 메타 태그를 이용해 모바일에서 뷰포트를 제어 할 수 있음
  > `<meta name="viewport" content="width=device-width, initial-scale=1.0">` - 기본적으로 권장하는 태그
- properties
  - `width`은 뷰포트의 너비 설정 px 단위고 기본 값은 980px 임 `device-width`로 설정하면 디바이스의 너비에 맞추겠다는 뜻
  - ` initial-scale`은 처음 페이지 로딩시 확대/ 축소 수준을 비율 설정
  - `minimum-scale`와 `maximum-scale`속성을 사용해서 확대/ 축소 최소 최대비율 설정 가능
  - `user-scalable: yes | no`는 사용자가 뷰포트를 확대 축소 할 수 있는지 설정함 기본값은 `yes`

## Media Query

- 미디어 쿼리는 단말기 유형이나 뷰포트같은 수치에 따라 웹 사이트나 앱 스타일을 수정할 때 사용
- `@media`를 이용해 단말기 유형이나 디바이스 크기나 비율을 구분 할 수 있음

```css
/* 브라우저 창이 600px 이하인 경우 body의 배경색인 lightblue로*/
@media only screen and (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```

#

## Reference

- https://www.w3schools.com/css/css_rwd_intro.asp
- https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Responsive_Design
- https://poiemaweb.com/css3-responsive-web-design
