{
  "info": {
    "name": "AutoDesk Forge Authenticate",
    "_postman_id": "a2d848af-f5f9-4509-a456-2478e68bf0d5",
    "description": "Authenticate.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "AutoCad",
      "item": [
        {
          "id": "9bcb14b3-b559-4763-9749-28c44228ff7c",
          "name": "AuthenticationV1AuthenticatePost",
          "request": {
            "url": "http://developer.api.autodesk.com/authentication/v1/authenticate",
            "method": "POST",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "client_id",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                },
                {
                  "key": "client_secret",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                },
                {
                  "key": "grant_type",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                },
                {
                  "key": "scope",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                }
              ]
            },
            "description": "Authenticate."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7b82961b-1606-43f0-863b-cab9e28a0c42"
            }
          ]
        }
      ]
    }
  ]
}