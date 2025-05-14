# scan.html
<!DOCTYPE html>
<html>
<head><meta charset="utf-8"><title>QR Scanner</title></head>
<body>
  <div id="reader" style="width:100%"></div>
  <script src="https://unpkg.com/html5-qrcode"></script>
  <script>
    function onScanSuccess(decodedText) {
      // sostituisci APP_ID con il tuo appId Glide
      const glideUrl = 
        `https://go.glideapps.app/app/APP_ID?last_scan=${encodeURIComponent(decodedText)}`;
      window.location.href = glideUrl;
    }
    new Html5Qrcode("reader")
      .start({ facingMode: "environment" }, {}, onScanSuccess);
  </script>
</body>
</html>
