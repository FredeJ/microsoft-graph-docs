---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

// THE PYTHON SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
client =  GraphServiceClient(request_adapter)

request_body = SendActivityNotificationToRecipientsPostRequestBody()
topic = TeamworkActivityTopic()
topic.source(TeamworkActivityTopicSource.EntityUrl('teamworkactivitytopicsource.entityurl'))

topic.value = 'https://graph.microsoft.com/beta/appCatalogs/teamsApps/{teamsAppId}'


request_body.topic = topic
request_body.activity_type = 'pendingFinanceApprovalRequests'

preview_text = ItemBody()
preview_text.content = 'Internal spending team has a pending finance approval requests'


request_body.preview_text = preview_text
recipients_teamwork_notification_recipient1 = TeamworkNotificationRecipient()
recipients_teamwork_notification_recipient1.@odata_type = 'microsoft.graph.aadUserNotificationRecipient'

additional_data = [
'user_id' => '569363e2-4e49-4661-87f2-16f245c5d66a', 
];
recipients_teamwork_notification_recipient1.additional_data(additional_data)



recipientsArray []= recipientsTeamworkNotificationRecipient1;
recipients_teamwork_notification_recipient2 = TeamworkNotificationRecipient()
recipients_teamwork_notification_recipient2.@odata_type = 'microsoft.graph.aadUserNotificationRecipient'

additional_data = [
'user_id' => 'ab88234e-0874-477c-9638-d144296ed04f', 
];
recipients_teamwork_notification_recipient2.additional_data(additional_data)



recipientsArray []= recipientsTeamworkNotificationRecipient2;
recipients_teamwork_notification_recipient3 = TeamworkNotificationRecipient()
recipients_teamwork_notification_recipient3.@odata_type = 'microsoft.graph.aadUserNotificationRecipient'

additional_data = [
'user_id' => '01c64f53-69aa-42c7-9b7f-9f75195d6bfc', 
];
recipients_teamwork_notification_recipient3.additional_data(additional_data)



recipientsArray []= recipientsTeamworkNotificationRecipient3;
request_body.recipients(recipientsArray)


template_parameters_key_value_pair1 = KeyValuePair()
template_parameters_key_value_pair1.name = 'pendingRequestCount'

template_parameters_key_value_pair1.value = '5'


templateParametersArray []= templateParametersKeyValuePair1;
request_body.templateparameters(templateParametersArray)





await client.teamwork.send_activity_notification_to_recipients.post(request_body = request_body)


```