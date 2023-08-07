## 오늘은 html, css, jsp를 이용하여 움직이는 웹사이트 만들기
#### feat.로그인화면, 회원가입

### [움직이는 사이트 꾸미기]
![image](https://github.com/hwan06/Web/assets/114748934/17d36082-e22a-4ee3-9891-0183897e63ea)
### [로그인 화면]
![image](https://github.com/hwan06/Web/assets/114748934/84ecb74b-636e-464a-b342-bf7c68c56ccf)
### [회원가입 화면]
![image](https://github.com/hwan06/Web/assets/114748934/3771f40a-75b9-4a39-ab12-a4368ee6b684)

### [메뉴바 js 코드]
``` js
$(".main-menu > li").mouseover(function(){
	$(this).children(".sub").stop().slideDown();
});

$(".main-menu > li").mouseleave(function(){
	$(this).children(".sub").stop().slideUp();
});
```
#### 마우스를 올려둘 때, 안올려둘 때 메뉴바 표시, 메뉴바 숨기기
---
### [사진 바꾸는 js 코드]
``` js
function start(){
	$(".imgs>img").eq(0).siblings().css({"margin-left":"-2000px"});
	setInterval(function(){slide();}, 2000);
}

function slide(){
	now = now == imgs? 0:now+=1;
	$(".imgs>img").eq(now-1).css({"margin-left":"-2000px"});
	$(".imgs>img").eq(now).css({"margin-left":"0px"});
}
```
---
### [로그인, 회원가입 js 코드]
``` js
function winOpen1(){
	var win1 = window.open('login.html','child1','toolbar = no, location = no, status = no, menubar = no, resizable = no, scrollbars = no, width = 700, height = 700')
}

function winOpen2(){
	var win2 = window.open('user.html','child2','toolbar = no, location = no, status = no, menubar = no, resizable = no, scrollbars = no, width = 1850, height = 1700')
}
```
---
### [현재 시각 js 코드]
``` js
const todayDiv = document.getElementById("notice");
		
function getTime(){
	let now = new Date();
	let year = now.getUTCFullYear();
	let month = now.getMonth();
	let date = now.getDate();
	let hour = now.getHours();
	let min = now.getMinutes();
	let second = now.getSeconds();
	
	month = month < 10 ? `0${month}` : month;
	date = date < 10 ? `0${date}` : date;
	hour = hour < 10 ? `0${hour}` : hour;
	min = min < 10 ? `0${min}` : min;
	second = second < 10 ? `0${second}` : second;
	todayDiv.textContent = `공지사항(${year}년 ${month}월 ${date}일 ${hour}시 ${min}분)`
	console.log(todayDiv.textContent)
}

setInterval(getTime, 1000)
```
#### 함수getTime()을 만들어서 Date객체를 이용하여 현재 시간을 가져와 화면에 출력한다.
