# CSS Sprites


* Image Sprites

	* An image sprite is a collection of images put into a single image.

	* A web page with many images can take a long time to load and generates multiple server requests.

	* Using image sprites will reduce the number of server requests and save bandwidth.

* 이미지 스프라이츠

	* 여러개의 이미지들을 하나의 이미지로 만드는 것
	
	* 여러개의 이미지를 포함한 웹페이지는 로딩되는데 많은 시간이 걸리기 때문에 이러한 방법이 더 효과적 (to make a web page load faster!)


예제 | 

css코드 작성법

1. 이미지를 삽입시켜줄 태그가 inline속성이라면 display:block;으로 재선언해준다
2. text-indent: -999px(width값에 안에 없는 범위면 뭐든 가능);


	* 글씨를 들여쓰기 해줘서 화면에 출력되지 않게 함

	white-space: nowrap; 
	
	* 지정해준 크기 보다 컨텐츠가 크면 튀어나감
	
	overflow: hidden;  
	
	* 넘치는 부분을 보이지 않게함

3. 배경이미지가 들어갈 부분의 width, height값을 지정

4. 만약 세로로 3개의 그림이 있다고 가정했을때, 두번째의 그림이 화면에 출력되길 원한다면! background-position: 0 -(음수값)을 지정해줌


참조 : 

> LearnWebCode : [CSS Sprites tutorial](https://youtu.be/d-O5rYbJjr4)

## TIL

이틀에 걸쳐서 image replacement와 sprites에 대한 개념정리를 끝냈다ㅠㅠ 솔직히 처음엔 그냥 이미지 파일 만들어서 위치를 조정하는 게 훨씬더 효율적이지 않을까라는 생각을 했었는데, 이 두 기법을 배우고 나서 생각을 고쳐먹었다. 심지어 이미지가 많아질 수록 화면 로딩 속도도 느려진다는 것을 알고나니 왜 미쳐 그 생각은 하지 못했을까라는 생각도 들었다. 알면 알수록 고려해야할 요소가 너무 많고, 찾아 읽어볼 레퍼런스도 너무 많고, 볼 유투브 영상도 너무 많다ㅋㅋ이렇게 원하는 정보 검색하다 검색왕이 될 것만 같다ㅋㅋㅋㅋㅋㅋ그것도..괜찮은데..? 오늘도 수고했음ㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋㅋ



	