## IR (Image Replacement)

Reference : 

* [C30: Using CSS to replace text with images of text and providing user interface controls to switch](https://www.w3.org/TR/WCAG20-TECHS/C30.html)


### Description [based on W3C]

* The objective of this technique is to demonstrate how CSS can be used to replace structured HTML text with images of text in a way that makes it possible for users to view content according to their preferences. To use this technique, an author starts by creating an HTML page that uses semantic elements to mark up the structure of the page. The author then designs two or more stylesheets for that page. One stylesheet presents the HTML text as text and the second uses CSS features to replace some of the HTML text with images of text. Finally, through the use of server-side or client-side scripting, the author provides a control that allows the user to switch between the available views.

* This technique can be used to meet Success Criterion 1.4.5 or 1.4.9 if a presentation that does not include images of text is available and as long as the user interface control that is provided to allow users to switch to an alternate presentation meets the relevant criteria. Where possible, authors should deliver the presentation that does not include images of text as the default presentation. In addition, the control used to switch should be located near the beginning of the page.

* A variety of "image replacement" techniques have been developed to address a variety of user agent, configuration and compatibility with assistive technology issues (See resources for more information). While there are a variety of approaches authors may use to replace text, it is important to consider compatibility with assistive technology, whether the technique will work correctly if scripting, CSS, images (or combinations of these) are turned off. Since it can be difficult to find a single solution that works in all cases, this technique recommends the use of a control that allows users to switch to a presentation that does not include an image replacement technique.


* 요약하면, 이 기술은 HTML의 텍스트 엘리먼트를 CSS를 사용하여 이미지로 교체하는 것을 가능하게 해준다. 예를 들면, 페이지의 로고이거나 제목일 수도 있다. 



**ir를 할 수 있는 여러가지 방법은 아래 링크를 참고하면된다.**

* [Nine Techniques for CSS Image Replacement](https://css-tricks.com/css-image-replacement/)



## Example 

수업시간에 작성한 코드는 다음과 같다.

There're many ways but, this is a HTML(using an internal stylesheet) I wrote in class to see how IR works. 

```
<!DOCTYPE html>
<html lang="ko-KR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>IR 기법</title>
    <style>
    .logo{
        box-sizing: border-box;
        position: relative;
        width: 290px;
        height: 195px;
        padding-top: 20px;
        text-align: center;
        font-size: 12px;
    }
    .logo::after{
        content: "";
        background: url("../images/title.png");
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
    }
    </style>
</head>
<body>
    <h1 class="logo">CSS Zen Garden</h1>
</body>
</html>

```

### CSS 코드 | Let's have a look at the CSS code


```
/* 스타일을 적용하기 위해 html파일 안 `<head>`영역 안에서 `<style>`시트를 생성한다 */

.logo{
        box-sizing: border-box;
        /* 너비, 높이속성가 컨텐트 안에 포함이 되어 패딩이나 
        	마진이 추가되어서 박스사이즈가 변하지 않는다 */
        position: relative;
        /* .logo뒤에 오는 이미지를 background로 가지는 가상요소의
        		배치를 위해 position:relative;로 선언한다 */
        width: 290px;
        height: 195px;
        /* 이미지의크기를 생각해서 높이와 너비 값을 지정한다 */
        padding-top: 20px;
        /* 이미지가 적용되었을 때 글씨가 위쪽으로 보이지 않게하기위해 위쪽으로 여백을 준다 */
        text-align: center;
        font-size: 12px;
    }
    .logo::after{
        content: "";
        background: url("../images/title.png");
        /* 가상요소를 생성해 배경을 깔아준다 */
        position: absolute;
        /* position:relative로 선언된 .logo를 기준으로 위치가 정해진다 */
        top: 0;
        left: 0;
        /* 왼쪽 상단에서부터 이미지가 시작된다 */
        width: 100%;
        height: 100%;
        /* .logo의 영역 전부에 적용된다 */
        
        '''
        
        <body>
    		<h1 class="logo">CSS Zen Garden</h1>
    		/* `<h1>`태그에 클래스 이름을 logo라고 지정한다 */
		 </body>


```



Today I learned :  

IR라는 기법을 사용해서 로고나 제목에 백그라운드 처리를해 
사용자가 보기에 그림처럼 보이는 효고를 줄 수 있다는 사실이 새로웠고, 많은 웹사이트들이 이러한 방법을 사용하고 있다는 사실에 또한 놀라웠다. 하지만 이러한 방법을 사용했을 때, 웹접근성이라는 부분에 대해서 생각을 더욱더 깊이 해야한다는 것도 알게되었다. 

만약, 내가 인터넷을 tab키나 커서로 선택되는 부분의 소리를 들어서 사용해야 할 경우에 이런식으로 내가 알아야할 부분에 이미지만 존재하고 아무런 설명이 나오지 않는다면, 기분이 썩 좋지는 않을 것 같기때문이당
 


