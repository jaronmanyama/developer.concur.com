
## Getting Started - Request v4

### Menu

* [Getting Started](#get-started)
* [Request](#request-v4-request-resources)
* [Workflow](#request-v4-workflow-resources)
* [Expected Expense](#request-v4-expected-expense-resources)
* [Request Cash Advance](#request-v4-request-cash-advance-resources)
* [Request Policy](#request-v4-request-policy-resources)
* [Travel Agency](#request-v4-travel-agency-resources)
* [Schema](#request-v4-endpoints-schema)
* [HTTP Status Codes](#request-v4-http-status-codes)
* [Run in Postman](https://app.getpostman.com/run-collection/8273d843078f0bcf0823)

Concur Request automates the spend request and approval process for both travel and everyday expenses, giving you the data you need to accurately track and better control spending. By increasing visibility into planned expenses and up-to-date budget data, you can make strategic spending decisions before any spending actually occurs. The Request API provides many possibilities, particularly Requests creation and transition into the approval workflow.

Version 4.0 of Request API works only with the new [Authentication API](/api-reference/authentication/apidoc.html).

### Getting Started

* [Overview](#getting-started-overview)
* [Prior Versions](#getting-started-prior-versions)
* [Process Flow](#getting-started-process-flow)
* [Products and Editions](#getting-started-products-and-editions)
* [Scope Usage](#getting-started-scope-usage)
* [Dependencies](#getting-started-dependencies)
* [Access Token Usage](#getting-started-access-token-usage)

#### <a name="overview"></a>Getting Started - Overview

The Request v4 API exposes five different resources:

Resource|Description
---|---
Request|You can read, create, update or delete a Request and get the list of existing Requests.
Workflow|You can perform action in the approval workflow of a Request (submit, approve, cancel...)
Expected Expense|You can read, create, update or delete an expected expense, and get the list of expected Expenses for a specific Request.
Request Policy|You can get the list of existing Request policies.
Travel Agency|You can get the description of a Travel Agency office.

These resources are used to manage documents used for pre-spend authorizations within Concur Request.

#### <a name="prior-versions"></a>Getting Started - Prior Versions

* Request v1 documentation is available [here](./v1.request.html).
* Request v3 documentation is available [here](./v3.request.html).

#### <a name="process-flow"></a>Getting Started - Process Flow
![Process Flow for Request V4](./v4.request-process-flow.png)

#### <a name="products-editions"></a>Getting Started - Products and Editions

* Concur Request Professional Edition
* Concur Request Standard Edition

#### <a name="scope-usage"></a>Getting Started - Scope Usage

Name|Description|Endpoint
---|---|---
`travelrequest.write`|Read and write Requests|GET, POST, PUT, DELETE

#### <a name="dependencies"></a>Getting Started - Dependencies

SAP Concur clients must purchase Concur Request in order to use this API. This API may require for some use cases to consume the following additional SAP Concur APIs:

* [User profile](/api-reference/profile/v1.user.html), to retrieve the `userId` - required in most of the endpoints when accessed via a Company Token.
* [List], to retrieve the `listItemId` - required in the management of custom fields related to list items. Currently in externalisation process, please liaise with List API owner team for further update.

#### <a name="access-token-usage"></a>Getting Started - Access Token Usage

This API supports both company level and user level access tokens.

#### Company Access Token

* The `userId` parameter is required to provide the user identity of who made the API call.
* Does not have an associated role.

#### User Access Token

* The `userId` parameter is not required.
* Requires the Web Service Admin role to call the API.

