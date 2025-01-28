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
```javascript 
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

####  Saweria Create Payment

Berikut adalah format data yang digunakan untuk melakukan request donation:

| Field            | Value                   | Type       | Description                                               |
|------------------|-------------------------|------------|-----------------------------------------------------------|
| `amount`         | `1000`                  | number     | Jumlah donasi (dalam satuan yang sesuai)                  |
| `message`        | `'Haii'`                | string     | Pesan yang ingin disampaikan oleh donatur                 |
| `anonymous`      | `true`                  | boolean    | Apakah donasi anonim atau tidak                           |
| `payment_type`   | `'qris'`                | string     | Jenis pembayaran yang digunakan (misalnya QRIS)           |
| `customer_info`  |                         | object     | Informasi tentang pelanggan                               |
| `- name`         | `'Saya kris'`           | string     | Nama pelanggan                                            |
| `- email`        | `'ssss@gmail.com'`      | string     | Email pelanggan                                           |
| `- phone`        | `'085786544568'`        | string     | Nomor telepon pelanggan                                   |

```javascript
const { createSaweria } = require('kropaa-api');

const donationData = {
  amount: 1000,
  message: 'Haii',
  anonymous: true,
  payment_type: 'qris',
  customer_info: {
  name: 'Saya kris',
  email: 'ssss@gmail.com',
  phone: '085786544568',
   },
 };
 
createSaweria('userId', 'Apikey', donationData)
  .then((res) => {
        console.log(res.data);
    })
    .catch((error) => {
        console.error(error.message);
    });
```
