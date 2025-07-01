# UBill\Sdk\SmsApi

All URIs are relative to https://api.ubill.dev/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createBrandName()**](SmsApi.md#createBrandName) | **POST** /sms/brandNameCreate | Create Brand Name |
| [**getDeliveryReport()**](SmsApi.md#getDeliveryReport) | **GET** /sms/report/{smsID} | Get Delivery Report |
| [**getSMSBalance()**](SmsApi.md#getSMSBalance) | **GET** /sms/balance | Get SMS Balance |
| [**listBrandNames()**](SmsApi.md#listBrandNames) | **GET** /sms/brandNames | Get All Brand Names |
| [**sendSMS()**](SmsApi.md#sendSMS) | **POST** /sms/send | Send SMS |


## `createBrandName()`

```php
createBrandName($createBrandNameRequest): \UBill\Sdk\Model\CreateBrandNameResponse
```

Create Brand Name

Register a new brand name for SMS messaging. Brand names are used to identify the sender of SMS messages (e.g., \"ubill-info\").

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = UBill\Sdk\Configuration::getDefaultConfiguration()->setApiKey('key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UBill\Sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('key', 'Bearer');


$apiInstance = new UBill\Sdk\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$createBrandNameRequest = new \UBill\Sdk\Model\CreateBrandNameRequest(); // \UBill\Sdk\Model\CreateBrandNameRequest | Brand Name payload to create

try {
    $result = $apiInstance->createBrandName($createBrandNameRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->createBrandName: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createBrandNameRequest** | [**\UBill\Sdk\Model\CreateBrandNameRequest**](../Model/CreateBrandNameRequest.md)| Brand Name payload to create | |

### Return type

[**\UBill\Sdk\Model\CreateBrandNameResponse**](../Model/CreateBrandNameResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `text/plain`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getDeliveryReport()`

```php
getDeliveryReport($smsID): \UBill\Sdk\Model\DeliveryReportResponse
```

Get Delivery Report

Fetch the delivery status of a previously sent SMS using its unique identifier.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = UBill\Sdk\Configuration::getDefaultConfiguration()->setApiKey('key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UBill\Sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('key', 'Bearer');


$apiInstance = new UBill\Sdk\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$smsID = 56; // int | Unique identifier of the SMS

try {
    $result = $apiInstance->getDeliveryReport($smsID);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->getDeliveryReport: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **smsID** | **int**| Unique identifier of the SMS | |

### Return type

[**\UBill\Sdk\Model\DeliveryReportResponse**](../Model/DeliveryReportResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/plain`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSMSBalance()`

```php
getSMSBalance(): \UBill\Sdk\Model\SMSBalanceResponse
```

Get SMS Balance

Retrieve your current SMS balance, indicating how many messages you can send.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = UBill\Sdk\Configuration::getDefaultConfiguration()->setApiKey('key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UBill\Sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('key', 'Bearer');


$apiInstance = new UBill\Sdk\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getSMSBalance();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->getSMSBalance: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\UBill\Sdk\Model\SMSBalanceResponse**](../Model/SMSBalanceResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/plain`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listBrandNames()`

```php
listBrandNames(): \UBill\Sdk\Model\BrandNamesResponse
```

Get All Brand Names

Retrieve a list of all registered brand names associated with your account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = UBill\Sdk\Configuration::getDefaultConfiguration()->setApiKey('key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UBill\Sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('key', 'Bearer');


$apiInstance = new UBill\Sdk\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listBrandNames();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->listBrandNames: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\UBill\Sdk\Model\BrandNamesResponse**](../Model/BrandNamesResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/plain`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `sendSMS()`

```php
sendSMS($sendSMSRequest): \UBill\Sdk\Model\SendSMSResponse
```

Send SMS

Send SMS messages to one or multiple recipients using a registered brand name.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = UBill\Sdk\Configuration::getDefaultConfiguration()->setApiKey('key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UBill\Sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('key', 'Bearer');


$apiInstance = new UBill\Sdk\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sendSMSRequest = new \UBill\Sdk\Model\SendSMSRequest(); // \UBill\Sdk\Model\SendSMSRequest | SMS payload for sending messages

try {
    $result = $apiInstance->sendSMS($sendSMSRequest);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->sendSMS: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sendSMSRequest** | [**\UBill\Sdk\Model\SendSMSRequest**](../Model/SendSMSRequest.md)| SMS payload for sending messages | |

### Return type

[**\UBill\Sdk\Model\SendSMSResponse**](../Model/SendSMSResponse.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `text/plain`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
