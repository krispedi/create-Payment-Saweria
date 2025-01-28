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

| Field | Type     | Description                |
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

*Contoh response*
```json
{
  powered: 'Powered By KropaApi',
  status: true,
  data: {
    data: {
      amount: 1000,
      amount_raw: 1000,
      created_at: 'Tue, 28 Jan 2025 11:10:41 GMT',
      currency: 'IDR',
      donator: [Object],
      donator_id: null,
      etc: [Object],
      id: '99df170b-0973-463f-9d8a-68cb7602af2d',
      message: 'Haii',
      need_notification: false,
      payment_type: 'qris',
      qr_string: '00020101021226570011ID.DANA.WWW011893600915016937059202091693705920303UME51440014ID.CO.QRIS.WWW0215ID20210917307330303UME520473925303360540410005802ID5907saweria6015Kota Jakarta Pu61051034062720115Q4YcjGk4XhN57KZ60490011ID.DANA.WWW0425MER202107140077450960864105011630437A5',
      status: 'PENDING',
      type: 'donation',
      user_id: '5a583c72-7883-4bf4-a49b-bf0fac243944'
    }
  }
}
```
