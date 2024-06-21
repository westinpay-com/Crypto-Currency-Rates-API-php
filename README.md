# Crypto-Currency-Rates-API-php
The WestinPay Currency Conversion API is a tool used for fast and reliable currency conversions by providing access to current and historical exchange rates. With this API, you can easily retrieve current and historical exchange rates for 32 different international currencies and seamlessly perform your transactions.


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
