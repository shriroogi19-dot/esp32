# Alcohol Detection Website - Vercel version

Structure:
- public/index.html   the website (served at /)
- api/send-sms.js     sends the SMS (serverless function)
- api/health.js       status check

## Deploy
Option A (GitHub): push this folder to a GitHub repo, then Vercel > Add New > Project > import it.
  Framework Preset: "Other". Leave build settings empty.
Option B (CLI): install Node.js, then in this folder run:  npx vercel   (and  npx vercel --prod)

## Set SMS keys
Vercel > Project > Settings > Environment Variables: add SMS_PROVIDER (+ FAST2SMS_API_KEY or the TWILIO_* ones).
Redeploy after adding them.

## Use
Open your https://....vercel.app link in Chrome on an Android phone (or PC), add phone numbers,
press "Send test SMS", then connect to the ESP32. Keep the page open near the car.
Set ACCESS_CODE on Vercel so strangers cannot use your SMS credit, and enter it in the site settings.
