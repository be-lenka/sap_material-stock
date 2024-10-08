# BeLenka\SAP\MaterialStock\MaterialStockApi

All URIs are relative to https://:/sap/opu/odata/sap/API_MATERIAL_STOCK_SRV, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**aMaterialSerialNumberMaterialMaterialSerialNumberSerialNumberToMatlStkInAcctModGet()**](MaterialStockApi.md#aMaterialSerialNumberMaterialMaterialSerialNumberSerialNumberToMatlStkInAcctModGet) | **GET** /A_MaterialSerialNumber(Material&#x3D;&#39;{Material}&#39;,SerialNumber&#x3D;&#39;{SerialNumber}&#39;)/to_MatlStkInAcctMod | Get entities from related to_MatlStkInAcctMod |
| [**aMaterialStockMaterialToMatlStkInAcctModGet()**](MaterialStockApi.md#aMaterialStockMaterialToMatlStkInAcctModGet) | **GET** /A_MaterialStock(&#39;{Material}&#39;)/to_MatlStkInAcctMod | Reads material stock information for a specific material |
| [**aMatlStkInAcctModGet()**](MaterialStockApi.md#aMatlStkInAcctModGet) | **GET** /A_MatlStkInAcctMod | Reads material stocks in account model |
| [**aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeGet()**](MaterialStockApi.md#aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeGet) | **GET** /A_MatlStkInAcctMod(Material&#x3D;&#39;{Material}&#39;,Plant&#x3D;&#39;{Plant}&#39;,StorageLocation&#x3D;&#39;{StorageLocation}&#39;,Batch&#x3D;&#39;{Batch}&#39;,Supplier&#x3D;&#39;{Supplier}&#39;,Customer&#x3D;&#39;{Customer}&#39;,WBSElementInternalID&#x3D;&#39;{WBSElementInternalID}&#39;,SDDocument&#x3D;&#39;{SDDocument}&#39;,SDDocumentItem&#x3D;&#39;{SDDocumentItem}&#39;,InventorySpecialStockType&#x3D;&#39;{InventorySpecialStockType}&#39;,InventoryStockType&#x3D;&#39;{InventoryStockType}&#39;) | Reads material stocks in account model for a specific set of stock identifiers |
| [**aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeToMaterialSerialNumberGet()**](MaterialStockApi.md#aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeToMaterialSerialNumberGet) | **GET** /A_MatlStkInAcctMod(Material&#x3D;&#39;{Material}&#39;,Plant&#x3D;&#39;{Plant}&#39;,StorageLocation&#x3D;&#39;{StorageLocation}&#39;,Batch&#x3D;&#39;{Batch}&#39;,Supplier&#x3D;&#39;{Supplier}&#39;,Customer&#x3D;&#39;{Customer}&#39;,WBSElementInternalID&#x3D;&#39;{WBSElementInternalID}&#39;,SDDocument&#x3D;&#39;{SDDocument}&#39;,SDDocumentItem&#x3D;&#39;{SDDocumentItem}&#39;,InventorySpecialStockType&#x3D;&#39;{InventorySpecialStockType}&#39;,InventoryStockType&#x3D;&#39;{InventoryStockType}&#39;)/to_MaterialSerialNumber | Get entities from related to_MaterialSerialNumber |
| [**aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeToMaterialStockGet()**](MaterialStockApi.md#aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeToMaterialStockGet) | **GET** /A_MatlStkInAcctMod(Material&#x3D;&#39;{Material}&#39;,Plant&#x3D;&#39;{Plant}&#39;,StorageLocation&#x3D;&#39;{StorageLocation}&#39;,Batch&#x3D;&#39;{Batch}&#39;,Supplier&#x3D;&#39;{Supplier}&#39;,Customer&#x3D;&#39;{Customer}&#39;,WBSElementInternalID&#x3D;&#39;{WBSElementInternalID}&#39;,SDDocument&#x3D;&#39;{SDDocument}&#39;,SDDocumentItem&#x3D;&#39;{SDDocumentItem}&#39;,InventorySpecialStockType&#x3D;&#39;{InventorySpecialStockType}&#39;,InventoryStockType&#x3D;&#39;{InventoryStockType}&#39;)/to_MaterialStock | Reads material stocks in account model for a specific set of stock identifiers including material ID and base unit |


## `aMaterialSerialNumberMaterialMaterialSerialNumberSerialNumberToMatlStkInAcctModGet()`

```php
aMaterialSerialNumberMaterialMaterialSerialNumberSerialNumberToMatlStkInAcctModGet($material, $serial_number, $top, $skip, $filter, $inlinecount, $orderby, $select, $expand): \BeLenka\SAP\MaterialStock\Model\Wrapper1
```

Get entities from related to_MatlStkInAcctMod

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\MaterialStock\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');

// Configure OAuth2 access token for authorization: OAuth2Auth
$config = BeLenka\SAP\MaterialStock\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BeLenka\SAP\MaterialStock\Api\MaterialStockApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$material = 'material_example'; // string | Material Number
$serial_number = 'serial_number_example'; // string | Serial Number
$top = 50; // int | Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=66)
$skip = 56; // int | Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$filter = 'filter_example'; // string | Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=64)
$inlinecount = 'inlinecount_example'; // string | Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=67)
$orderby = array('orderby_example'); // string[] | Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aMaterialSerialNumberMaterialMaterialSerialNumberSerialNumberToMatlStkInAcctModGet($material, $serial_number, $top, $skip, $filter, $inlinecount, $orderby, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MaterialStockApi->aMaterialSerialNumberMaterialMaterialSerialNumberSerialNumberToMatlStkInAcctModGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **material** | **string**| Material Number | |
| **serial_number** | **string**| Serial Number | |
| **top** | **int**| Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;66) | [optional] |
| **skip** | **int**| Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **filter** | **string**| Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;64) | [optional] |
| **inlinecount** | **string**| Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;67) | [optional] |
| **orderby** | [**string[]**](../Model/string.md)| Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **select** | [**string[]**](../Model/string.md)| Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;68) | [optional] |
| **expand** | [**string[]**](../Model/string.md)| Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;63) | [optional] |

### Return type

[**\BeLenka\SAP\MaterialStock\Model\Wrapper1**](../Model/Wrapper1.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth), [OAuth2Auth](../../README.md#OAuth2Auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aMaterialStockMaterialToMatlStkInAcctModGet()`

```php
aMaterialStockMaterialToMatlStkInAcctModGet($material, $top, $skip, $filter, $inlinecount, $orderby, $select, $expand): \BeLenka\SAP\MaterialStock\Model\Wrapper1
```

Reads material stock information for a specific material

Reads material stock information in the account model for a specific material for which a certain stock has been posted.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\MaterialStock\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');

// Configure OAuth2 access token for authorization: OAuth2Auth
$config = BeLenka\SAP\MaterialStock\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BeLenka\SAP\MaterialStock\Api\MaterialStockApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$material = 'material_example'; // string | Material Number
$top = 50; // int | Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=66)
$skip = 56; // int | Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$filter = 'filter_example'; // string | Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=64)
$inlinecount = 'inlinecount_example'; // string | Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=67)
$orderby = array('orderby_example'); // string[] | Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aMaterialStockMaterialToMatlStkInAcctModGet($material, $top, $skip, $filter, $inlinecount, $orderby, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MaterialStockApi->aMaterialStockMaterialToMatlStkInAcctModGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **material** | **string**| Material Number | |
| **top** | **int**| Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;66) | [optional] |
| **skip** | **int**| Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **filter** | **string**| Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;64) | [optional] |
| **inlinecount** | **string**| Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;67) | [optional] |
| **orderby** | [**string[]**](../Model/string.md)| Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **select** | [**string[]**](../Model/string.md)| Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;68) | [optional] |
| **expand** | [**string[]**](../Model/string.md)| Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;63) | [optional] |

### Return type

[**\BeLenka\SAP\MaterialStock\Model\Wrapper1**](../Model/Wrapper1.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth), [OAuth2Auth](../../README.md#OAuth2Auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aMatlStkInAcctModGet()`

```php
aMatlStkInAcctModGet($top, $skip, $filter, $inlinecount, $orderby, $select, $expand): \BeLenka\SAP\MaterialStock\Model\Wrapper1
```

Reads material stocks in account model

Reads material stocks in account model for which a certain stock has been posted.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\MaterialStock\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');

// Configure OAuth2 access token for authorization: OAuth2Auth
$config = BeLenka\SAP\MaterialStock\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BeLenka\SAP\MaterialStock\Api\MaterialStockApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$top = 50; // int | Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=66)
$skip = 56; // int | Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$filter = 'filter_example'; // string | Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=64)
$inlinecount = 'inlinecount_example'; // string | Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=67)
$orderby = array('orderby_example'); // string[] | Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aMatlStkInAcctModGet($top, $skip, $filter, $inlinecount, $orderby, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MaterialStockApi->aMatlStkInAcctModGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **top** | **int**| Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;66) | [optional] |
| **skip** | **int**| Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **filter** | **string**| Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;64) | [optional] |
| **inlinecount** | **string**| Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;67) | [optional] |
| **orderby** | [**string[]**](../Model/string.md)| Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **select** | [**string[]**](../Model/string.md)| Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;68) | [optional] |
| **expand** | [**string[]**](../Model/string.md)| Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;63) | [optional] |

### Return type

[**\BeLenka\SAP\MaterialStock\Model\Wrapper1**](../Model/Wrapper1.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth), [OAuth2Auth](../../README.md#OAuth2Auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeGet()`

```php
aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeGet($material, $plant, $storage_location, $batch, $supplier, $customer, $wbs_element_internal_id, $sd_document, $sd_document_item, $inventory_special_stock_type, $inventory_stock_type, $select, $expand): \BeLenka\SAP\MaterialStock\Model\AMatlStkInAcctModType
```

Reads material stocks in account model for a specific set of stock identifiers

Reads material stocks in account model for which a certain stock has been posted for a specific set of stock identifiers.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\MaterialStock\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');

// Configure OAuth2 access token for authorization: OAuth2Auth
$config = BeLenka\SAP\MaterialStock\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BeLenka\SAP\MaterialStock\Api\MaterialStockApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$material = 'material_example'; // string | Material in Respect of Which Stock is Managed
$plant = 'plant_example'; // string | Plant
$storage_location = 'storage_location_example'; // string | Storage Location
$batch = 'batch_example'; // string | Batch Number (Stock Identifier)
$supplier = 'supplier_example'; // string | Supplier for Special Stock
$customer = 'customer_example'; // string | Customer for Special Stock
$wbs_element_internal_id = 'wbs_element_internal_id_example'; // string | WBS Element
$sd_document = 'sd_document_example'; // string | Sales order number of valuated sales order stock
$sd_document_item = 'sd_document_item_example'; // string | Sales Order Item of Valuated Sales Order Stock
$inventory_special_stock_type = 'inventory_special_stock_type_example'; // string | Special Stock Type
$inventory_stock_type = 'inventory_stock_type_example'; // string | Stock Type of Goods Movement (Stock Identifier)
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeGet($material, $plant, $storage_location, $batch, $supplier, $customer, $wbs_element_internal_id, $sd_document, $sd_document_item, $inventory_special_stock_type, $inventory_stock_type, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MaterialStockApi->aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **material** | **string**| Material in Respect of Which Stock is Managed | |
| **plant** | **string**| Plant | |
| **storage_location** | **string**| Storage Location | |
| **batch** | **string**| Batch Number (Stock Identifier) | |
| **supplier** | **string**| Supplier for Special Stock | |
| **customer** | **string**| Customer for Special Stock | |
| **wbs_element_internal_id** | **string**| WBS Element | |
| **sd_document** | **string**| Sales order number of valuated sales order stock | |
| **sd_document_item** | **string**| Sales Order Item of Valuated Sales Order Stock | |
| **inventory_special_stock_type** | **string**| Special Stock Type | |
| **inventory_stock_type** | **string**| Stock Type of Goods Movement (Stock Identifier) | |
| **select** | [**string[]**](../Model/string.md)| Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;68) | [optional] |
| **expand** | [**string[]**](../Model/string.md)| Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;63) | [optional] |

### Return type

[**\BeLenka\SAP\MaterialStock\Model\AMatlStkInAcctModType**](../Model/AMatlStkInAcctModType.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth), [OAuth2Auth](../../README.md#OAuth2Auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeToMaterialSerialNumberGet()`

```php
aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeToMaterialSerialNumberGet($material, $plant, $storage_location, $batch, $supplier, $customer, $wbs_element_internal_id, $sd_document, $sd_document_item, $inventory_special_stock_type, $inventory_stock_type, $top, $skip, $filter, $inlinecount, $orderby, $select, $expand): \BeLenka\SAP\MaterialStock\Model\Wrapper
```

Get entities from related to_MaterialSerialNumber

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\MaterialStock\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');

// Configure OAuth2 access token for authorization: OAuth2Auth
$config = BeLenka\SAP\MaterialStock\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BeLenka\SAP\MaterialStock\Api\MaterialStockApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$material = 'material_example'; // string | Material in Respect of Which Stock is Managed
$plant = 'plant_example'; // string | Plant
$storage_location = 'storage_location_example'; // string | Storage Location
$batch = 'batch_example'; // string | Batch Number (Stock Identifier)
$supplier = 'supplier_example'; // string | Supplier for Special Stock
$customer = 'customer_example'; // string | Customer for Special Stock
$wbs_element_internal_id = 'wbs_element_internal_id_example'; // string | WBS Element
$sd_document = 'sd_document_example'; // string | Sales order number of valuated sales order stock
$sd_document_item = 'sd_document_item_example'; // string | Sales Order Item of Valuated Sales Order Stock
$inventory_special_stock_type = 'inventory_special_stock_type_example'; // string | Special Stock Type
$inventory_stock_type = 'inventory_stock_type_example'; // string | Stock Type of Goods Movement (Stock Identifier)
$top = 50; // int | Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=66)
$skip = 56; // int | Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$filter = 'filter_example'; // string | Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=64)
$inlinecount = 'inlinecount_example'; // string | Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=67)
$orderby = array('orderby_example'); // string[] | Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeToMaterialSerialNumberGet($material, $plant, $storage_location, $batch, $supplier, $customer, $wbs_element_internal_id, $sd_document, $sd_document_item, $inventory_special_stock_type, $inventory_stock_type, $top, $skip, $filter, $inlinecount, $orderby, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MaterialStockApi->aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeToMaterialSerialNumberGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **material** | **string**| Material in Respect of Which Stock is Managed | |
| **plant** | **string**| Plant | |
| **storage_location** | **string**| Storage Location | |
| **batch** | **string**| Batch Number (Stock Identifier) | |
| **supplier** | **string**| Supplier for Special Stock | |
| **customer** | **string**| Customer for Special Stock | |
| **wbs_element_internal_id** | **string**| WBS Element | |
| **sd_document** | **string**| Sales order number of valuated sales order stock | |
| **sd_document_item** | **string**| Sales Order Item of Valuated Sales Order Stock | |
| **inventory_special_stock_type** | **string**| Special Stock Type | |
| **inventory_stock_type** | **string**| Stock Type of Goods Movement (Stock Identifier) | |
| **top** | **int**| Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;66) | [optional] |
| **skip** | **int**| Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **filter** | **string**| Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;64) | [optional] |
| **inlinecount** | **string**| Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;67) | [optional] |
| **orderby** | [**string[]**](../Model/string.md)| Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **select** | [**string[]**](../Model/string.md)| Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;68) | [optional] |
| **expand** | [**string[]**](../Model/string.md)| Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;63) | [optional] |

### Return type

[**\BeLenka\SAP\MaterialStock\Model\Wrapper**](../Model/Wrapper.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth), [OAuth2Auth](../../README.md#OAuth2Auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeToMaterialStockGet()`

```php
aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeToMaterialStockGet($material, $plant, $storage_location, $batch, $supplier, $customer, $wbs_element_internal_id, $sd_document, $sd_document_item, $inventory_special_stock_type, $inventory_stock_type, $select, $expand): \BeLenka\SAP\MaterialStock\Model\AMaterialStockType
```

Reads material stocks in account model for a specific set of stock identifiers including material ID and base unit

Reads material stocks in account model for which a certain stock has been posted for a specific set of stock identifiers including material ID and base unit.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\MaterialStock\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');

// Configure OAuth2 access token for authorization: OAuth2Auth
$config = BeLenka\SAP\MaterialStock\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BeLenka\SAP\MaterialStock\Api\MaterialStockApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$material = 'material_example'; // string | Material in Respect of Which Stock is Managed
$plant = 'plant_example'; // string | Plant
$storage_location = 'storage_location_example'; // string | Storage Location
$batch = 'batch_example'; // string | Batch Number (Stock Identifier)
$supplier = 'supplier_example'; // string | Supplier for Special Stock
$customer = 'customer_example'; // string | Customer for Special Stock
$wbs_element_internal_id = 'wbs_element_internal_id_example'; // string | WBS Element
$sd_document = 'sd_document_example'; // string | Sales order number of valuated sales order stock
$sd_document_item = 'sd_document_item_example'; // string | Sales Order Item of Valuated Sales Order Stock
$inventory_special_stock_type = 'inventory_special_stock_type_example'; // string | Special Stock Type
$inventory_stock_type = 'inventory_stock_type_example'; // string | Stock Type of Goods Movement (Stock Identifier)
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeToMaterialStockGet($material, $plant, $storage_location, $batch, $supplier, $customer, $wbs_element_internal_id, $sd_document, $sd_document_item, $inventory_special_stock_type, $inventory_stock_type, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MaterialStockApi->aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeToMaterialStockGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **material** | **string**| Material in Respect of Which Stock is Managed | |
| **plant** | **string**| Plant | |
| **storage_location** | **string**| Storage Location | |
| **batch** | **string**| Batch Number (Stock Identifier) | |
| **supplier** | **string**| Supplier for Special Stock | |
| **customer** | **string**| Customer for Special Stock | |
| **wbs_element_internal_id** | **string**| WBS Element | |
| **sd_document** | **string**| Sales order number of valuated sales order stock | |
| **sd_document_item** | **string**| Sales Order Item of Valuated Sales Order Stock | |
| **inventory_special_stock_type** | **string**| Special Stock Type | |
| **inventory_stock_type** | **string**| Stock Type of Goods Movement (Stock Identifier) | |
| **select** | [**string[]**](../Model/string.md)| Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;68) | [optional] |
| **expand** | [**string[]**](../Model/string.md)| Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;63) | [optional] |

### Return type

[**\BeLenka\SAP\MaterialStock\Model\AMaterialStockType**](../Model/AMaterialStockType.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth), [OAuth2Auth](../../README.md#OAuth2Auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
