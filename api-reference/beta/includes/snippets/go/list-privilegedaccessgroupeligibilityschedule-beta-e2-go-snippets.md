---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphidentitygovernance "github.com/microsoftgraph/msgraph-beta-sdk-go/identitygovernance"
	  //other-imports
)

graphClient, err := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestParameters := &graphidentitygovernance.IdentityGovernancePrivilegedAccessGroupEligibilitySchedulesRequestBuilderGetQueryParameters{
	Select: [] string {"accessId","principalId","groupId"},
}
configuration := &graphidentitygovernance.IdentityGovernancePrivilegedAccessGroupEligibilitySchedulesRequestBuilderGetRequestConfiguration{
	QueryParameters: requestParameters,
}

result, err := graphClient.IdentityGovernance().PrivilegedAccess().Group().EligibilitySchedules().Get(context.Background(), configuration)


```