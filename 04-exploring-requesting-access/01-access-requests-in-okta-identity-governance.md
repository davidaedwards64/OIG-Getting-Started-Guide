## Access Requests in Okta Identity Governance


A core component of any Identity Governance and Administration (IGA)
solution is a means to request access. Most IGA deployments will need to
look at balancing birthright access and access that is granted as
required. The former includes assigning access based on roles. The
latter is implemented through access requests. Some organisations may
have most of their access granted as birthright with a minor set of
request-based access. Others may have few (and very generic) birthright
assignments, and rely heavily on request-based access.

Within Okta and OIG, birthright access can be implemented via **group
rules** (for assignment via groups) or **entitlement policy** (for
application entitlements, as covered earlier in this guide). This
section will look at the OIG Access Request mechanisms.

### The Access Request Platform and Access Requests

If you refer back to the [<u>Architectural Overview of Okta Identity
Governance</u>](#architectural-overview-of-okta-identity-governance)
section, you will notice there is an Access Request Platform listed.
This is the engine for running the access requests and serves as the
administrative interface for some types of requests. It is a tenant in
its own right, but tightly integrated with the Okts Org, and has its own
user interfaces that will be explored in detail in the last lab in this
section.

### Conditions vs Request Types

In OIG there are two primary ways to manage how users request access to
resources: Access Request **Conditions** (part of Resource-Centric
Access Requests) and **Request Types**. Whilst you may see different
terminology, the [<u>Access Requests documentation
page</u>](https://help.okta.com/oie/en-us/content/topics/identity-governance/access-requests/ar-overview.htm)
uses the terms “Conditions” and “Request Types” and this document will
follow that terminology.

***Conditions***

> *Conditions are rules that define who can request access, the level of
> access that they can request, the duration of access, and the approval
> sequence for each app directly from the app's profile page in your
> Admin Console. An approval sequence is a linear series of steps like
> questions, Okta Workflows, approvals, and tasks. These steps govern
> the information that specific users must provide, the users
> responsible for approving or denying the request, and any actions that
> must be completed.*
>
> *When you use conditions to manage access to a resource, requesters
> can directly go to the End-User Dashboard, select the resource's tile,
> and then enter the required information to request access.*
>
> *If you're new to Access Requests, use conditions to manage access
> requests first.*

***Request types***

> *Request types are structured flows that define the lifecycle of a
> request. These flows are made of steps like questions, tasks, and
> timers. You can associate a request type with a resource (apps,
> groups, entitlement bundles) using a configuration list. Each Access
> Requests team owns and manages multiple request types and associated
> requests. You can also set up some automated actions in Okta and in
> integrated external systems like Jira and ServiceNow.*
>
> *With request types, the requesters go to the Okta Access Requests web
> app from their End-User Dashboard, select a request type, and then
> enter the required information to request access. Requesters can also
> request access from Slack or Microsoft Teams (if integrated with
> Access Requests).*
>
> *You can't create request types to manage access requests for Okta
> admin role bundles. Also, groups that grant Okta admin roles can't be
> assigned using access requests that are managed by request types. If
> users request such groups, they get an error on the request details
> page of their request.*

While Request Types were the original method, Okta is shifting toward
Conditions for most standard use cases because they are more scalable
and integrated directly into the Admin Console. Ideally you should use
Conditions wherever possible and Request types when there is no other
alternative.

The following table provides a comparison between Conditions and Request
Types.

| **Feature**                                                 |
|-------------------------------------------------------------|
| **Primary Philosophy**                                      |
| **Terminology**                                             |
| **Management Console**                                      |
| **User Experience**                                         |
| **Approval Logic**                                          |
| **Admin Role Support**                                      |
| **Complex Logic**                                           |
| **Integrations**                                            |
| **Scalability**                                             |
| **Access Duration**                                         |
| [**<u>APIs</u>**](https://developer.okta.com/docs/api/iga/) |

Key differences to consider between Conditions and Request Types:

**1. Where they "Live"**

> Conditions are rules you attach directly to an application or group.
> For example, if you go to the "Salesforce" app in Okta, you can create
> a condition there that says "Members of the Sales group can request
> this."
>
> Request Types are global flows. You create a "Laptop Request" or
> "Database Access" flow in the Access Requests console and then define
> what happens once it's triggered.

**2. The Requester Journey**

> With Conditions, the user experience is "Unified." When a user sees an
> app they don't have access to on their dashboard, they can click
> "Request Access" right there.
>
> With Request Types, users typically browse a catalog of "Forms"
> (Request Types) in the Access Requests portal or via a chat bot in
> Slack or Microsoft Teams.

**3. Complexity vs. Ease of Use**

> Use Conditions if: You need a quick, scalable way to govern standard
> app access, AD groups, or Okta Admin roles. This is Okta's recommended
> "starting point" for most organizations.
>
> Use Request Types if: You need complex business logic, such as "If the
> user is in Department A, ask Question X; if in Department B, assign a
> task to the IT Hardware team," or if you need to trigger external
> tickets in Jira/ServiceNow.

The remainder of this section will look at both, but with a focus on
Conditions.

---

<sub>[Introduction to the Labs →](02-introduction-to-the-labs.md)</sub>
