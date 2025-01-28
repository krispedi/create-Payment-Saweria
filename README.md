# Kropa-API

Kropa-API adalah library Node.js sederhana untuk mempermudah akses ke berbagai fitur API yang Anda butuhkan. Pastikan menggunakan versi terbaru untuk pengalaman yang lebih baik.

---

## **Fitur**
- Placeholder untuk versi awal (v1.0.0).
- Versi terbaru berisi berbagai fitur API yang dapat membantu proyek Anda.

---

## **Instalasi**
Untuk menginstal Kropa-API, jalankan perintah berikut:

```sh
npm install kropaa-api@latest
```

## API Reference

####  Saweria Login
```bash 
const { loginSaweria } = require('kropaa-api');

loginSaweria('email@gmail.com', 'password')
    .then((res) => {
        console.log(res.data);
    })
    .catch((error) => {
        console.error(error.message);
    });
```
[Result](https://clayza.biz.id/ClayzaAubert/API-Sparkle-Docs/Result-Saweria-Login.json)

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `email` | `string` | **Required**. Your Email Saweria |
| `password` | `string` | **Required**. Your Password Saweria |
