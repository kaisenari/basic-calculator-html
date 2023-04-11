# basic-calculator-html
creating a basic calculator on html
<!DOCTYPE html>
<html>
<head>
	<title>Calculator</title>
</head>
<body>
	<h1>Calculator</h1>
	<form>
		<input type="text" name="num1" placeholder="Enter first number">
		<br>
		<input type="text" name="num2" placeholder="Enter second number">
		<br>
		<label>Select operation:</label>
		<br>
		<select name="operator">
			<option value="+">Addition</option>
			<option value="-">Subtraction</option>
			<option value="*">Multiplication</option>
			<option value="/">Division</option>
		</select>
		<br>
		<button type="submit">Calculate</button>
	</form>

	<?php
		if(isset($_GET['num1']) && isset($_GET['num2']) && isset($_GET['operator'])){
			$num1 = $_GET['num1'];
			$num2 = $_GET['num2'];
			$operator = $_GET['operator'];

			switch ($operator) {
				case '+':
					$result = $num1 + $num2;
					break;
				case '-':
					$result = $num1 - $num2;
					break;
				case '*':
					$result = $num1 * $num2;
					break;
				case '/':
					$result = $num1 / $num2;
					break;
				default:
					$result = "Invalid operator";
					break;
			}

			echo "<p>Result: $result</p>";
		}
	?>
</body>
</html>

