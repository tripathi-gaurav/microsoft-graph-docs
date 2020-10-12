### Devices and apps

| **Change type** | **Version** | **Description** |
|:---|:---|:---|
|Addition|beta|Added the **displayName** property to [printerBase](https://docs.microsoft.com/en-us/graph/api/resources/printerBase?view=graph-rest-beta) resource|
|Addition|beta|Added the **shares** relationship to [printer](https://docs.microsoft.com/en-us/graph/api/resources/printer?view=graph-rest-beta) resource|
|Addition|beta|Added the **state** property to [printerStatus](https://docs.microsoft.com/en-us/graph/api/resources/printerStatus?view=graph-rest-beta) resource|
|Addition|beta|Added the **details** property to [printerStatus](https://docs.microsoft.com/en-us/graph/api/resources/printerStatus?view=graph-rest-beta) resource|
|Addition|beta|Added the **description** property to [printerStatus](https://docs.microsoft.com/en-us/graph/api/resources/printerStatus?view=graph-rest-beta) resource|
|Addition|beta|Added the **feedOrientations** property to [printerCapabilities](https://docs.microsoft.com/en-us/graph/api/resources/printerCapabilities?view=graph-rest-beta) resource|
|Addition|beta|Added the **displayName** property to [printConnector](https://docs.microsoft.com/en-us/graph/api/resources/printConnector?view=graph-rest-beta) resource|
|Addition|beta|Added the **feedOrientation** property to [printerDocumentConfiguration](https://docs.microsoft.com/en-us/graph/api/resources/printerDocumentConfiguration?view=graph-rest-beta) resource|
|Addition|beta|Added the **configuration** property to [printJob](https://docs.microsoft.com/en-us/graph/api/resources/printJob?view=graph-rest-beta) resource|
|Addition|beta|Added the **redirectedTo** property to [printJob](https://docs.microsoft.com/en-us/graph/api/resources/printJob?view=graph-rest-beta) resource|
|Addition|beta|Added the **redirectedFrom** property to [printJob](https://docs.microsoft.com/en-us/graph/api/resources/printJob?view=graph-rest-beta) resource|
|Addition|beta|Added the **isFetchable** property to [printJob](https://docs.microsoft.com/en-us/graph/api/resources/printJob?view=graph-rest-beta) resource|
|Addition|beta|Added the **state** property to [printJobStatus](https://docs.microsoft.com/en-us/graph/api/resources/printJobStatus?view=graph-rest-beta) resource|
|Addition|beta|Added the **description** property to [printJobStatus](https://docs.microsoft.com/en-us/graph/api/resources/printJobStatus?view=graph-rest-beta) resource|
|Addition|beta|Added the **isAcquiredByPrinter** property to [printJobStatus](https://docs.microsoft.com/en-us/graph/api/resources/printJobStatus?view=graph-rest-beta) resource|
|Addition|beta|Added the **details** property to [printJobStatus](https://docs.microsoft.com/en-us/graph/api/resources/printJobStatus?view=graph-rest-beta) resource|
|Addition|beta|Added the [printJobConfiguration](https://docs.microsoft.com/en-us/graph/api/resources/printJobConfiguration?view=graph-rest-beta) resource type|
|Addition|beta|Added the [printDocumentUploadProperties](https://docs.microsoft.com/en-us/graph/api/resources/printDocumentUploadProperties?view=graph-rest-beta) resource type|
|Addition|beta|Added the [uploadSession](https://docs.microsoft.com/en-us/graph/api/resources/uploadSession?view=graph-rest-beta) resource type|
|Addition|beta|Added the **printerProcessingStateDetail** enumeration type|
|Addition|beta|Added the **printJobStateDetail** enumeration type|
|Addition|beta|Added the **printerFeedOrientation** enumeration type|
|Addition|beta|Added the [restoreFactoryDefaults](https://docs.microsoft.com/en-us/graph/api/printer-restoreFactoryDefaults?view=graph-rest-beta) method to the [printer](https://docs.microsoft.com/en-us/graph/api/resources/printer?view=graph-rest-beta) resource|
|Addition|beta|Added the [createUploadSession](https://docs.microsoft.com/en-us/graph/api/printDocument-createUploadSession?view=graph-rest-beta) method to the [printDocument](https://docs.microsoft.com/en-us/graph/api/resources/printDocument?view=graph-rest-beta) resource|
|Addition|beta|Added the [cancel](https://docs.microsoft.com/en-us/graph/api/printJob-cancel?view=graph-rest-beta) method to the [printJob](https://docs.microsoft.com/en-us/graph/api/resources/printJob?view=graph-rest-beta) resource|
|Addition|beta|Added the [start](https://docs.microsoft.com/en-us/graph/api/printJob-start?view=graph-rest-beta) method to the [printJob](https://docs.microsoft.com/en-us/graph/api/resources/printJob?view=graph-rest-beta) resource|
|Change|beta|Changed the **displayName** property in the [printDocument](https://docs.microsoft.com/en-us/graph/api/resources/printDocument?view=graph-rest-beta) resource from required to optional|
|Change|beta|Changed the **contentType** property in the [printDocument](https://docs.microsoft.com/en-us/graph/api/resources/printDocument?view=graph-rest-beta) resource from required to optional|
|Deletion|beta|Removed the `pendingHeld` member from the **printJobProcessingState** enumeration|
|Deletion|beta|Removed the `processing` member from the **printJobProcessingState** enumeration|
|Deletion|beta|Removed the `paused` member from the **printJobProcessingState** enumeration|
|Deletion|beta|Removed the `stopped` member from the **printJobProcessingState** enumeration|
|Deletion|beta|Removed the `completed` member from the **printJobProcessingState** enumeration|
|Deletion|beta|Removed the `canceled` member from the **printJobProcessingState** enumeration|
|Deletion|beta|Removed the `aborted` member from the **printJobProcessingState** enumeration|
