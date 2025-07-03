<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>XSS CSP Test</title>
  <!-- This CSP only works if no CSP headers are sent via HTTP -->
  <meta http-equiv="Content-Security-Policy"
        content="default-src *; style-src 'self' 'unsafe-inline'; script-src 'self' 'unsafe-inline' 'unsafe-eval' http://www.google.com">
</head>
<body>

<!-- External script (note: using http here will fail on https pages due to mixed content) -->
<script src="http://www.google.com/recaptcha/api.js?onload=myCallBack&render=explicit" async defer></script>

<!-- SVG XSS Payload -->
<svg xmlns="http://www.w3.org/2000/svg" onload="alert(document.domain)">
</svg>

</body>
</html>
