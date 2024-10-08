# BeLenka\SAP\MaterialStock\MaterialMasterApi

All URIs are relative to https://:/sap/opu/odata/sap/API_MATERIAL_STOCK_SRV, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**aMaterialStockGet()**](MaterialMasterApi.md#aMaterialStockGet) | **GET** /A_MaterialStock | Reads material ID and base unit of measure |
| [**aMaterialStockMaterialGet()**](MaterialMasterApi.md#aMaterialStockMaterialGet) | **GET** /A_MaterialStock(&#39;{Material}&#39;) | Reads material ID and base unit of measure for a specific material |
| [**aMaterialStockMaterialToMatlStkInAcctModGet()**](MaterialMasterApi.md#aMaterialStockMaterialToMatlStkInAcctModGet) | **GET** /A_MaterialStock(&#39;{Material}&#39;)/to_MatlStkInAcctMod | Reads material stock information for a specific material |
| [**aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeToMaterialStockGet()**](MaterialMasterApi.md#aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeToMaterialStockGet) | **GET** /A_MatlStkInAcctMod(Material&#x3D;&#39;{Material}&#39;,Plant&#x3D;&#39;{Plant}&#39;,StorageLocation&#x3D;&#39;{StorageLocation}&#39;,Batch&#x3D;&#39;{Batch}&#39;,Supplier&#x3D;&#39;{Supplier}&#39;,Customer&#x3D;&#39;{Customer}&#39;,WBSElementInternalID&#x3D;&#39;{WBSElementInternalID}&#39;,SDDocument&#x3D;&#39;{SDDocument}&#39;,SDDocumentItem&#x3D;&#39;{SDDocumentItem}&#39;,InventorySpecialStockType&#x3D;&#39;{InventorySpecialStockType}&#39;,InventoryStockType&#x3D;&#39;{InventoryStockType}&#39;)/to_MaterialStock | Reads material stocks in account model for a specific set of stock identifiers including material ID and base unit |


## `aMaterialStockGet()`

```php
aMaterialStockGet($top, $skip, $filter, $inlinecount, $orderby, $select, $expand): \BeLenka\SAP\MaterialStock\Model\Wrapper2
```

Reads material ID and base unit of measure

Reads material ID and base unit of measure for which a certain stock has been posted.

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


$apiInstance = new BeLenka\SAP\MaterialStock\Api\MaterialMasterApi(
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
    $result = $apiInstance->aMaterialStockGet($top, $skip, $filter, $inlinecount, $orderby, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MaterialMasterApi->aMaterialStockGet: ', $e->getMessage(), PHP_EOL;
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

[**\BeLenka\SAP\MaterialStock\Model\Wrapper2**](../Model/Wrapper2.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth), [OAuth2Auth](../../README.md#OAuth2Auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aMaterialStockMaterialGet()`

```php
aMaterialStockMaterialGet($material, $select, $expand): \BeLenka\SAP\MaterialStock\Model\AMaterialStockType
```

Reads material ID and base unit of measure for a specific material

Reads material ID and base unit of measure for which a certain stock has been posted for a specific material.

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


$apiInstance = new BeLenka\SAP\MaterialStock\Api\MaterialMasterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$material = 'material_example'; // string | Material Number
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aMaterialStockMaterialGet($material, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MaterialMasterApi->aMaterialStockMaterialGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **material** | **string**| Material Number | |
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


$apiInstance = new BeLenka\SAP\MaterialStock\Api\MaterialMasterApi(
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
    echo 'Exception when calling MaterialMasterApi->aMaterialStockMaterialToMatlStkInAcctModGet: ', $e->getMessage(), PHP_EOL;
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


$apiInstance = new BeLenka\SAP\MaterialStock\Api\MaterialMasterApi(
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
    echo 'Exception when calling MaterialMasterApi->aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeToMaterialStockGet: ', $e->getMessage(), PHP_EOL;
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
