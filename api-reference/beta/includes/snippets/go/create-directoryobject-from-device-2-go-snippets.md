---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphmodels "github.com/microsoftgraph/msgraph-beta-sdk-go/Devices/Item/RegisteredUsers/Item"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphmodels.NewRegisteredUser()
additionalData := map[string]interface{}{
	"odataId" : "https://graph.microsoft.com/beta/directoryObjects/{id}", 
}
requestBody.SetAdditionalData(additionalData)

graphClient.DevicesById("device-id").RegisteredUsersById("directoryObject-id").Post(context.Background(), requestBody, nil)


```