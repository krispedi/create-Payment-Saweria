# Saweria API Integration

This project provides a simple integration with the Saweria API to check the status of donations using QRIS. It offers an easy-to-use function to retrieve the status of a donation based on the provided donation ID.

## Requirements

- Node.js (v12 or higher)
- NPM (v6 or higher)
- [Axios](https://www.npmjs.com/package/axios) (for making HTTP requests)

## Installation

To get started with the project, follow these steps:

 API Request Example
To interact with the Saweria API, we provide a simple function that allows you to check the status of a donation. This function makes a GET request to the Saweria API, passing the donationId to retrieve the status.

cekStatus(donationId)
This function checks the donation status based on the provided donation ID.

Parameters:
donationId (string): The ID of the donation you want to check.
Returns:
An object containing the status and message of the donation:
status: Either false, true.
msg: A message that indicates the donation status 'PENDING' or 'SUKSES'.
qrString: The QR code string.
