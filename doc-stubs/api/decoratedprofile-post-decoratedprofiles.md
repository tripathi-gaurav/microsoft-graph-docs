---
title: "Create DecoratedProfile"
description: "Create a new DecoratedProfile object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
localization_priority: Normal
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Create DecoratedProfile
Namespace: microsoft.graph

Create a new [DecoratedProfile](../resources/decoratedprofile.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/concepts/permissions-reference.md).

|Permission type|Permissions (from most to least privileged)|
|:---|:---|
|Delegated (work or school account)|**TODO: Provide applicable permissions.**|
|Delegated (personal Microsoft account)|**TODO: Provide applicable permissions.**|
|Application|**TODO: Provide applicable permissions.**|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /decoratedProfiles
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [DecoratedProfile](../resources/decoratedprofile.md) object.

The following table shows the properties that are required when you create the [DecoratedProfile](../resources/decoratedprofile.md).

|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/entity.md)|
|profileUrl|String|**TODO: Add Description**|
|firstName|String|**TODO: Add Description**|
|lastName|String|**TODO: Add Description**|
|headline|String|**TODO: Add Description**|
|industryName|String|**TODO: Add Description**|
|summary|String|**TODO: Add Description**|
|location|String|**TODO: Add Description**|
|picture|String|**TODO: Add Description**|
|recentPositions|[Position](../resources/position.md) collection|**TODO: Add Description**|
|totalPositionCount|Int32|**TODO: Add Description**|
|recentEducations|[Education](../resources/education.md) collection|**TODO: Add Description**|
|totalEducationCount|Int32|**TODO: Add Description**|
|skills|String collection|**TODO: Add Description**|
|endorsedSkills|[SkillEndorsement](../resources/skillendorsement.md) collection|**TODO: Add Description**|
|totalEndorsedSkillCount|Int32|**TODO: Add Description**|
|emails|String collection|**TODO: Add Description**|
|phoneNumbers|[PhoneNumber](../resources/phonenumber.md) collection|**TODO: Add Description**|
|ims|[IM](../resources/im.md) collection|**TODO: Add Description**|
|websites|[liWebsite](../resources/liwebsite.md) collection|**TODO: Add Description**|
|bornOn|[Date](../resources/date.md)|**TODO: Add Description**|
|locale|[Locale](../resources/locale.md)|**TODO: Add Description**|
|connection|[Connection](../resources/connection.md)|**TODO: Add Description**|
|connected|Boolean|**TODO: Add Description**|
|connectionDegree|ConnectionDegree|**TODO: Add Description**. Possible values are: `OUT_OF_NETWORK`, `SELF`, `DISTANCE_1`, `DISTANCE_2`, `DISTANCE_3`.|
|invitationSentFromViewer|Boolean|**TODO: Add Description**|
|pendingInvitationSentFromViewee|[liInvitation](../resources/liinvitation.md)|**TODO: Add Description**|
|simpleProfileHighlights|[SimpleProfileHighlight](../resources/simpleprofilehighlight.md) collection|**TODO: Add Description**|
|profileHighlights|[DecoratedProfileProfileHighlights](../resources/decoratedprofileprofilehighlights.md) collection|**TODO: Add Description**|
|userGeneratedContents|[UserGeneratedContent](../resources/usergeneratedcontent.md) collection|**TODO: Add Description**|
|newsMentions|[NewsMention](../resources/newsmention.md) collection|**TODO: Add Description**|
|viewerCanConnectViewee|Boolean|**TODO: Add Description**|
|viewerCanFollowViewee|Boolean|**TODO: Add Description**|
|salesNavigatorInfo|[SalesNavigatorInfo](../resources/salesnavigatorinfo.md)|**TODO: Add Description**|



## Response

If successful, this method returns a `201 Created` response code and a [DecoratedProfile](../resources/decoratedprofile.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "create_decoratedprofile_from_decoratedprofiles"
}
-->
``` http
POST https://graph.microsoft.com/beta/decoratedProfiles
Content-Type: application/json
Content-length: 2001

{
  "@odata.type": "#microsoft.graph.DecoratedProfile",
  "profileUrl": "String",
  "firstName": "String",
  "lastName": "String",
  "headline": "String",
  "industryName": "String",
  "summary": "String",
  "location": "String",
  "picture": "String",
  "recentPositions": [
    {
      "@odata.type": "microsoft.graph.Position"
    }
  ],
  "totalPositionCount": "Integer",
  "recentEducations": [
    {
      "@odata.type": "microsoft.graph.Education"
    }
  ],
  "totalEducationCount": "Integer",
  "skills": [
    "String"
  ],
  "endorsedSkills": [
    {
      "@odata.type": "microsoft.graph.SkillEndorsement"
    }
  ],
  "totalEndorsedSkillCount": "Integer",
  "emails": [
    "String"
  ],
  "phoneNumbers": [
    {
      "@odata.type": "microsoft.graph.PhoneNumber"
    }
  ],
  "ims": [
    {
      "@odata.type": "microsoft.graph.IM"
    }
  ],
  "websites": [
    {
      "@odata.type": "microsoft.graph.liWebsite"
    }
  ],
  "bornOn": {
    "@odata.type": "microsoft.graph.Date"
  },
  "locale": {
    "@odata.type": "microsoft.graph.Locale"
  },
  "connection": {
    "@odata.type": "microsoft.graph.Connection"
  },
  "connected": "Boolean",
  "connectionDegree": "String",
  "invitationSentFromViewer": "Boolean",
  "pendingInvitationSentFromViewee": {
    "@odata.type": "microsoft.graph.liInvitation"
  },
  "simpleProfileHighlights": [
    {
      "@odata.type": "microsoft.graph.SimpleProfileHighlight"
    }
  ],
  "profileHighlights": [
    {
      "@odata.type": "microsoft.graph.DecoratedProfileProfileHighlights"
    }
  ],
  "userGeneratedContents": [
    {
      "@odata.type": "microsoft.graph.UserGeneratedContent"
    }
  ],
  "newsMentions": [
    {
      "@odata.type": "microsoft.graph.NewsMention"
    }
  ],
  "viewerCanConnectViewee": "Boolean",
  "viewerCanFollowViewee": "Boolean",
  "salesNavigatorInfo": {
    "@odata.type": "microsoft.graph.SalesNavigatorInfo"
  }
}
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.decoratedprofile"
}
-->
``` http
HTTP/1.1 201 Created
Content-Type: application/json
{
  "@odata.type": "#microsoft.graph.DecoratedProfile",
  "id": "b2ff5d52-5d52-b2ff-525d-ffb2525dffb2",
  "profileUrl": "String",
  "firstName": "String",
  "lastName": "String",
  "headline": "String",
  "industryName": "String",
  "summary": "String",
  "location": "String",
  "picture": "String",
  "recentPositions": [
    {
      "@odata.type": "microsoft.graph.Position"
    }
  ],
  "totalPositionCount": "Integer",
  "recentEducations": [
    {
      "@odata.type": "microsoft.graph.Education"
    }
  ],
  "totalEducationCount": "Integer",
  "skills": [
    "String"
  ],
  "endorsedSkills": [
    {
      "@odata.type": "microsoft.graph.SkillEndorsement"
    }
  ],
  "totalEndorsedSkillCount": "Integer",
  "emails": [
    "String"
  ],
  "phoneNumbers": [
    {
      "@odata.type": "microsoft.graph.PhoneNumber"
    }
  ],
  "ims": [
    {
      "@odata.type": "microsoft.graph.IM"
    }
  ],
  "websites": [
    {
      "@odata.type": "microsoft.graph.liWebsite"
    }
  ],
  "bornOn": {
    "@odata.type": "microsoft.graph.Date"
  },
  "locale": {
    "@odata.type": "microsoft.graph.Locale"
  },
  "connection": {
    "@odata.type": "microsoft.graph.Connection"
  },
  "connected": "Boolean",
  "connectionDegree": "String",
  "invitationSentFromViewer": "Boolean",
  "pendingInvitationSentFromViewee": {
    "@odata.type": "microsoft.graph.liInvitation"
  },
  "simpleProfileHighlights": [
    {
      "@odata.type": "microsoft.graph.SimpleProfileHighlight"
    }
  ],
  "profileHighlights": [
    {
      "@odata.type": "microsoft.graph.DecoratedProfileProfileHighlights"
    }
  ],
  "userGeneratedContents": [
    {
      "@odata.type": "microsoft.graph.UserGeneratedContent"
    }
  ],
  "newsMentions": [
    {
      "@odata.type": "microsoft.graph.NewsMention"
    }
  ],
  "viewerCanConnectViewee": "Boolean",
  "viewerCanFollowViewee": "Boolean",
  "salesNavigatorInfo": {
    "@odata.type": "microsoft.graph.SalesNavigatorInfo"
  }
}
```
