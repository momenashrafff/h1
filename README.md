<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>XSS Test</title>
</head>
<body>
  <h1>Testing SVG XSS</h1>
  <svg xmlns="http://www.w3.org/2000/svg" onload="alert('SVG XSS on github.io')"></svg>
</body>
</html>
