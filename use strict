"use strict"; // 안전한 코딩을 위한 가이드 라인
/*
"use strict" 주의
    1. "use strict"는 함수나 스크립트의 최상위에서 사용되어야 한다.
    2.IE 10 이전 버전에서는 사용할 수 없다.

strict 모드의 제한
    "use strict" 사용하였을 경우 제한 되는 경우

    1. 선언하지 않고 변수를 사용할 때.
    test = 3.14; // test 변수를 선언하지 않고 사용하고 있기 때문에 오류.

    2. 변수, 함수, 매개변수를 삭제하려 할 때.
    var test = 3.14;
    delete test; // 삭제 안됨.

    3. 동일한 프로퍼티를 한번 이상 선언하려 할 때.
    var test = { p1:10, p1:20} //p1, p1 동일하므로 오류

    4. 매개변수 이름이 동일할 때.
    function(p1, p1){ //p1, p1 동일하므로 오류
        //
    }

    5. 8진법의 숫자 리터럴과 특수문자를 할당하려 할 때.
    var test = 010; // 8진법의 숫자 리터럴을 할당해서 오류
    var test2 = %; // 특수문자를 할당해서 오류

    6. 읽기전용에 할당하려 할 때.
    var obj = {};
    Object.defineProperty(obj, "x", { varle : 0, writable : false });
    obj.x = 3.14; // 오류

    7. 얻기 전용(get-only)에 할당하려 할 때.
    var obj ={
        get x() {
                return 0
        }
    }
    obj.x = 3.14;//오류

    8. 삭제불가능한 프로퍼티를 삭제하려 할 때.
    delete Object.prototype; //오류

    9. with 키워드를 사용하려 할 때.
    with(Math){
        x = cos(2);
    } // 오류

    10. eval()을 사용하려 할 때.
    eval("var x=2");
    alert(x); // 오류? 테스트 해보면 문제없이 실행되는데...

    with와 eval()은 대표적으로 사용하지 말아야 하는 키워드.

    eval()은 보안상, 퍼포먼스상 문제가 있기 때문에 반드시 필요한 것이 아니라면 사용하지 말라고 함.

    with 명령어
    : with 이후에 오는 구문을 위해 scope chain에 인자로 받는 object를 추가한다.
    예제) style의 설정을 간단하게 적용.
    with ( document.getElementById('testDiv').style ) {
        background = 'yellow';
        color = 'red';
        border = '1px solid red';
    }

    with 명령어를 사용하면 안되는 이유
    1. 새로운 scope를 생성함으로써 생기는 추가적인 자원 소모.
    새로운 인자로 들어온 scope에서만 데이터와 함수들을 이용할 경우 성능이 향상되겠지만, 상위의 scope에서 데이터를 가져오는 경우 그때마다 추가적인 처리 시간이 들어가게 된다. 이것은 with 안의 구문들이 어떠한 구문들로 이루어졌느냐에 따라 성능의 차가 다르게 나올 것이다.

    2. with로 인해서 생기는 모호성
    예) function doSomething( value, obj ){
        with ( obj ) {
            value = "which scope is this?";
            console.log(value);
        }
    }
    위의 경우 value는 인자인 "value" 일수도 있고, obj 안의 속성인 "value" 일수도 있다. value가 어떤것인지 정확하게 아는 것은 해당 함수를 작업한 본인뿐이다. 때문에 with문 사용을 자제하라고 하는 것이다.

    with의 대체제
    예제) style의 설정을 간단하게 적용.
    var s = document.getElementById("testDiv").style;
    s.background = "yellow";
    s.color = "red";
    s.border = "1px solid red";
    with 보다 글자수는 많지만 더 직관적이고, with처럼 헷갈릴만한 요소도 없다.
    성능상 하나의 scope를 새로 만드는 것보다 로컬 변수에 대한 접근이 더 빠른 경우가 많기도 함.
*/
