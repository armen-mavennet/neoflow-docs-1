# API User Guide

`Vaish`

This document provides the guide to getting started on the Neoflow platform and integrate with the REST APIs exposed. The intended audience is a software developer well acquainted with REST APIs and JSON. With that knowledge, the Swagger API Documentation will be the best place to start testing and exploring the platform APIs.

talk about onboarding here?

## Swagger API Documentation

The REST APIs in Neoflow follow the OpenAPI standard specifications. These APIs are documented using the famous [Swagger tool](https://swagger.io/), which provides developers to interact and execute API calls directly from the Swagger UI.

[Environment links]() which envs prod/staging?

## Authentication

TODO: how are we portraying the NF picture as? Invite-only platform? APIKEY or Cognito Managed setup's JWT?

## Products

A product can be any Oil or Gas commodity in Neoflow. The product information is stored in the form of a verifiable credential issued by the organization who created it. Presently, Neoflow supports below set of commodities for Oil and Gas & electricity -

Below are the set of functions that can be carried out on the product. Please be sure to have the authentication material at hand before beginning to work with the API endpoints.

### 1. Creation

The products can be created and fetched in the Neoflow platform using below set of API endpoints. When a product is created, a corresponding creation of the product event is also stored in Neoflow. Each product and the event is uniquely identified with a UUID. 

> POST /v1/products  
> GET /v1/products  
> GET /v1/products/{id}  


### 2. Transformation

Within a lifecycle of the product(s), the owner of the product(s) can upgrade, refine, blend, pool and split into multiple child products. Every new transformed child product issues a verifiable credential. Eg. Bitumen and Naphtha can be upgraded to Crude Oil. Gasoline can be split into multiple gasoline batches. Each transformation is stored as an event associated to the product.

> POST /v1/products/transform

### 3. Ownership transfer

The ownership transfer of the product is carried out in three steps - 
1. The current owner organization creates an ownership transfer request for the product with the prospective new owner of the product.
2. The prospective new owner receives the request, can fetch/review the information in the request and either accept it or request for change in the transfer request.
3. If the request is accepted by the prospective new owner then the current owner can actually make the transfer of product to the new owner. This will create a transfer of ownership event which will be associated to the product. If the changes are requested then the current owner can make corresponding changes and start with step 2.

> POST /v1/products/transferownership/requests  
> PUT /v1/products/transferownership/requests  
> POST /v1/products/transferownership/confirm  
> POST /v1/products/transferownership  
> POST /v1/products/transfer/requests  
> DELETE /v1/products/transfer/requests  

### 4. Custody transfer

The custody transfer of the product follows similar three steps process as ownership transfer - 
1. The current owner or the custodian organization creates a custody transfer request for the product with the prospective new custodian of the product.
2. The prospective new custodian receives the request, can fetch/review the information in the request and either accept it or request for change in the transfer request.
3. If the request is accepted by the prospective new custodian then the current owner or the custodian can actually make the custody transfer of product to the new custodian. This will create a transfer of custody event which will be associated to the product. If the changes are requested then the current owner can make corresponding changes and start with step 2.

> POST /v1/products/transfercustody/requests  
> PUT /v1/products/transfercustody/requests  
> POST /v1/products/transfercustody/confirm  
> POST /v1/products/transfercustody  
> POST /v1/products/transfer/requests  
> DELETE /v1/products/transfer/requests  

### 5. Transport

The custodian organization transports the product from one location to another. This movement is recorded in Neoflow in the form of `start` and `end` transport events. Bill of Lading details are captured at during this process. Transport events support correction of the details using the VC revocation standards. 

> POST /v1/products/transport  
> PUT /v1/products/transport  

### 6. Storage

The owner or custodian organization stores the product at a given tank location. This is recorded in Neoflow as `start` event - indicating the product is in storage at the tank location and `end` event - indicating the product is out of storage.

> POST /v1/products/storage  

### 7. Entry Summary

The owner of the product should first share the product with the broker organization. The broker can then access the product and add the entry summary (also called as QP Inbond) details on the product. This is stored as an event on Neoflow. Neoflow supports correction of the entry summary details using the VC revocation standards.

> POST /v1/products/QPInBond  
> PUT /v1/products/QPInBond  

### 8. Inspection

The owner or custodian organization can inspect the product for its physical and chemical specifications at any point of time. The inspection result is recorded as event in Neoflow.

> POST /v1/products/inspect  

### 9. Certify

The owner can claim the U.S.-Mexico-Canada Agreement (USMCA) benefits for the product by certifying the product with the requested set of fields as per USMCA guidelines. 

> POST /v1/products/certify  

### 10. Share

The owner of the product can share or unshare the product with another organization(s). If the product is shared, an organization can access all the product details such as product's physical and chemical specifications, associated events with their location of occurrence, origin, product's composition/traceablility hierarchy and uploaded documents if any.

> POST /v1/products/share  
> GET /v1/products/share  
> DELETE /v1/products/share  


## HTTP Status Codes & Errors

Neoflow uses conventional HTTP response codes to indicate the success or failure of an API request.

|HTTP Status Code|Summary|
|---|---|
|200| Everything works as expected.|
|201| Resource created successfully.|
|400| Bad request due to missing a required parameter.|
|401| Not authorized.|
|403| Do not have permission to access the resource.|
|404| Requested resource not found.|
|500| Something went wrong on Neoflow.|

## Support

If you would like to have support, please contact at it@mavennet.com.