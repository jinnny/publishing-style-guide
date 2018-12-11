#semantic UI custom

골자는 semantic UI를 쓰되, 불필요한 부분은 제거한 소스입니다.
기본은 test 에 있는 형태로 사용하며, 프로젝트에 따라, 컬러, 모양 등은 따로 커스텀을 할 예정입니다.

##커스텀 내용
1. 모든 태그에 font-family 제거 (다국어 대체를 위해 _fonts.scss를 쓰기 위함)
2. margin 값 제거 (h1-h6, p)
3. 테두리 라운드 0 처리 (border-radius: 0)
4. b, strong 폰트 두께 상속값으로 변경 (font-weight: inherit)
5. body 태그의 background, min-width 값 제거
6. dropdown .text:not(.default)쪽 불필요한 두께/색 제거
7. dropdown(modules)의 min-width, min-height 값 제거
8. input의 안쪽 shadow 제거 (ios 문제, -webkit-appearance: inherit)
9. mark 태그의 배경색 투명하게 변경, 폰트색 상속값으로 변경
10. 아이콘 폰트 및 이미지 경로 변경 (assets 폴더에 함께 움직이기 위함)

##style 구조
> base/
>> _reset.scss  (초기화)  <br>
>> _fonts.scss  (폰트)<br> 

> components/ (버튼, 모달 등 위젯, 컴포넌트)
>> _buttons.scss (버튼)<br>
>> _modal.scss (모달)<br>
>> …             (기타)

>layout/  (사이트의 주요 레이아웃 )<br>
>>_header.scss      (헤더)<br>
>>_footer.scss      (푸터)<br>
>>_common.scss   (레이아웃 공통요소)<br>
>> …                    (기타)

> pages/ (각페이지)
>> _index.scss   (메인)<br>
>> …             (기타)

> utils/ (프로젝트에서 사용되는 모든 Sass 도구와 헬퍼)

>>_var.scss   (변수)<br>
>>_mixins.scss      (믹스인)

> vendor/ (외부 라이브러리와 프레임워크)
>> _semantic.css

>–index.scss(index.css)  메인 파일) 

###구조 네이밍 규칙
1. 임포트 될 파일은 파일명 앞에 언더바(_)를 사용해야합니다. ex) _main.scss
1. 단어와 단어사이는 하이픈(-)을 사용해야합니다. ex) _main-content.scss