# Individual
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
</head>

<body>
	<form name="app">
	<input type="button" value="Выполнить" onclick="run()">
	</form>
	<div id="result"></div>
</body>

<script>
	function Palindrom(number) {
		var n=number;
		var d = n, s = 0;
		var d2 = n.toString(2), s2 = 0;
		while (d > 0) {
			s = s * 10 + d % 10;
			d = Math.floor(d / 10);
		}
		while (d2 > 0) {
			s2 = s2 * 10 + d2 % 10;
			d2 = Math.floor(d2 / 10);
		}
		var res = document.getElementById('result');
		if (n == s && n.toString(2) == s2)
			res.innerHTML = res.innerHTML + n + ", ";
	}

	function run() {
		for (var i = 1; i < 1000000; i++)
			Palindrom(i);		
	}
</script>
</html>
