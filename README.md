# Calculator-App
My Project

<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>SIMPLE CALCULATOR</title>


	<style type="text/css">


				body
				{
					background-image: url("peni.jpg");
					background-repeat: no-repeat;
					background-position: center;
					background-color: #cc9900;
				}
		
				.calculator
				{
					padding: 10px;
					border-radius: 10px;
					height: 740px;
					width: 600px;
					margin: auto;
					background-color: #ffffff;
					box-shadow: rgba(0, 0, 0, 0.2)0px 10px 20px, rgba(0, 0, 0, 0.23)0px 6px 8px;
					background-color: #ccccff;

				}

				.display-box
				{

					font-family: 'orbitron',sans-serif;
					background-color: #e41338;
					border: 1px solid black;
					border-radius: 4px;
					height: 60%;
					width: 106%;
					font-size: 240%;
					color: black;
				}

				#btn
				{
					background-color: #e41338;
					border-radius: 10px;

				
				}

				input[type=button]{
										font-family:'orbitron',sans-serif ;
										background-color:#d9d2d3 ;
										border: 1px solid white;
										border-radius: 10px;
										color: black;
										width: 90%;
										height: 50%;
										outline: none;
										font-size: xx-large;
									}

				input:active[type=button]{

					background-color: #cdccb9;
					box-shadow: inset 0px 0px 5px black;
				}


	</style>

</head>
<body>

		<table class="calculator">
			<tr>
				<td colspan="3"><input type="text" class="display-box" id="result" disabled></td>

			<tr>
				<td><input type="button" value="7" onclick="display('7')"></td>
				<td><input type="button" value="8" onclick="display('8')"></td>
				<td><input type="button" value="9" onclick="display('9')"></td>
				<td><input type="button" value="+" onclick="display('+')"></td>

			</tr>
			<tr>
				<td><input type="button" value="4" onclick="display('4')"></td>
				<td><input type="button" value="5" onclick="display('5')"></td>
				<td><input type="button" value="6" onclick="display('6')"></td>
				<td><input type="button" value="-" onclick="display('-')"></td>
			</tr>
			<tr>
				<td><input type="button" value="1" onclick="display('1')"></td>
				<td><input type="button" value="2" onclick="display('2')"></td>
				<td><input type="button" value="3" onclick="display('3')"></td>
				<td><input type="button" value="*" onclick="display('*')"></td>
			<tr>
				<td><input type="button" value="0" onclick="display('0')"></td>
				<td><input type="button" value="C" id="btn" onclick="clearScreen()"></td>
				<td><input type="button" value="/" onclick="display('/')"></td>
				<td><input type="button" value="=" id="btn" onclick="calculate()"></td>
			</tr>
			
		</table>

		<script type="text/javascript">
			
			function clearScreen()
				{
					document.getElementById('result').value="";
				}

			function display(value)
				{
					document.getElementById('result').value+=value;
				}

			function calculate(value)
				{
					var p=document.getElementById('result').value;
					var q=eval(p);
					document.getElementById('result').value=q;
				}
		</script>

</body>
</html>
