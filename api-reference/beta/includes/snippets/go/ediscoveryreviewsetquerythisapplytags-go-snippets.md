---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphsecurity "github.com/microsoftgraph/msgraph-beta-sdk-go/security"
	  graphmodelssecurity "github.com/microsoftgraph/msgraph-beta-sdk-go/models/security"
	  //other-imports
)

graphClient, err := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestBody := graphsecurity.NewApplyTagsPostRequestBody()


ediscoveryReviewTag := graphmodelssecurity.NewEdiscoveryReviewTag()
id := "d3d99dc704a74801b792b3e1e722aa0d"
ediscoveryReviewTag.SetId(&id) 

tagsToAdd := []graphsecurity.Objectable {
	ediscoveryReviewTag,

}
requestBody.SetTagsToAdd(tagsToAdd)

graphClient.Security().Cases().EdiscoveryCases().ByEdiscoveryCaseId("ediscoveryCase-id").ReviewSets().ByReviewSetId("ediscoveryReviewSet-id").Queries().ByQuerieId("ediscoveryReviewSetQuery-id").MicrosoftGraphSecurityApplyTags().Post(context.Background(), requestBody, nil)


```