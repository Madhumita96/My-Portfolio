# API Reference Document

## Resource: 
pet
## Description
This API adds a new pet to the pet store.
## Base URL 
petstore.swagger.io/v2
## Method 
POST
## Request URL 
https://petstore.swagger.io/v2/pet
## Example Request JSON
<ExampleRequestJSON>
    <![CDATA[
    {
      "id": 123,
      "category": {
        "id": 2,
        "name": "dog"
      },
      "name": "Pookie",
      "photoUrls": [
        "string"
      ],
      "tags": [
        {
          "id": 0,
          "name": "string"
        }
      ],
      "status": "available"
    }
    ]]>
</ExampleRequestJSON>


## Request Parameters

