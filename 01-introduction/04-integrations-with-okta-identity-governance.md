## Integrations with Okta Identity Governance


The primary integration is the provisioning integrations leveraged by
LCM. These include:

- **Okta Integration Network (OIN)** integrations that support
  [<u>directory and HR
  Sync</u>](https://www.okta.com/au/integrations/?category=directory-and-hr-sync)
  or
  [<u>provisioning</u>](https://www.okta.com/au/integrations/?category=lifecycle-management),
  via SCIM or APIs. These are ready to connect and understand the
  identity repository of the connected system.

  - A growing number of these also support [<u>entitlement
    management</u>](https://www.okta.com/au/integrations/?category=lifecycle-management&capability=entitlement-management).

- **Generic SCIM connectors** where you build the implementation to feed
  off SCIM API calls from Okta.

- **On-Premise Provisioning** integrations, where a SCIM service is used
  with bespoke code to [<u>provision to on-premise
  systems</u>](https://help.okta.com/oie/en-us/content/topics/provisioning/opp/opp-main.htm).

  - There are On-Prem Connectors for [<u>Oracle
    EBS</u>](https://help.okta.com/oie/en-us/content/topics/provisioning/opc/connectors/oracle-ebs.htm),
    [<u>SAP Netweaver
    ABAP</u>](https://help.okta.com/oie/en-us/content/topics/provisioning/opc/connectors/sap-netweaver-abap.htm)
    and a soon-to-be released database connector.

- **Custom connectors** leveraging OIG APIs, Workflows or other
  mechanisms.

As mentioned in the architecture section above, the access requests
component can use chatbots in Slack or Microsoft Teams. Many components
in OIG and Okta leverage email.

---

<sub>[← Users, Groups and Entitlements](03-users-groups-and-entitlements.md) | [Other Uses of Okta Identity Governance →](05-other-uses-of-okta-identity-governance.md)</sub>
