# content="";



* The content property in CSS is used in conjunction with the pseudo elements ::before and ::after. It is used to literally insert content. There are four value types it can have.

* content 속성은 가상요소에 보이는 컨텐츠를 지정해줄 때 쓰인다

## "" 안에 들어갈 수 있는 4가지 요소



### String = 글씨

예제 | 

```
.name::before{
		content:"Name:";
}

-

<div class="name">Chris</div>

```

렌더링된 화면 |

```
Name: Chris
```




> It could also be an empty string, which is commonly seen in things like the clearfix.
> ""안에 아무것도 안적을 수도 있음 clearfix처럼

### Counter = 카운터 

CSS counter 속성을 사용하기 위해서 `counter-reset`속성(초기값 0)을 사용해서 초기화 시켜야한다

*카운터 표시하기*

* Counter의 값은 content 속성에서 counter()나 counters() 함수를 사용하여 표시할 수 있습니다.

* counter() 함수는 'counter(name)'와 'counter(name, style)' 두 가지 형태로 사용할 수 있습니다. 생성된 텍스트는 가상 요소가 속한 범위에 있는 이름(name)의 가장 안쪽 counter의 값입니다. 텍스트는 지정된 서식(기본값은 십진수decimal)으로 뿌려집니다.

* counters() 함수도 'counters(name, string)'나 'counters(name, string, style)' 두 가지 형태로 사용할 수 있습니다. 생성된 텍스트는 가상 요소가 속한 모든 범위에서 지정된 이름을 가진 counters의 값으로, 바깥 쪽부터 안쪽까지 값이 주어지며 지정된 문자열로 구분됩니다. counters는 지정된 스타일(기본값은 십진수decimal)로 렌더링 됩니다.


예제 1 | 

```
body{
	counter-reset : myCounter; 
		/* myCounter라는 이름을 지정해주며 값은 0에서 시작함 */
}

h1::before{
	counter-increment : myCounter;
		/* 0에서 1씩 증가함 | 음수를 뒤에 추가하면 1씩 줄어듬 */
	content: counter(myCounter) "";
}

```

예제 2 |

```
body {
	counter-reset: mySecondCounter 40;
	/* mySecondCounterd의 시작 값을 40이로 지정 */
}
h1::after{
	counter-increment: mySecondCounter -10;
			/* 시작값 40에서 -10씩 줄어듬 */
	content=counter(mySecondCounter)"";
}
```

-> 화면에 첫번째 보이는 값은 30!


### Image = 이미지

예제 | 

```
div::before{
	content: url(image.jpg);
}
```

* This is literally an image on the page like <img> would be. It could also be a gradient. Note that you cannot change the dimensions of the image when inserted this way. You could also insert an image by using an empty string for the content, making it display: block in some way, sizing it, and using background-image. That way you could re-size it with background-size.

* 이미지를 배경으로 지정하는 거라서, 사이즈 조정을 하고 싶다면 background-size를 사용해서 크기 조정가능

### Attribute = 속성

예제 | 

* You can use values (strings, anyway) that are taken right from attributes in the HTML.

* HTML안의 속성들의 값을 넣을 수도 있다

```
<div data-visual-label="Widget Rating">60</div>
-
[data-visual-label]:before {
  content: attr(data-visual-label) ": ";
}
```



## 9월 19일 TIL

오늘 드디어 Webcafe 웹사이트 예제를 다 끝냈음ㅠㅠ세상 뿌듯함 휴
마지막 슬로건과 푸터 부분 디자인 할 때 선생님께서 시간을 주셔서 혼자 해봤는데, html & css 2주차에 드디어 스스로 만들었음! 수업시간에 다 만들고 소리지를뻔했는데 참음ㅋㅋㅋㅋㅋㅋㅋ그 성취감이란 캬_ 중간중간 나오는 개념들은 깃허브에 정리해서 올리고 있는데 아직 갈 길이 하아아아아아아아아아아-안참 남은듯하다. 그래도 즐기면서 끝까지 해보고 싶다ㅋㅋㅋㅋㅋ항상 하는 말이고 생각인데... 잘하는 사람보다 즐기면서하는 사람 못이긴다고ㅋㅋ끝까지 즐기면서 스트레스 최소한으로 받으며 공부 해봐야겠다! 그런의미롴ㅋㅋㅋㅋㅋㅋㅋㅋcss속성선택자 정리하고 집에 가야겠다