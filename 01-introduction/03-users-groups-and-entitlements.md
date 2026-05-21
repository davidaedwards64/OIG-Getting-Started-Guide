## Users, Groups and Entitlements


OIG is primarily concerned with users, groups and entitlements.

**Users** in Okta represent people and are stored in User Profiles with
user attributes. Okta does not talk about accounts like other IGA
solutions. However where there is a user/account object on a connected
system, Okta will store the account/user representation in an
application user profile which would normally be synchronised with the
connected system.

Okta collects users into **Groups**. These may be Okta groups (defined
in Okta) or application groups (imported from connected systems like
Microsoft Active Directory, Entra ID and Google Workspace). Groups can
be pushed to connected systems (for example Okta Privileged Access uses
groups pushed from Okta for admin roles and policy) to drive
entitlement. Whilst most application groups are mastered in their
application, and thus are read-only in Okta, Active Directory groups can
have their memberships managed in Okta and pushed to AD.

Okta does NOT have the concept of a role like other IGA products (except
for the Admin Roles to manage the Okta platform). Many customers use
groups to implement business roles, but there is no hierarchy normally
associated with role implementations.

Whilst users and groups are there with all Okta Workforce
implementations, OIG also supports **Entitlements**. These are
application-specific objects used to control access. Common examples are
Roles, Licenses, Permission Sets and Profiles. Some [<u>supported
apps</u>](https://help.okta.com/oie/en-us/content/topics/identity-governance/em/app-connectors-with-entitlements.htm)
have a single entitlement type and others have multiple.
[<u>Salesforce.com</u>](http://salesforce.com) supports five different
types of entitlements. These are imported into OIG and assignment to
them is managed in OIG (Access Requests, Access Certification).
Entitlements can also be used in [<u>Separation of
duties</u>](https://help.okta.com/oie/en-us/content/topics/identity-governance/sd/separation-of-duties.htm)
controls.

---

<sub>[← Architectural Overview of Okta Identity Governance](02-architectural-overview-of-okta-identity-governance.md) | [Integrations with Okta Identity Governance →](04-integrations-with-okta-identity-governance.md)</sub>
