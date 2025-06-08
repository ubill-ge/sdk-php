# UBill\Sdk\SmsApi

All URIs are relative to https://api.ubill.dev/v1, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createBrandName()**](SmsApi.md#createBrandName) | **POST** /sms/brandNameCreate | Create Brand Name |
| [**getBalance()**](SmsApi.md#getBalance) | **GET** /sms/balance | Get SMS Balance |
| [**getBrandNames()**](SmsApi.md#getBrandNames) | **GET** /sms/brandNames | Get All Brand Names |
| [**getDeliveryReport()**](SmsApi.md#getDeliveryReport) | **GET** /sms/report/{smsID} | Get Delivery Report |
| [**send()**](SmsApi.md#send) | **POST** /sms/send | Send SMS |


## `createBrandName()`

```php
createBrandName($createBrandNamePayload): \UBill\Sdk\Model\CreateBrandNameResponse
```

Create Brand Name

Register a new brand name for SMS messaging. Brand names are used to identify the sender of SMS messages (e.g., \"ubill-info\").

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = UBill\Sdk\Configuration::getDefaultConfiguration()->setApiKey('key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UBill\Sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('key', 'Bearer');


$apiInstance = new UBill\Sdk\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$createBrandNamePayload = new \UBill\Sdk\Model\CreateBrandNamePayload(); // \UBill\Sdk\Model\CreateBrandNamePayload | Brand Name payload to create

try {
    $result = $apiInstance->createBrandName($createBrandNamePayload);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->createBrandName: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **createBrandNamePayload** | [**\UBill\Sdk\Model\CreateBrandNamePayload**](../Model/CreateBrandNamePayload.md)| Brand Name payload to create | [optional] |

### Return type

[**\UBill\Sdk\Model\CreateBrandNameResponse**](../Model/CreateBrandNameResponse.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `text/plain`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getBalance()`

```php
getBalance(): \UBill\Sdk\Model\SMSBalanceResponse
```

Get SMS Balance

Retrieve your current SMS balance, indicating how many messages you can send.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
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
    $result = $apiInstance->getBalance();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->getBalance: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\UBill\Sdk\Model\SMSBalanceResponse**](../Model/SMSBalanceResponse.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/plain`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getBrandNames()`

```php
getBrandNames(): \UBill\Sdk\Model\BrandNamesResponse
```

Get All Brand Names

Retrieve a list of all registered brand names associated with your account.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
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
    $result = $apiInstance->getBrandNames();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->getBrandNames: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\UBill\Sdk\Model\BrandNamesResponse**](../Model/BrandNamesResponse.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
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


// Configure API key authorization: api_key
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

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `text/plain`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `send()`

```php
send($sMSPayload): \UBill\Sdk\Model\SendSMSResponse
```

Send SMS

Send SMS messages to one or multiple recipients using a registered brand name.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: api_key
$config = UBill\Sdk\Configuration::getDefaultConfiguration()->setApiKey('key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = UBill\Sdk\Configuration::getDefaultConfiguration()->setApiKeyPrefix('key', 'Bearer');


$apiInstance = new UBill\Sdk\Api\SmsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$sMSPayload = new \UBill\Sdk\Model\SMSPayload(); // \UBill\Sdk\Model\SMSPayload | SMS payload for sending messages

try {
    $result = $apiInstance->send($sMSPayload);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SmsApi->send: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sMSPayload** | [**\UBill\Sdk\Model\SMSPayload**](../Model/SMSPayload.md)| SMS payload for sending messages | [optional] |

### Return type

[**\UBill\Sdk\Model\SendSMSResponse**](../Model/SendSMSResponse.md)

### Authorization

[api_key](../../README.md#api_key)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `text/plain`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
