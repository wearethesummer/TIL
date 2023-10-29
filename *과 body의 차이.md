~~~
* {}
body {}
~~~

둘 다 전체에 적용된다는 뜻을 갖고 있지만 큰 차이가 있다.

```body```태그는 속성 값을 정의해주면 태그 자체와 상속이 허용되는 값들은 body 태그 내의 태그나 클래스 아이디로 상속된다. 
<br/>
하지만 ```*```는 상속과는 관계없이, 모든 요소에 적용된다.

예를들어 박스를 어떤 기준에 맞춰 계산할지 정하는 속성 ```box-sizing```은 상속이 되지 않는다.

~~~
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        body {box-sizing: border-box}
        .contents {
            padding: 20px;
            width: 300px;
            background: orangered;
            height: 300px;
        }
    </style>

</head>
<body>
    <div class="contents"></div>
</body>
</html>
~~~

이렇게 ```body``` 태그에``` box-sizing``` 을 주더라도 ```contents``` 클래스에는 ```border-box``` 가 상속되지 않는다. 
<br/>
실질적으로 background 는 총 넓이에 칠해지게 된다.
<br/>
하지만 ```*``` 에 ```box-sizing``` 속성을 주게 되면, 300px의 넓이에 칠해지는 것을 볼 수 있다.
