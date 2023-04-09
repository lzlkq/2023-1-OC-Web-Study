# 기초 웹 스터디 4주차

**HTML과 WEB**

- HTML : Hyper Txt Markup Language, 하이퍼링크의 텍스트
- World Wide Web project : 최초의 웹사이트
    
    [https://www.w3.org/History/19921103-hypertext/hypertext/WWW/TheProject.html](https://www.w3.org/History/19921103-hypertext/hypertext/WWW/TheProject.html) 
    

**HTML 기본 골격**

- tag
    - 일종의 꼬리표
    - html, head, title, body, h1…
    - 열면 닫아줘야 한다.
    - 가끔씩 하나 짜리도 있다. ex. <br>
- attribute : 속성, 태그가 가지는 속성을 정해줄 수 있다.
- f11에서 요소를 보면 css태그를 볼 수 있다.

**TAG**

```html
<!DOCTYPE html> <!--document type html-->
<html>
	<head> <!--html문서이고 여기 안에 내용이 다 있다.-->
		<meta> <!-- 문서가 어떤 내용을 담고 있고, 문서의 키워드는 무엇인지, 누가 만들었는지 등의 문서 자체의 특성을 담고 있다.-->
		<title> </title> <!--title 빼고는 화면에 안 나온다. 컴퓨터나 프로그램에게 정보를 준다.-->
	</head>
	
	<body> <!--우리가 실제로 보는 부분, 웹사이트의 렌더링 할 몸통-->
		<h1>제목이나 주제를 표현할 때 쓴다.</h1>
		<b>글자를 굵게 표현한다. html의 스타일을 정의</b>
		<strong>글자를 굵게 표현한다. html의 의미를 정의</strong>
		<mark>형관펜이 칠해진다.</mark>
		<ins>밑줄이 표시된다.</ins>
		
		<ul> <!--목록 태그, unordered list-->
			<li>검은색 점</li>
		</ul>

		<table border="1"> <!--table : 표, border : 표의 경계선 두께-->
			<tr> <!--행-->
				<td>열</td>
				<td></td>
			</tr>
		</table>

		<br> <!--break, 줄 바꿈-->
		<p>paragraph, 단락</p>

		<label for="animal-name">동물 이름 : </label>
		<input type="text" id="animal-name" placeholder="동물 이름을 입력하세." autofocus>
		<!-- label : input태그의 의미를 정의하기 위한 태그, input : 입력창 생성, placeholder : 입력창 설명, autofocus : 커서 위치-->
	</body>
</html>
```

- <meta> : 문서에 대한 메타적인 정보를 적어놓았다. 인코딩이나 웹사이트를 설명한다. 검색 엔진, 시각장애인을 위한 프로그램에도 쓰인다.