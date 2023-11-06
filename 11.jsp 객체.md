● 객체란 : 프로그래밍에서 '객체'는 데이터를 저장하고 처리하는 기본 단위 <br>
       : 자바스크립트에서 객체는관련된 정보와 동작을 함께 모아 놓은 것 <br>


● 내장 객체 : 프로그래밍을 할 때 자주 사용하는 요소들을 자바스크립트에서 미리 정의해 놓은 객체 <br>
● 문서 객체 모델(DOM) : 웹 문서 자체도 객체이고 웹 문서에 포함된 이미지와 링크, 텍스트 필드 등은 모두 이미지 객체, 링크 객체, 폼 객체처럼 각각 별도의 객체.<br>
● 브라우저 객체 모델 : 웹 브라우저에서 사용하는 정보도 객체로 지정되어 있다.<br>
● 사용자 정의 객체 : 필요할 때마다 사용자가 만들어 사용하는 객체 <br>

● 사용자 정의 객체 만들기 <br>
(1)<br>
객체는 여러 개의 프로퍼티(속성)로 구성되어 있는데, 프로퍼티는 '키 : 값' 형태를 가지고 있다.<br>

● 키와 값<br>
객체명 { <br>
    키1 : 값1, <br>
    키2 : 값2,<br>
    ...<br>
}<br>


```  let book = {

            title: "phyon",
            page: 20,
            array: ["java", "html", "css"],
            content: {
                a: 10,
                b: 20
                //배열 안에 배열 넣기
            }
        }

        console.log(book);
        console.log(book.page);
        console.log(book.array);
        console.log(book.content.a); // 배열안에 배열을 넣어서 출력도 가능

        book.content = [1000,2000]; //content를 고치기도 가능
        console.log(book.content);
```

(2) 
빈 객체를 만든 후 프로퍼티를 추가하면서 객체를 만들 수 있다.
빈 객체 만들기 : 
ex)
``` 
     let name = { } or let name = new Object();
```
빈 객체에 추가하기
``` 
        let book2 = Object();
        book2.title = 'jsp';
        book2.page = 20;
        console.log(book2);
```

● 객체 중첩하기 <br>
객체 안에 또다른 객체를 넣을 수 있다 - 둘 이상의 객체 중첩
```
    let student = {
            name: "철수",
            score: {
                국어: 40,
                수학: 70,
                average: function () {
                    return (this.sum()) / 2
                },
                sum : function () {
                return(this.국어 + this.수학)
                }
            }
        }
        console.log(student.score.average());
        console.log(student.score.sum());

```

● 객체 메서드 정의하기 <br>
메서드(method) : 객체의 프로퍼티중 객체의 동작을 지정하는 함수 <br>
메서드를 선언하는 방법은 일반적인 함수를 선언하는 것과 비슷

```
let book = {
title : 'phyon',
buy : function () {
    console.log('이 책을 구입했습니다.);
}
}
```

● 객체 복사하기 <BR>

(1) 원시 유형 자료 복사 <br>
'값'을 복사한다<br>
복사한 자료의 값을 변경하고 원래 자료의 값은 그대로<br>

(2)객체 복사 <br>
'주소'를 복사한다 <br>
복사한 자료의 값 변경되고 원래 자료의 값도 바뀜<br>



