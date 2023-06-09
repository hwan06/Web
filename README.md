## 오늘은 html, css, js를 이용하여 움직이는 웹사이트 만들기
#### feat.로그인화면, 회원가입

### [움직이는 SCP 사이트 꾸미기]
![image](https://github.com/hwan06/Web/assets/114748934/261d257f-3a91-4a93-91fe-c0e115ba4c61)
### [로그인 화면]
![image](https://github.com/hwan06/Web/assets/114748934/84ecb74b-636e-464a-b342-bf7c68c56ccf)
### [회원가입 화면]
![image](https://github.com/hwan06/Web/assets/114748934/db612a2f-f288-441f-8d24-39d1b7f424ab)
### [메인 화면 html 코드]
``` html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Insert title here</title>
<link rel = "stylesheet" href = "css/style.css" type = "text/css">
<script src = "https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js" defer = "defer"></script>
<script src = "js/script.js" defer = "defer"></script>
</head>
<body>
<div id = "page">
	<header>
		<div id = "logo">
			<img src = "imgs/logo.png" alt="style size" style="width:250px; height:100px">
		 </div>
		 
		 <div id = "top">
		 	<ul class = "main-menu">
	 			<li>
 					<a href = "#">SCP소개</a>
 						<ul class = "sub">
 							<li><a href = "#">SCP란?</a>
 							<li><a href = "#">SCP의 유래</a>
 							<li><a href = "#">SCP등급</a>
 							<li><a href = "#">SCP</a>
 						</ul> 
		 			</li>
		 			<li>
 					<a href = "#">위험도</a>
 						<ul class = "sub">
 							<li><a href = "#">안전(Safe)</a>
 							<li><a href = "#">유클리드(Euclid)</a>
 							<li><a href = "#">케테르(Keter)</a>
 							<li><a href = "#">타우미엘(Thaumiel)</a>
 						</ul> 
		 			</li>
		 			<li>
 					<a href = "#">SCP시리즈</a>
 						<ul class = "sub">
 							<li><a href = "#">시리즈ⅰ</a>
 							<li><a href = "#">시리즈ⅱ</a>
 							<li><a href = "#">시리즈ⅲ</a>
 							<li><a href = "#">시리즈ⅳ</a>
 						</ul> 
		 			</li>
		 			<li>
 					<a href = "#">계정 생성</a>
 						<ul class = "sub">
 							<li onclick="winOpen1()"><a href = "#">로그인</a>
 							<li onclick="winOpen2()"><a href = "#">회원가입</a>
 						</ul> 
		 			</li>
		 	</ul>
		 </div>
	</header>
	<div class = "clear"></div>
	
	<section>
			<div class = "imgs">
				<img src = "imgs/다운로드.jpg">
				<img src = "imgs/main_img2.jpg">
				<img src = "imgs/main_img3.jpg">
				<img src = "imgs/logo.png">  
				<div class = "welcome">
					<h2><span>SCP단체에 오신 것을 환영합니다.</span></h2>
				</div>
			</div>	
	</section>
	<div class = "clear"></div>
		
			<div class = "notice">
				<h2>공지사항</h2>
				<table class = "table">
				<tr>
					<th>내용</th>
					<th>날짜</th>
				</tr>
				<tr>
					<td><a href = "#">SCP 사진 모음</a>
					<td>2022-06-01</td>
				</tr>
				<tr>
					<td><a href = "#">실험 결과 확인</a>
					<td>2022-08-01</td>
				</tr>
				<tr>
					<td><a href = "#">사건/사고</a>
					<td>2022-10-01</td>
				</tr>
				<tr>
					<td><a href = "#">격리 현황</a>
					<td>2022-11-01</td>
				</tr>
				<tr>
					<td><a href = "#">건의사항</a>
					<td>2022-12-01</td>
				</tr>
				</table>
			
			</div>
		<div class = "clear"></div>
		 
		<footer>
		<div id = "address" align = "center">
			<img src = "imgs/address.png" alt="style size" style="width:250px; height:100px"> 
		</div>
		</footer>
</div>



</body>
</html>
```
### [로그인 화면 html 코드]
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>로그인페이지</title>
</head>
<body>
    <form> 
        <p>ID : <input type = "text" size="20"> </p>
        <p> Password : <input type = "password" size="30"></p>
        <p> <input type="submit" value="확인"> <input type="reset" value="취소"></p>
    </form>
    
</body>
</html>
```
### [회원가입 화면 html 코드]
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Insert title here</title>
<style>
body{
	font-size : 14px;
	font-family: 돋움;
}

table{
	width : 800px;
	margin : 0 auto;
}

table, tr, th, td{
	border : 1px solid #333;
	border-spacing : 0;
}

strong{color : red;}
caption {
	text-align : right;
}

th, td{
	padding : 10px 15px;
}

span{color : red;}

th{text-align : right;}

#btn{float : right;}
</style>
</head>
<body>
<form> 
<table>
<caption>(*)표시는 <strong> 필수입력</strong> 입니다.</caption>
<tr>
	<th><span>*</span>회원유형</th>
	<td>학생</td>
</tr>
<tr>
	<th><span>*</span>이름(실명)</th>
	<td>홍길동</td>
</tr>
<tr>
	<th><span>*</span>아이디</th>
	<td><p><input type = "text" size="20"></p>
	<p>6~15자의 영문소문자, 숫자만 가능합니다.</p>
	</td>
</tr>
	
<tr>
<th><span>*</span>비밀번호</th>
<td><p><input type = "password" size="20"></p>
<p>비밀번호는 <strong> 영댜문자, 영소문자, 숫자, 특수문자의 조합</strong> 으로 이루어져야합니다<br>
- 조합이 2종류 이상인 경우 10자리 이상<br>
- 조합이 3종류 이상인 경우 8자리 이상 가능합니다.
</td>
</tr>

<tr>
<th><span>*</span>비밀번호 확인</th>
<td><input type = "password" size="20"></td>
</tr>

<tr>
<td colspan = '2'><p>SCP 단체에 가입하시겠습니까?<span id = "btn">
<input type="submit" value="확인">&nbsp; <input type="reset" value="취소"></span></td>

</tr> 
</table>
</form> 
</body>
</html>
```

### [js 풀코드]
``` javascript
$(".main-menu > li").mouseover(function(){
	$(this).children(".sub").stop().slideDown();
});

$(".main-menu > li").mouseleave(function(){
	$(this).children(".sub").stop().slideUp();
});

start();
var imgs = 5;
var now = 0;

function start(){
	$(".imgs>img").eq(0).siblings().css({"margin-left":"-2000px"});
	setInterval(function(){slide();}, 2000);
}

function slide(){
	now = now == imgs? 0:now+=1;
	$(".imgs>img").eq(now-1).css({"margin-left":"-2000px"});
	$(".imgs>img").eq(now).css({"margin-left":"0px"});
}

function winOpen1(){
	var win1 = window.open('login.html','child1','toolbar = no, location = no, status = no, menubar = no, resizable = no, scrollbars = no, width = 700, height = 700')
}

function winOpen2(){
	var win2 = window.open('user.html','child2','toolbar = no, location = no, status = no, menubar = no, resizable = no, scrollbars = no, width = 1850, height = 1700')
}
```
### [css 풀코드]
``` css
@charset "UTF-8";
*{
	padding : 0px;
	margin : 0px;
}


a{
	color:inherit;
	text-decoration: none;
}

li{
	list-style: none;
	
}



#logo{
	float : left;
	margin-top : 20px;
	}
#page{
	width : 995px;
	margin : 0 auto;
}

header{
	width : 995px;
	height : 120px;
	margin-top : 10px;
	border : solid 1px #cccccc;
}

#top{
	float: right;
	margin : 20px 20px 0 0;
}

.main-menu{
	width : 600px;
	height : 40px;
	margin-top : 10px;
	background-color: maroon;
	line-height : 40px;
	color : white;
}

.main-menu li{
	float :left;
	width : 150px;
	text-align : center;
	
}
.main-menu li:hover{
	color :blueviolet;
	background-color: white;
}

.sub {
	position: absolute;
	width : 150px;
	background-color: #aabbdd;
	display: none;
	z-index: 1;
}

.sub li:hover{
	background-color: #aabbdd;
}

.clear{
	clear: both;
}

section{
	width : 995px;
	height : 240px;
	float : left;
	margin-top: 10px;
	align-content: center;
}

.imgs{
	width : 995px;
	height : 220px;
	position: absolute;
	overflow: hidden;
}

.imgs>img{
	position: absolute;
	transition : all 2s;
}

.welcome {
	position: relative;
	text-align: center;
	margin: -35px 0 0 -350px !important;
	width : 750px;
	height : 50px;
	line-height : 50px;
	background-color: #000000;
	border-radius: 30px;
	left: 50%;
	top: 50%;
}
span{
	color: #FF0000; 
}

.notice{
	width : 995px;
	margin-top : 10px;
	float : left;
}

h2{
	text-align : center;
}

.table{
	width : 995px;
	border-collapse: collapse;
	font-size : 1rem;
	color : #000000;
}

.table tr>th{
	padding : 5px;
}

.table tr>td{
	padding : 5px;
	text-align: center;
}

.table tr:nth-child(2n){
	background-color: maroon;
}

footer{
	width : 995px;
	height : 130px;
	border-top: solid 1px #cccccc;
	margin-top : 20px;
}

address{
	margin : 30px 0 0 50px;
}



```
