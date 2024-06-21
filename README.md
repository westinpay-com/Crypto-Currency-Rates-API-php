# Crypto-Currency-Rates-API-php
The WestinPay Currency Conversion API is a tool used for fast and reliable currency conversions by providing access to current and historical exchange rates. With this API, you can easily retrieve current and historical exchange rates for 32 different international currencies and seamlessly perform your transactions.


WestinPay's Free Crypto Currency API provides real-time exchange rates and currency conversion for all cryptocurrencies. It's ideal for financial apps, e-commerce platforms, and travel services.

## Endpoint

The WestinPay Crypto Currency Endpoint delivers real-time exchange rates.

### Authentication

Once you have created an account on [WestinPay](https://westinpay.com/merchant/register), your account will be assigned a unique 32-character API key. Think of this like a secure password; keep it safe and do not share it with others.

### Getting Your API Key

After registering, go to the dashboard and navigate to the "Currency Key" section. Here, you can generate your Fiat API key. This key is essential for authenticating your requests to the API.

### Parameters

- **base**: The base currency for conversion. Default is BTC. // For other currencies, use the currency symbol e.g. base=USDT
- **output**: Response format, either JSON or XML. Default is JSON.
- **api_key**: Your unique API key. Replace YOUR-API-KEY with your actual API key.

### Usage Limitations

Please note that your API key allows for up to 5000 monthly requests. This limit is automatically renewed each month. It's important to manage your usage to ensure continuous access to the API.
## WestinPay Crypto Currency PHP Code

```php
<?php
$api_key = 'your_api_key';
$base = 'BTC';
$output = 'JSON';
$url = "https://westinpay.com/currency/crypto_api?api_key=$api_key&base=$base&output=$output";

$response = file_get_contents($url);

if ($response !== FALSE) {
    $data = json_decode($response, true);
    print_r($data);
} else {
    echo "Error: Unable to fetch data";
}
?>
