## Lab 2.3 - Request Conditions with SoD Checking


Earlier in the [<u>Entitlement
Management</u>](#exploring-entitlement-management) section we created a
[<u>Separation of Duties</u>](#separation-of-duties) rule. We will use
this as part of the access request conditions we created earlier to
validate SoD checking when requesting access. The rule we set up
involved conflicts between privileged access to the Computer Hall and
the Doc Archives. If you did not do that lab, you can either skip this
lab or go back and do that lab then come back here.

We’ll first look at the default (block) behaviour then modify it to the
allow behaviour and show the warnings carried through the request.

### SoD Default Behaviour

#### Contractor Requests Access

We first want to look at the default SoD checking behaviour.

1.  As your contractor user, log into the **Okta Dashboard** and click
    the **Request access** button.

2.  Select the app that has the entitlements and SoD rule (Building
    Access in our case).

3.  Click the access level you didn’t select in the previous lab. You
    should see a Conflict Details message appear to the right.

> <img
> src="../media/image11.png"
> style="width:6.47292in;height:2.95712in" />
>
> The access is blocked and you cannot submit the request.

4.  Click on the **Show conflict details** button to see the reason for
    the block. It shows the title and description of the SoD rule.

Blocking SoD conflicts is the default behaviour and may be appropriate
to your environment. However we want to allow, with oversight, SoD
conflicts. We will change the behaviour to allow conflicts.

#### Check SoD Configuration for App

To update the SoD rule behaviour:

5.  Log into the **Okta Admin Console** and go to **Applications \>
    Applications.**

6.  Select the application you setup SoD rules (our Building Access
    app).

7.  Go to the **<u>Access requests</u>** tab.

8.  Click on the **Settings** button.

9.  On the **\<app\> access request** settings page, click **Edit** in
    the **When SOD conflicts occur** section.

> There are three options: **Allow requests**, **Allow requests with
> custom settings** and **Block requests** (the default).

10. Click on the **Allow requests with custom settings** option.

> <img
> src="../media/image237.png"
> style="width:6.48125in;height:4.21474in" />
>
> This option allows the SoD violation, but can either run a separate
> approval sequence (perhaps you want to have an additional level of
> approval) or set a specific access duration (perhaps a much shorter
> window of access given the potential increased risk). You can select
> both.

11. Click on the **Allow requests** setting (the custom settings
    disappears) and click the **Save** button.

> <img
> src="../media/image291.png"
> style="width:6.47292in;height:2.81264in" />

There is also a setting to allow requests on behalf of someone else.
When enabled it can be set to only allow managers to request on behalf
of their reports, or anyone in the organization. If you were going to
enable this, particularly to allow anyone to request access for anyone
else, you would need to ensure you have appropriate checks (approvals)
in the request condition sequence. We will not cover this in the labs.

### Behaviour with SoD Set to Allow

#### Contractor Request Access Again

Try requesting access again:

12. As the contractor sign out and sign into the Okta Dashboard again.

13. Select the Request access button.

14. Select the app

15. Select the other access again

> <img
> src="../media/image72.png"
> style="width:6.48125in;height:4.35941in" />
>
> The **Conflict Details** are now a warning and the **Business
> Justification** question is shown.

16. Enter a **Business Justification** and click the **Submit request**
    button.

Approval Processing

17. As the contractors manager, log into the **Okta Dashboard** and go
    to the **Okta Access Requests** app.

18. Select the new request.

> <img
> src="../media/image283.png"
> style="width:6.48958in;height:3.27376in" />
>
> The request flags that there is a Separation of duties conflict at the
> top so that the approver can see there is risk associated with the
> request. He can click on the See SOD conflict details to see the SoD
> rule title and description.

19. Provide details of the **Contractor Role** and click the **Submit**
    button as you did in the previous lab.

20. Click the **Approve** button to approve the request. It then goes to
    the second level approver (recall that both request conditions used
    the same sequence).

21. As the second approver, log into the Okta Dashboard, go to the Okta
    Access Request app and select the new request.

> Note that this approver also sees the Separation of duties conflict
> message.

22. Click the **Approve** button.

> <img
> src="../media/image236.png"
> style="width:6.48125in;height:2.39189in" />

#### Confirm Additional Access Added

23. Log into the **Okta Admin Console** as the administrator.

24. Go to **Applications \> Applications** and select the app.

25. On the **<u>Assignments</u>** tab, find the contractor, select the
    **more actions** icon and the **View access details** option.

> <img
> src="../media/image154.png"
> style="width:5.0625in;height:4.89654in" />
>
> You should see the new entitlement bundle has been added (in our case
> both Building Access = Head Office and Privileged Access = Doc
> Archive). The General expiration date has been bumped up to the date
> of the latest access request (so that even when the first request
> expires, the app access will remain).

This concludes the SoD lab. In this lab we have shown how to set the SoD
rule processing behaviour (block or allow) and what this means to the
user experience for both the requester and the approvers.

This is the last lab looking at conditions. The next lab will look at
Request Types.

---

[← Lab 2.2 - Request Conditions with Application Entitlements](04-lab-22---request-conditions-with-application-entitlements.md) | [Lab 2.4 - Request Types for Complex Requirements →](06-lab-24---request-types-for-complex-requirements.md)
