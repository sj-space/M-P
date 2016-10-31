# M

attribute-quotes.md
    속성은 따옴표로 감싸는게 좋은듯.
    span[class^=main] 보다
    span[class^="main"]
url-quotes.md
    url도  따옴표로 감싸는게 좋은듯.
    background-image: url(bar/ + $foo); 보다
    background-image: url("bar/" + $foo);
quotes.md
    속성, url과 같게 쌍따옴표 사용.

bem-depth.md


border-zero.md
    0값이 경우 숫자보다 none 사용하는 것이 좋은 방법이라고 알고 있음.

brace-style.md
    style: '1tbs'
    allow-single-line: false
    이 방식이 작업에 익숙한 방법 같음.

class-name-format.md


clean-import-paths.md


empty-args.md


empty-line-between-blocks.md


extends-before-declarations.md
extends-before-mixins.md
    순서까지 정해야 하는건가?

final-newline.md


force-attribute-nesting.md
force-element-nesting.md
force-pseudo-nesting.md
    줄바꿈이 필요없는 상태에서 일부러 구분하기 위해서 줄바꿈을 해서 얻어지는건 무엇인가?

function-name-format.md


hex-length.md
    style: short
    줄여 쓸수 있는 색상은 짧게 쓰는게 나을듯

hex-notation.md
    style: lowercase
    소문자로 쓰는게 익숙

id-name-format.md
    allow-leading-underscore:false
    convention: camelcase
    카멜방식으로 가면 밑줄 허용 필요 없을듯 한데~

indentation.md
    size:4
    탭이 스페이스로 했을때 4칸이므로~

leading-zero.md
    include: false (defaults to false)
    소수점 앞에 있는 0을 안쓰는게 좋은 방법이라 알고 있음. 증거를 찾아야 겠음.

mixin-name-format.md


mixins-before-declarations.md


nesting-depth.md


no-attribute-selectors.md
    속성 선택자 사용은 가능해야 하지 않을까~
    no-attribute-selectors은 활성화 되면 안될듯

no-color-hex.md
    no-color-hex 비활성화 해야 할듯
    색상사용시 핵사코드를 사용안하면 어찌

no-color-keywords.md
    no-color-keywords 비활성화 해야 할듯
    임시 테스트시 색상을 키워드로 넣는 경우가 있는데 이걸 막으면 안될듯.

no-color-literals.md


no-combinators.md
    비활성화

no-css-comments.md
    필요한가?


no-debug.md
    @debug 지시어는 오류를 감지하고 표준 에러 출력 스트림에 SassScript 식의 값을 표시합니다.

no-disallowed-properties.md
    ?? 왜 필요한거

no-duplicate-properties.md
    관련 내용 넣으면 안될듯 한데..

no-empty-rulesets.md
    내용이 비어있는 선택자는 결국 필요없긴 하지

no-extends.md
    extend를 연달아 쓸 경우 문제가 있나? 없다면 필요없지 싶은데

no-ids.md


no-important.md
    important 사용을 지양하기는 하지만 막기엔 추후 문제가 있지 않을까

no-invalid-hex.md
    필요한 이유가? 없어도 잘못넣은 색상코드는 안되지 않나?

no-mergeable-selectors.md
    중복된 선택자....extend 사용하면 나오는거 아닌가?

no-misspelled-properties.md
    철자가 틀리면 작업시 원래 오류 나는거 아님? 오류 났다고 알려주는거니까 좋은건가.

no-qualifying-elements.md
    ??

no-trailing-whitespace.md
    ?? 공백을 후행하는 것은 허용되지 않음 ??

no-trailing-zero.md
    ??

no-transition-all.md
    ?? transition에서 all ??

no-universal-selectors.md
    * 선택자는 사용 안하는게 좋지

no-url-protocols.md
    ??링크 방법까지 정해야 하나? 필요없어 보임

no-vendor-prefixes.md
    ??

no-warn.md
    ??@warn 지시문이 문제에 대한 주의 조언을 제공하는 데 사용

one-declaration-per-line.md
    min파일로 압축할땐테 라인을 내려쓰느냐 한줄로 쓰느냐에 대한 가이드가 필요한지 모르겠음

placeholder-in-extend.md
    ??

placeholder-name-format.md
    ??기호가 이름 앞에옴?

property-sort-order.md
    속성 규직이 include와 extend등을 사용하는데 규칙 어긋남이 있을것 같은데...

property-units.md


pseudo-element.md
    .foo::before {, .foo:hover {

shorthand-values.md
    속성값 1, 2, 3

single-line-per-selector.md
    single-line-per-selector: 0 값을 주면 비활성화로 여러 선택자를 한줄에 넣어도 되는건가?

space-after-bang.md


space-after-colon.md


space-after-comma.md


space-around-operator.md
    기호의 앞뒤로 공간을 두는것이 보기에 편하지

space-before-bang.md


space-before-brace.md
    선택자와 { 사이에 빈 공간 읽는게 보기 편하지

space-before-colon.md
    보기 편하다는 의미에서 같음

space-between-parens.md
    bar( $baz )역시 같은 의미에서 빈 공간 읽는게 편하지 않나?

trailing-semicolon.md
    세미콜론은 찍어주는게 좋지

variable-for-property.md
    ??

variable-name-format.md
    allow-leading-underscore: true
    convention: hyphenatedlowercase
    클래스와 구분짓는것...그럼 기능 클래스하고 겹치기는 하는데....

zero-unit.md
    include: false
    0px과 같이 단위 쓰는게 익숙하므로
