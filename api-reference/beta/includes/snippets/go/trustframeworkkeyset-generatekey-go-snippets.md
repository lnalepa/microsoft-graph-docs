---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)

requestBody := graphmodels.NewGenerateKeyPostRequestBody()
use := "sig"
requestBody.SetUse(&use) 
kty := "RSA"
requestBody.SetKty(&kty) 
nbf := int64(1508969811)
requestBody.SetNbf(&nbf) 
exp := int64(1508969811)
requestBody.SetExp(&exp) 

result, err := graphClient.TrustFramework().KeySetsById("trustFrameworkKeySet-id").GenerateKey().Post(context.Background(), requestBody, nil)


```