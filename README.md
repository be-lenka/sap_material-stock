# OpenAPIClient-php

This service enables you to retrieve material stock information using the OData protocol with filter data provided in the payload. It can be consumed by external warehouse applications.


## Installation & Usage

### Requirements

PHP 7.4 and later.
Should also work with PHP 8.0.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\MaterialStock\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');

// Configure OAuth2 access token for authorization: OAuth2Auth
$config = BeLenka\SAP\MaterialStock\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new BeLenka\SAP\MaterialStock\Api\BatchRequestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->batchPost();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchRequestsApi->batchPost: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://:/sap/opu/odata/sap/API_MATERIAL_STOCK_SRV*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*BatchRequestsApi* | [**batchPost**](docs/Api/BatchRequestsApi.md#batchpost) | **POST** /$batch | Send a group of requests
*MaterialMasterApi* | [**aMaterialStockGet**](docs/Api/MaterialMasterApi.md#amaterialstockget) | **GET** /A_MaterialStock | Reads material ID and base unit of measure
*MaterialMasterApi* | [**aMaterialStockMaterialGet**](docs/Api/MaterialMasterApi.md#amaterialstockmaterialget) | **GET** /A_MaterialStock(&#39;{Material}&#39;) | Reads material ID and base unit of measure for a specific material
*MaterialMasterApi* | [**aMaterialStockMaterialToMatlStkInAcctModGet**](docs/Api/MaterialMasterApi.md#amaterialstockmaterialtomatlstkinacctmodget) | **GET** /A_MaterialStock(&#39;{Material}&#39;)/to_MatlStkInAcctMod | Reads material stock information for a specific material
*MaterialMasterApi* | [**aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeToMaterialStockGet**](docs/Api/MaterialMasterApi.md#amatlstkinacctmodmaterialmaterialplantplantstoragelocationstoragelocationbatchbatchsuppliersuppliercustomercustomerwbselementinternalidwbselementinternalidsddocumentsddocumentsddocumentitemsddocumentiteminventoryspecialstocktypeinventoryspecialstocktypeinventorystocktypeinventorystocktypetomaterialstockget) | **GET** /A_MatlStkInAcctMod(Material&#x3D;&#39;{Material}&#39;,Plant&#x3D;&#39;{Plant}&#39;,StorageLocation&#x3D;&#39;{StorageLocation}&#39;,Batch&#x3D;&#39;{Batch}&#39;,Supplier&#x3D;&#39;{Supplier}&#39;,Customer&#x3D;&#39;{Customer}&#39;,WBSElementInternalID&#x3D;&#39;{WBSElementInternalID}&#39;,SDDocument&#x3D;&#39;{SDDocument}&#39;,SDDocumentItem&#x3D;&#39;{SDDocumentItem}&#39;,InventorySpecialStockType&#x3D;&#39;{InventorySpecialStockType}&#39;,InventoryStockType&#x3D;&#39;{InventoryStockType}&#39;)/to_MaterialStock | Reads material stocks in account model for a specific set of stock identifiers including material ID and base unit
*MaterialStockApi* | [**aMaterialSerialNumberMaterialMaterialSerialNumberSerialNumberToMatlStkInAcctModGet**](docs/Api/MaterialStockApi.md#amaterialserialnumbermaterialmaterialserialnumberserialnumbertomatlstkinacctmodget) | **GET** /A_MaterialSerialNumber(Material&#x3D;&#39;{Material}&#39;,SerialNumber&#x3D;&#39;{SerialNumber}&#39;)/to_MatlStkInAcctMod | Get entities from related to_MatlStkInAcctMod
*MaterialStockApi* | [**aMaterialStockMaterialToMatlStkInAcctModGet**](docs/Api/MaterialStockApi.md#amaterialstockmaterialtomatlstkinacctmodget) | **GET** /A_MaterialStock(&#39;{Material}&#39;)/to_MatlStkInAcctMod | Reads material stock information for a specific material
*MaterialStockApi* | [**aMatlStkInAcctModGet**](docs/Api/MaterialStockApi.md#amatlstkinacctmodget) | **GET** /A_MatlStkInAcctMod | Reads material stocks in account model
*MaterialStockApi* | [**aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeGet**](docs/Api/MaterialStockApi.md#amatlstkinacctmodmaterialmaterialplantplantstoragelocationstoragelocationbatchbatchsuppliersuppliercustomercustomerwbselementinternalidwbselementinternalidsddocumentsddocumentsddocumentitemsddocumentiteminventoryspecialstocktypeinventoryspecialstocktypeinventorystocktypeinventorystocktypeget) | **GET** /A_MatlStkInAcctMod(Material&#x3D;&#39;{Material}&#39;,Plant&#x3D;&#39;{Plant}&#39;,StorageLocation&#x3D;&#39;{StorageLocation}&#39;,Batch&#x3D;&#39;{Batch}&#39;,Supplier&#x3D;&#39;{Supplier}&#39;,Customer&#x3D;&#39;{Customer}&#39;,WBSElementInternalID&#x3D;&#39;{WBSElementInternalID}&#39;,SDDocument&#x3D;&#39;{SDDocument}&#39;,SDDocumentItem&#x3D;&#39;{SDDocumentItem}&#39;,InventorySpecialStockType&#x3D;&#39;{InventorySpecialStockType}&#39;,InventoryStockType&#x3D;&#39;{InventoryStockType}&#39;) | Reads material stocks in account model for a specific set of stock identifiers
*MaterialStockApi* | [**aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeToMaterialSerialNumberGet**](docs/Api/MaterialStockApi.md#amatlstkinacctmodmaterialmaterialplantplantstoragelocationstoragelocationbatchbatchsuppliersuppliercustomercustomerwbselementinternalidwbselementinternalidsddocumentsddocumentsddocumentitemsddocumentiteminventoryspecialstocktypeinventoryspecialstocktypeinventorystocktypeinventorystocktypetomaterialserialnumberget) | **GET** /A_MatlStkInAcctMod(Material&#x3D;&#39;{Material}&#39;,Plant&#x3D;&#39;{Plant}&#39;,StorageLocation&#x3D;&#39;{StorageLocation}&#39;,Batch&#x3D;&#39;{Batch}&#39;,Supplier&#x3D;&#39;{Supplier}&#39;,Customer&#x3D;&#39;{Customer}&#39;,WBSElementInternalID&#x3D;&#39;{WBSElementInternalID}&#39;,SDDocument&#x3D;&#39;{SDDocument}&#39;,SDDocumentItem&#x3D;&#39;{SDDocumentItem}&#39;,InventorySpecialStockType&#x3D;&#39;{InventorySpecialStockType}&#39;,InventoryStockType&#x3D;&#39;{InventoryStockType}&#39;)/to_MaterialSerialNumber | Get entities from related to_MaterialSerialNumber
*MaterialStockApi* | [**aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeToMaterialStockGet**](docs/Api/MaterialStockApi.md#amatlstkinacctmodmaterialmaterialplantplantstoragelocationstoragelocationbatchbatchsuppliersuppliercustomercustomerwbselementinternalidwbselementinternalidsddocumentsddocumentsddocumentitemsddocumentiteminventoryspecialstocktypeinventoryspecialstocktypeinventorystocktypeinventorystocktypetomaterialstockget) | **GET** /A_MatlStkInAcctMod(Material&#x3D;&#39;{Material}&#39;,Plant&#x3D;&#39;{Plant}&#39;,StorageLocation&#x3D;&#39;{StorageLocation}&#39;,Batch&#x3D;&#39;{Batch}&#39;,Supplier&#x3D;&#39;{Supplier}&#39;,Customer&#x3D;&#39;{Customer}&#39;,WBSElementInternalID&#x3D;&#39;{WBSElementInternalID}&#39;,SDDocument&#x3D;&#39;{SDDocument}&#39;,SDDocumentItem&#x3D;&#39;{SDDocumentItem}&#39;,InventorySpecialStockType&#x3D;&#39;{InventorySpecialStockType}&#39;,InventoryStockType&#x3D;&#39;{InventoryStockType}&#39;)/to_MaterialStock | Reads material stocks in account model for a specific set of stock identifiers including material ID and base unit
*SerialNumbersWithMaterialStockApi* | [**aMaterialSerialNumberGet**](docs/Api/SerialNumbersWithMaterialStockApi.md#amaterialserialnumberget) | **GET** /A_MaterialSerialNumber | Get entities from A_MaterialSerialNumber
*SerialNumbersWithMaterialStockApi* | [**aMaterialSerialNumberMaterialMaterialSerialNumberSerialNumberGet**](docs/Api/SerialNumbersWithMaterialStockApi.md#amaterialserialnumbermaterialmaterialserialnumberserialnumberget) | **GET** /A_MaterialSerialNumber(Material&#x3D;&#39;{Material}&#39;,SerialNumber&#x3D;&#39;{SerialNumber}&#39;) | Get entity from A_MaterialSerialNumber by key
*SerialNumbersWithMaterialStockApi* | [**aMaterialSerialNumberMaterialMaterialSerialNumberSerialNumberToMatlStkInAcctModGet**](docs/Api/SerialNumbersWithMaterialStockApi.md#amaterialserialnumbermaterialmaterialserialnumberserialnumbertomatlstkinacctmodget) | **GET** /A_MaterialSerialNumber(Material&#x3D;&#39;{Material}&#39;,SerialNumber&#x3D;&#39;{SerialNumber}&#39;)/to_MatlStkInAcctMod | Get entities from related to_MatlStkInAcctMod
*SerialNumbersWithMaterialStockApi* | [**aMatlStkInAcctModMaterialMaterialPlantPlantStorageLocationStorageLocationBatchBatchSupplierSupplierCustomerCustomerWBSElementInternalIDWBSElementInternalIDSDDocumentSDDocumentSDDocumentItemSDDocumentItemInventorySpecialStockTypeInventorySpecialStockTypeInventoryStockTypeInventoryStockTypeToMaterialSerialNumberGet**](docs/Api/SerialNumbersWithMaterialStockApi.md#amatlstkinacctmodmaterialmaterialplantplantstoragelocationstoragelocationbatchbatchsuppliersuppliercustomercustomerwbselementinternalidwbselementinternalidsddocumentsddocumentsddocumentitemsddocumentiteminventoryspecialstocktypeinventoryspecialstocktypeinventorystocktypeinventorystocktypetomaterialserialnumberget) | **GET** /A_MatlStkInAcctMod(Material&#x3D;&#39;{Material}&#39;,Plant&#x3D;&#39;{Plant}&#39;,StorageLocation&#x3D;&#39;{StorageLocation}&#39;,Batch&#x3D;&#39;{Batch}&#39;,Supplier&#x3D;&#39;{Supplier}&#39;,Customer&#x3D;&#39;{Customer}&#39;,WBSElementInternalID&#x3D;&#39;{WBSElementInternalID}&#39;,SDDocument&#x3D;&#39;{SDDocument}&#39;,SDDocumentItem&#x3D;&#39;{SDDocumentItem}&#39;,InventorySpecialStockType&#x3D;&#39;{InventorySpecialStockType}&#39;,InventoryStockType&#x3D;&#39;{InventoryStockType}&#39;)/to_MaterialSerialNumber | Get entities from related to_MaterialSerialNumber

## Models

- [AMaterialSerialNumberType](docs/Model/AMaterialSerialNumberType.md)
- [AMaterialStockType](docs/Model/AMaterialStockType.md)
- [AMatlStkInAcctModType](docs/Model/AMatlStkInAcctModType.md)
- [APIMATERIALSTOCKSRVAMaterialSerialNumberType](docs/Model/APIMATERIALSTOCKSRVAMaterialSerialNumberType.md)
- [APIMATERIALSTOCKSRVAMaterialSerialNumberTypeCreate](docs/Model/APIMATERIALSTOCKSRVAMaterialSerialNumberTypeCreate.md)
- [APIMATERIALSTOCKSRVAMaterialSerialNumberTypeCreateToMatlStkInAcctMod](docs/Model/APIMATERIALSTOCKSRVAMaterialSerialNumberTypeCreateToMatlStkInAcctMod.md)
- [APIMATERIALSTOCKSRVAMaterialSerialNumberTypeToMatlStkInAcctMod](docs/Model/APIMATERIALSTOCKSRVAMaterialSerialNumberTypeToMatlStkInAcctMod.md)
- [APIMATERIALSTOCKSRVAMaterialSerialNumberTypeUpdate](docs/Model/APIMATERIALSTOCKSRVAMaterialSerialNumberTypeUpdate.md)
- [APIMATERIALSTOCKSRVAMaterialStockType](docs/Model/APIMATERIALSTOCKSRVAMaterialStockType.md)
- [APIMATERIALSTOCKSRVAMaterialStockTypeCreate](docs/Model/APIMATERIALSTOCKSRVAMaterialStockTypeCreate.md)
- [APIMATERIALSTOCKSRVAMaterialStockTypeUpdate](docs/Model/APIMATERIALSTOCKSRVAMaterialStockTypeUpdate.md)
- [APIMATERIALSTOCKSRVAMatlStkInAcctModType](docs/Model/APIMATERIALSTOCKSRVAMatlStkInAcctModType.md)
- [APIMATERIALSTOCKSRVAMatlStkInAcctModTypeCreate](docs/Model/APIMATERIALSTOCKSRVAMatlStkInAcctModTypeCreate.md)
- [APIMATERIALSTOCKSRVAMatlStkInAcctModTypeCreateToMaterialSerialNumber](docs/Model/APIMATERIALSTOCKSRVAMatlStkInAcctModTypeCreateToMaterialSerialNumber.md)
- [APIMATERIALSTOCKSRVAMatlStkInAcctModTypeToMaterialSerialNumber](docs/Model/APIMATERIALSTOCKSRVAMatlStkInAcctModTypeToMaterialSerialNumber.md)
- [APIMATERIALSTOCKSRVAMatlStkInAcctModTypeUpdate](docs/Model/APIMATERIALSTOCKSRVAMatlStkInAcctModTypeUpdate.md)
- [CollectionOfAMaterialSerialNumberType](docs/Model/CollectionOfAMaterialSerialNumberType.md)
- [CollectionOfAMaterialStockType](docs/Model/CollectionOfAMaterialStockType.md)
- [CollectionOfAMatlStkInAcctModType](docs/Model/CollectionOfAMatlStkInAcctModType.md)
- [Error](docs/Model/Error.md)
- [ErrorError](docs/Model/ErrorError.md)
- [ErrorErrorMessage](docs/Model/ErrorErrorMessage.md)
- [Wrapper](docs/Model/Wrapper.md)
- [Wrapper1](docs/Model/Wrapper1.md)
- [Wrapper2](docs/Model/Wrapper2.md)

## Authorization

Authentication schemes defined for the API:
### OAuth2Auth

- **Type**: `OAuth`
- **Flow**: `accessCode`
- **Authorization URL**: `https://{host}:{port}`
- **Scopes**: 
    - **API_MATERIAL_STOCK_SRV_0001**: 

### BasicAuth

- **Type**: HTTP basic authentication

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `1.1.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
