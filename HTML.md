# HTML 코딩 스타일

## 웹표준과 웹접근성

- 웹표준 준수
- 브라우저는 IE11+, Chrome, Safari, Firefox, edge, wale 지원
- 마크업시 문서의 흐름을 생각하며 마크업 (CSS가 없어도 문서로 읽힐 수 있도록 마크업)
- html으로 구조를 잡고난 뒤에 스타일시트를 이용하여 디자인을 맞추는 순서로 퍼블리싱을 진행

## HTML5

- html5에서 없어진 tag들은 사용하지 않는다.
- style 과 script tag에 Type을 지정하지 않는다.
- 페이지에 제목으로 명시될만한 요소가 없는 경우 `class="hidden"` 으로 페이지 타이틀을 명시해준다.
- style 을 HTML tag에 inline으로 넣지 않는다.
- 각종 Path는 ” 로 묶어준다.
- attribute 의 네이밍 에는 언더바( _ ) 가 아닌 하이픈 ( - ) 으로 공백 구분하여 네이밍 한다.
  - data-sample_attribute (X)
  - data-sample-attribute (O)

---

### 줄바꿈과 들여쓰기

- Indent : space 4칸
- Continuation Indent : ?칸 - 정하는중
- block요소들 그리고 CSS의 display가 block 또는 inline-block 으로 지정된 inline 요소 들은 줄바꿈과 들여쓰기를 한다.
- header, footer, section, article, nav, aside, div, form, field 등 내용이 그룹화 되는 tag 뒤에는 새로운 빈줄을 추가한다.

## Tag 주의사항

| Tag       | Comment                                                      |
| --------- | ------------------------------------------------------------ |
| div, span | 절대적으로 최소화 해서 사용. div 와 span을 남용할 경우 소스의 가독성이 떨어진다. |
| table     | thead, tfoot, tbody 구분을 명확히 해야하며 th 와 td 또한 구분해서 사용해야 한다. caption 또한 가능하면 넣어준다. |
| button, a | 둘을 명확히 구분해서 사용해야 한다. 별다른 동작이 필요없이 link 역할을 할때에는 a 를, JS와의 연동 혹은 submit 역할을 할때에는 button 을 사용한다. button을 사용할 시에 특정 type 이 지정되지 않을 경우에 type="button" 을 항상 명시해준다. |
| img       | alt 를 반드시 넣어준다.                                      |
| form요소  | 디자인을 위한 Custom UI 를 구현할 때에도 반드시 form 요소들을 사용해야한다. |
| nav       | 사이트 최상위 메뉴(GNB 영역)에 한번만 사용한다.              |

## Class, ID 네이밍 규칙

- 스타일 적용을 위한 class와 ID 는 모두 소문자와 under_score 를 조합하여 만든다.

- JavaScript용 class name은 앞에 'js_'를 붙여 style용 class name과 구분한다. (태그가 변경되거나 불필요한 스타일용 클래스가 제거 되어도 기능에 영향을 최대한 적게 주기 위한 방안)

  ```
  .js_series_list (O)
  ```

- naming은 내용을 기준으로 지정하여 style 과 분리시킨다.

  ```
  .blue_box, .orange_text             (X)
  .header_title, .subcategory_info    (O)
  ```

- 네이밍은 재사용성을 위해 최대한 일반화한다.

  ```
  .warning_text_point_consume     (X)
  .warning_text                   (O)
  ```

- 요소를 감싸고 있는 DOM과 실제 역할을 하는 요소들의 네이밍 통일성을 최대한 맞춰준다.

  ```
  <ul class="element_item_wrapper">
     <li class="element_item"></li>
     <li class="element_item"></li>
  </ul>
  ```

## 참고

- [HTML Validator](http://validator.kldp.org/)

- [CSS Validator](http://www.css-validator.org/)

- [Google HTML Style Guide](https://google.github.io/styleguide/htmlcssguide.xml)

- [ridi Style Guide](https://github.com/ridi/style-guide/blob/master/HTML.md)

  

