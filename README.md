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

#### Get Apikey
`Silahkan hubungi develover kami untuk mendapatkan Apikey`
- [Hubungi saya di Telegram](https://t.me/csegenix21)  
- [Hubungi saya di WhatsApp](https://wa.me/62882007324217)  
- Kirim email ke [krispedia1@gmail.com](mailto:krispedia1@gmail.com)

####  Saweria Login
```bash 
const { loginSaweria } = require('kropaa-api');

loginSaweria('email@gmail.com', 'password', 'apikey')
    .then((res) => {
        console.log(res.data);
    })
    .catch((error) => {
        console.error(error.message);
    });
```
[Result](https://github.com/krispedi/create-Payment-Saweria/response-login.json)

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `email` | `string` | **Required**. Your Email Saweria |
| `password` | `string` | **Required**. Your Password Saweria |
