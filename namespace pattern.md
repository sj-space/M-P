[javascript namespace]

네임스페이스 패턴을 사용하는 이유는 수많은 함수, 객체, 변수들이 전역으로 선언 되는 것을 줄이고자 하는데 큰 목적이 있다.
이와 같은 패턴을 사용하는 이유는 전역변수를 적게 쓰면 미세하지만 메모리를 줄일수 있고,
규모가 큰 홈페이지를 작업시 라이브러리, 트래킹코드 등 서드파티(3자)의 코드를 삽입하게 될때 변수명의 충돌을 방지할 수 있다.

예) 네임스페이스를 사용하지 않은 예제.
function fnTest1(){};
function fnTest2(){};
var test1 = 'var 1';
var test2 = {};
var test3 = {};
// 위와 같은 선언은 모두 전역변수로 총 5개의 전역변수를 선언한 결과가 된다.
/* 콘솔창에서 전역변수 확인
console.log(window.fnTest1)
    //function fnTest1(){};

console.log(window.fnTest2)
    //function fnTest2(){};

console.log(window.test1)
    //var test1 = 'var 1';
    
console.log(window.test2)
    //var test2 = {};
            
console.log(window.test3)
    //var test3 = {};
*/

예) 네이스페이스를 사용한 예제
var MYTEST = {};
MYTEST.fnTest1 = function(){};
MYTEST.fnTest2 = function(){};
MYTEST.test1 = 'var 1';
MYTEST.test2 = {};
MYTEST.test3 = {};
// 하나의 전역객체 생성하여 해당 객체에 프로퍼티를 동적으로 생성하여 사용.
/* 콘솔창에서 전역변수 확인
console.log(window.MYTEST)
    //Object {test1: "var 1", test2: Object, test3: Object}

console.dir(window.MYTEST)
    //Object
        fnTest1:function()
        fnTest2:function()
        test1:"var 1"
        test2:Object
        test3:Object
*/


네이스페이스 패턴의 단점.
1. 오든 변수와 함수에 접두어를 붙여야 한다. 코드량이 길어지고 다운로드해야 하는 파일의 크기도 커진다.
2. 전역 인스턴스가 하나 뿐이어서 코드의 한 부분이 수정되면 전역 인스턴스를 수정해야 한다. (???)
3. 이름이 중첩되고 길어지므로 프로퍼티를 판별하기 위한 검색 작업이 느려진다.
이러한 단점에도 불구하고 네임스페이스는 좋은 패턴으로 사용을 권한다.


범용 네임스페이스 함수
프로그램의 복잡도가 증가하면 네임스페이스에 추가하려는 프로퍼티가 이미 존재 할 수도 있고, 실수로 내용을 덮어 쓰게 될지도 모른다.
그러므로 네임스페이스를 생성하거나 프로퍼티를 추가하기 전에 이미 존재하는지 체크하는 것이 바람직하다.

예)
// 기본
var MYAPP = {};

// 개선안
if ( typeof MYAPP === 'undefined') {
    var MYAPP = {};
}
// 위 방법보다 짧게
var MYAPP = MYAPP || {};


