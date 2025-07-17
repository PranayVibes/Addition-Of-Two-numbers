<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Addition Calculator</title>
  <style>
    body {
      background: linear-gradient(to right, #6a11cb, #2575fc);
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    .calculator {
      background-color: #ffffffdd;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 8px 16px rgba(0,0,0,0.3);
      text-align: center;
      max-width: 350px;
      width: 100%;
    }

    .calculator h2 {
      color: #333;
      margin-bottom: 20px;
    }

    .input-field {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      font-size: 18px;
      border-radius: 10px;
      border: 2px solid #ccc;
      transition: 0.3s;
    }

    .input-field:focus {
      border-color: #2575fc;
      outline: none;
    }

    .btn {
      background-color: #2575fc;
      color: white;
      border: none;
      padding: 12px 25px;
      border-radius: 10px;
      font-size: 16px;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    .btn:hover {
      background-color: #6a11cb;
    }

    .result {
      margin-top: 20px;
      font-size: 20px;
      font-weight: bold;
      color: #444;
    }
  </style>
</head>
<body>

  <div class="calculator">
    <h2>Add Two Numbers</h2>
    <input type="number" id="num1" class="input-field" placeholder="Enter first number">
    <input type="number" id="num2" class="input-field" placeholder="Enter second number">
    <button class="btn" onclick="addNumbers()">Add</button>
    <div class="result" id="result"></div>
  </div>

  <script>
    function addNumbers() {
      const n1 = parseFloat(document.getElementById("num1").value);
      const n2 = parseFloat(document.getElementById("num2").value);
      const result = n1 + n2;
      document.getElementById("result").textContent = `Result: ${result}`;
    }
  </script>

</body>
</html>
