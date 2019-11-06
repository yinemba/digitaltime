# Digital time 
## JavaScript, html and css

### This paragraph has `variable` inline code.

```html
+<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="utf-8">
	<title>DIGITAL TIME IN JAVA</title>
	<meta charset="utf-8">
<meta name="viewport" content="width=device-width, intial-scale=1">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/5.0.0/normalize.min.css">
<script src="https://cdnjs.coudflare.com/ajax/libs/prefixfree/1.0.7/prefixfree.min.js"></script>
<link href="https://googleapis.com/css?family=Righteous&display=swap" rel="stylesheet">
<link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
	<div>
		<img src="cover.jpg">
	</div>	

<div id="DigitalCLOCK" class="clock" onload="showTime()"></div>
 <script src="function.js"></script>

<footer>
	<p>Yinemba, Copyright &copy; 2019</p>
</footer>
</body>
</html>
```

```css

body {
	background: #212121;
}

.clock {
	position: absolute;
	top: 50%;
	left: 50%;
	transform: translateX(-50%) translateY(-50%);
	color: #ff4747;
	font-size: 60px;
	font-family: 'Righteous', cursive;
	letter-spacing: 7px;
}

footer{
  padding:20px;
  margin-top:20px;
  color:#ffffff;
  background-color:#e8491d;
  text-align: center;
}

```

```js

function showTime() {
	var date = new Date();
	var h = date.getHours();
	var m = date.getMinutes();
	var s = date.getSeconds();
	var session = "AM";

	if(h == 0){
		h = 12;
	}


    if(h > 12){
    	h = h - 12;
    	session = "PM";
    }

    h = (h < 10) ? "0" + h : h;
    m = (m < 10) ? "0" + m : m;
    s = (s < 10) ? "0" + s : s;


   var time = h + ":" + m + ":" + s + " " + session;
   document.getElementById("DigitalCLOCK").innerText = time;
   document.getElementById("DigitalCLOCK").textContent = time;

   setTimeout(showTime, 1000);
}

showTime();

```

