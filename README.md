# ua-workday
Workday adapter for ConnectALL using Universal Adapter
ConnectALL Workday Universal Adapter (ua-Workday)
The ConnectALL Workday Universal Adapter is developed as an extension to the universal adapter capability of ConnectALL. This adapter allows users to integrate Workday with ConnectALL for streamlined worker data.
This document outlines the current capabilities, configuration steps, and limitations of the Workday Universal Adapter.


**Setup**
Supported Entities
This Universal Adapter currently supports the following Workday entities (subject to Workday API access rights):
Worker object


**Connection Details**

Connection Name: Workday

Application Type: workday

URL: Base URL for Workday tenant (e.g., https://wd5.myworkday.com)

User Name: Workday API integration user

Password: Workday API integration user password

Auth Operation: Header

Application Category: Select from dropdown (e.g., worker)

Time Zone: GMT+0

Authentication Type: Basic

**Flow Filters**

Flow filters can be applied using Workday-specific query parameters as defined in the Workday Web Services or REST API documentation.

Examples:

To filter workers by organization: organization_id=12345

To filter job requisitions by status: status=Open

**Notes:**

Refer to Workday’s API documentation for supported query parameters per endpoint.

Filters must conform to Workday’s supported request schema and security permissions.

**Known Limitations**

Entity support is limited to what is exposed through the Workday APIs and permissions of the integration user.

Some Workday tenants may use custom reports or RaaS (Report-as-a-Service) endpoints. These are not universally supported via UA and may require custom implementation.

Pagination and large data set handling may require configuration of flow throttling.

Certain entities (e.g., Benefits, Payroll) may be unavailable depending on the Workday subscription module and permissions.

