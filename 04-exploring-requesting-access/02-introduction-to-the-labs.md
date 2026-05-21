## Introduction to the Labs


This section provides an overview of the labs and the prerequisites to
run them.

### The Labs in this Section

As with the previous section looking at Entitlements, this section
presents some prereqs and three “follow the bouncing ball” lab sections.
The lab sections are:

- **Lab 2.1 - Request Conditions with Applications and Groups**. This is
  a simple use case where an application has some push-groups assigned
  and we want to expose them via request conditions to be requestable
  (i.e. a user will get the application access and be added to a group).

- **Lab 2.2 - Request Conditions with Application Entitlements**. This
  utilises application entitlements covered in the previous section,
  making them requestable.

- **Lab 2.3 - Request Conditions with SoD Checking**. Using the
  separation of duties rules built earlier, create and test a SoD
  violation in an access request.

- **Lab 2.4 - Request Types for Complex Requirements**. This use case
  uses the older request type mechanism for more complex access request
  flows.

You do not need to do all of them, but it is suggested you do them in
the order presented as latter labs are less verbose (with less screen
shots) where content is a repeat of earlier labs. See the prerequisites
section below for the apps needed for each app.

We will not cover the Slack or Microsoft Teams integration in this
guide.

### Prerequisites

The prerequisites for this section were covered in the earlier
[<u>Preparing Your Okta
Environment</u>](#preparing-your-okta-environment) section:

- OIG enabled in your Okta org

- Administrator access to create/manage access requests

- User(s) with a manager who will request access

- Manager(s) who can review and approve access requests

- A dummy application for the first lab,

- An entitlement-enabled application for the second lab,

- An entitlement-enabled application with SoD rules for the third lab
  and

- ???? for the fourth lab

We will use a Carpark Access dummy app, the Building Access SCIM
application, and the Salesforce.com apps in the examples.

The last lab will use the Access Requests Platform for Request Types. It
will require some configuration that will be covered in the lab
instructions.

### Access Request Apps and SSO Configuration

Prior to starting the labs, you need to read and follow the steps in
[<u>Configure policies for Access requests
apps</u>](https://help.okta.com/oie/en-us/content/topics/identity-governance/access-requests/ar-governance-apps.htm).
This describes the Okta apps related to Access Requests.

There is currently a change that was applied to Okta Preview
environments in July 2025 that removes the **Okta Access Request Admin**
app but at the time of writing is still in Okta Production orgs. If you
have this app, you need to configure the policies for that app as per
the docs.

You should follow the steps for the **Okta Identity Governance** app in
the docs.

---

<sub>[← Access Requests in Okta Identity Governance](01-access-requests-in-okta-identity-governance.md) | [Lab 2.1 - Request Conditions with Applications and Groups →](03-lab-21---request-conditions-with-applications-and-groups.md)</sub>
