<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>แจ้งเหตุ</title>
<script src="https://static.line-scdn.net/liff/edge/2/sdk.js"></script>
</head>
<body>
<h2>🚨 แจ้งเหตุฉุกเฉิน</h2>

<button onclick="sendAlert()">แจ้งเหตุ</button>

<script>
async function sendAlert() {
  await liff.init({ liffId: "2009090447-Nq66YDbS" });

  if (!liff.isLoggedIn()) {
    liff.login();
    return;
  }

  await liff.sendMessages([{
    type: "text",
    text: "🚨 แจ้งเหตุจากการสแกน QR Code"
  }]);

  alert("ส่งแจ้งเตือนแล้ว");
}
</script>
</body>
</html>
