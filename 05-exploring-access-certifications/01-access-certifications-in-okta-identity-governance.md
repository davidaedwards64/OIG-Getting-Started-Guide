## Access Certifications in Okta Identity Governance


Access certification is a key control in Identity Governance and
Administration (IGA). It is used to validate that users have only the
access they need to do their job, and to provide an audit trail that
there is regular review of the access. You may also hear the terms
recertification, attestation or user access review (UAR). Access
certification is normally a key control in compliance regulations,
sometimes focused on administrative, privileged, or high-risk access.

Without an automated solution like what Okta Identity Governance
provides, many organisations rely on resource-intensive manual processes
involving spreadsheets and emails. Access certification may impact all
parts of a business and needs to be easy to use so it doesn’t get in the
way of doing business.

The lifecycle of an access certification campaign is:

- The campaign is **defined**, covering the users and systems/accesses
  to be reviewed and how the campaign is to run. This may be a one-off
  campaign or a recurring campaign.

- The campaign is **launched**. The system takes a snapshot of the users
  and systems/accesses, determines the reviewers, and sends out emails
  to those reviewers.

- The campaign **runs** from its start date to its end date. Reviewers
  review the review items assigned to them and approve/revoke the access
  or reassign the review to someone else.

- The campaign **ends**, and any unreviewed accesses are processed
  according to configuration in the campaign.

Prior to building and running certification campaigns, you need to
consider how access is granted in your Okta. Users can be assigned
directly to applications, or groups will be assigned to applications and
users are added to, and removed from, the groups as needed. Also, how
are users assigned to groups? Are they Okta managed groups or
application-managed (like AD)? Are they manually assigned or are there
group rules automatically assigning group membership?

Understanding this for your environment will be crucial to effective
Access Certification campaigns – revoking access in a campaign may have
unexpected results if Okta is not set up to allow removing the group
membership.

See also [<u>Exploring Enhanced Group Remediation in Access
Certification</u>](https://support.okta.com/help/s/article/exploring-enhanced-group-remediation-in-access-certification?language=en_US).

---

<sub>[Introduction to the Labs →](02-introduction-to-the-labs.md)</sub>
