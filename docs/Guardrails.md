Cloud Guardrails
================

This document focuses on a **preliminary set of baseline security
controls** to ensure that the cloud service environment has a minimum
set of configurations for the cloud environment. Departments are
expected to must implement, validate, and report on in the first 30
business days.

Departments are responsible for implementing the minimum configurations
identified in the table below. Validation of the guardrails will be
performed by SSC Cloud Services Directorate. The [Standard Operating
Procedure (SOP) on Validating Cloud
Guardrails](https://www.gcpedia.gc.ca/gcwiki/images/1/19/SOP_for_Validating_Cloud_Guardrails.pdf)
has been developed to support this activity.

For this document the following definitions will be used:

-   Mandatory requirements: A set of baseline security controls that
    > departments must implement, validate, and report on in the first
    > 30 business days.

```{=html}
<!-- -->
```
-   Additional considerations: Additional security controls that are
    > highly recommended and should be taken into consideration. While
    > these are not expected to be implemented within 30 business days,
    > they include best practices that should be considered as
    > departments progress with the establishment of their cloud-based
    > environments.

Guardrail \#1 -- Protect user accounts and identities 
-----------------------------------------------------

+----------------------------------+----------------------------------+
| **Objective:** Protect user      |                                  |
| accounts and identities.         |                                  |
+==================================+==================================+
| ***Applicable Service Models:    |                                  |
| IaaS, PaaS, SaaS***              |                                  |
+----------------------------------+----------------------------------+
| **Mandatory Requirements**       | **Validation**                   |
+----------------------------------+----------------------------------+
| -   Implement strong             | -   Confirm that MFA is          |
|     multi-factor authentication  |     implemented as per GC        |
|     (MFA) for all user accounts. |     guidance through             |
|     Use phishing resistant MFA   |     screenshots, compliance      |
|     where and when available.    |     reports, or compliance check |
|                                  |     enabled through a reporting  |
| *(Note: User accounts and        |     tool for all user accounts.  |
| identities include:*             |                                  |
|                                  | -   Confirm that digital         |
| 1.  *Root/Global administrator   |     policies are in place to     |
|     (as it is one that that has  |     ensure that MFA              |
|     enhanced/highest level of    |     configurations are enforced. |
|     privileges over the control  |                                  |
|     plane and addresses all      | -   Confirm and report the count |
|     aspects of access control).* |     of Root/Global administrator |
|                                  |     registered (should have at   |
| 2.  *Other Administrative user   |     least two and no more than   |
|     accounts. Refer to Section 4 |     five).                       |
|     of the "[Directive on        |                                  |
|     Service and Digital-         |                                  |
|     Cana                         |                                  |
| da.ca](https://www.tbs-sct.canad |                                  |
| a.ca/pol/doc-eng.aspx?id=32601), |                                  |
|     [Appendix G: Standard on     |                                  |
|     Enterprise Information       |                                  |
|     Technology Service Common    |                                  |
|     Configurations-              |                                  |
|     Canad                        |                                  |
| a.ca](https://www.tbs-sct.canada |                                  |
| .ca/pol/doc-eng.aspx?id=32713) - |                                  |
|     [Account Management          |                                  |
|     Configuration Requirements - |                                  |
|     Canada.ca](https://www.      |                                  |
| canada.ca/en/government/system/d |                                  |
| igital-government/policies-stand |                                  |
| ards/enterprise-it-service-commo |                                  |
| n-configurations/account.html)"* |                                  |
|     *for the definition of       |                                  |
|     privileged accounts.*        |                                  |
|                                  |                                  |
| 3.  ***Regular user accounts)*** |                                  |
+----------------------------------+----------------------------------+
| -   Configure alerting to ensure | -   ***Confirm if monitoring and |
|     the prompt detection of a    |     auditing is implemented for  |
|     potential compromise, in     |     all user accounts.***        |
|     accordance with the GC Event |                                  |
|     Logging Guidance.            | -   Confirm alert notification   |
|                                  |     to the authorized personnel  |
|                                  |     is implemented for flagging  |
|                                  |     misuse, suspicious           |
|                                  |     activities , for all user    |
|                                  |     accounts.                    |
+----------------------------------+----------------------------------+
| -   Use separate dedicated       | -   Provide evidence that        |
|     accounts for highly          |     dedicated user accounts are  |
|     privileged roles (e.g.       |     used for administration      |
|     domain admins, global        |     (e.g., privileged access).   |
|     admins, root, and any domain |                                  |
|     admin equivalent access)     |                                  |
|     when administering cloud     |                                  |
|     services to minimize the     |                                  |
|     blast radius.                |                                  |
+----------------------------------+----------------------------------+
| ***Additional Considerations***  |                                  |
+----------------------------------+----------------------------------+
| ***None***                       |                                  |
+----------------------------------+----------------------------------+
| ***References***                 |                                  |
|                                  |                                  |
| 1.  , subsection 6.2.3           |                                  |
|                                  |                                  |
| 2.  CSE Top 10 \#3               |                                  |
|                                  |                                  |
| 3.  Refer to the [ ]{.underline} |                                  |
|     [Recommendations for         |                                  |
|     Two-Factor User              |                                  |
|     Authentication Within the    |                                  |
|     Government of Canada         |                                  |
|     Enterprise                   |                                  |
|     Domain](https://intranet.ca  |                                  |
| nada.ca/wg-tg/rtua-rafu-eng.asp) |                                  |
|                                  |                                  |
| 4.  Refer to the [GC             |                                  |
|     Multi-Factor Authentication  |                                  |
|     (MFA) Strategy               |                                  |
|     Paper](h                     |                                  |
| ttps://www.gcpedia.gc.ca/gcwiki/ |                                  |
| images/9/9e/GC_MFA_Strategy.pdf) |                                  |
|                                  |                                  |
| 5.  Refer to the [Directive on   |                                  |
|     Service and                  |                                  |
|     Di                           |                                  |
| gital](https://www.tbs-sct.canad |                                  |
| a.ca/pol/doc-eng.aspx?id=32601), |                                  |
|     [Appendix G: Standard on     |                                  |
|     Enterprise Information       |                                  |
|     Technology Service Common    |                                  |
|     Configurat                   |                                  |
| ions](https://www.tbs-sct.canada |                                  |
| .ca/pol/doc-eng.aspx?id=32713) - |                                  |
|     [Account Management          |                                  |
|     Configuration                |                                  |
|     Requirements](https://ww     |                                  |
| w.canada.ca/en/government/system |                                  |
| /digital-government/policies-sta |                                  |
| ndards/enterprise-it-service-com |                                  |
| mon-configurations/account.html) |                                  |
|                                  |                                  |
| 6.  Refer to the [GC Event       |                                  |
|     Logging                      |                                  |
|     Guidance](https://www        |                                  |
| .gcpedia.gc.ca/gcwiki/images/e/e |                                  |
| 3/GC_Event_Logging_Strategy.pdf) |                                  |
|                                  |                                  |
| 7.  Refer to [ITSP.50.104        |                                  |
|     Guidance on defence in depth |                                  |
|     for cloud-based              |                                  |
|     s                            |                                  |
| ervices,](https://cyber.gc.ca/en |                                  |
| /guidance/itsp50104-guidance-def |                                  |
| ence-depth-cloud-based-services) |                                  |
|     subsection 4.6               |                                  |
|                                  |                                  |
| 8.  [User authentication         |                                  |
|     guidance for information     |                                  |
|     technology systems           |                                  |
|     (ITSP.30.031                 |                                  |
|     v3)](https://www.c           |                                  |
| yber.gc.ca/en/guidance/user-auth |                                  |
| entication-guidance-information- |                                  |
| technology-systems-itsp30031-v3) |                                  |
+----------------------------------+----------------------------------+
| **Related security controls:**   |                                  |
| AC-2, AC-2(11), AC-3, AC-5,      |                                  |
| AC-6, AC- 6(5), AC- 6(10),       |                                  |
| AC-19, AC -- 20 (3), IA-2,       |                                  |
| IA-2(1)                          |                                  |
|                                  |                                  |
| *IA - 2(2), IA-2(3), IA --       |                                  |
| 2(11), IA-5(8), SI-4, SI-4(5),   |                                  |
| SA-4(12), CM-5.*                 |                                  |
+----------------------------------+----------------------------------+

Guardrail \#2 -- Manage access
------------------------------

+----------------------------------+----------------------------------+
| **Objective:** Establish access  |                                  |
| control policies and procedures  |                                  |
| for management of all accounts.  |                                  |
+==================================+==================================+
| ***Applicable Service Models:    |                                  |
| IaaS, PaaS, SaaS***              |                                  |
+----------------------------------+----------------------------------+
| ***Mandatory Requirements***     | ***Validation***                 |
+----------------------------------+----------------------------------+
| -   Implement a mechanism for    | -   Demonstrate access           |
|     enforcing access             |     configurations and policies  |
|     authorizations for all user  |     are implemented for          |
|     accounts, based on criteria  |     different classes of users   |
|     listed in Directive on       |     (non-privileged, and         |
|     Service and Digital Appendix |     privileged users).           |
|     G -- Account Management      |                                  |
|     Configuration Requirements   | -   Confirm that the access      |
|     -- Section 3.                |     authorization mechanisms     |
|                                  |     have been implemented for    |
|                                  |     the following:               |
|                                  |                                  |
|                                  | 1.  To uniquely identify and     |
|                                  |     authenticate users to the    |
|                                  |     cloud service;               |
|                                  |                                  |
|                                  | 2.  Validating that the least    |
|                                  |     privilege role is assigned;  |
|                                  |                                  |
|                                  | 3.  Validating that Role Based   |
|                                  |     Access is implemented;       |
|                                  |                                  |
|                                  | 4.  Terminating of role          |
|                                  |     assignment upon job change   |
|                                  |     or termination;              |
|                                  |                                  |
|                                  | 5.  Performing periodic reviews  |
|                                  |     of role assignment (minimum  |
|                                  |     yearly);                     |
|                                  |                                  |
|                                  | 6.  Disabling default and        |
|                                  |     dormant accounts;            |
|                                  |                                  |
|                                  | 7.  Avoiding use of user generic |
|                                  |     accounts.                    |
|                                  |                                  |
|                                  | -   Verify that a review of      |
|                                  |     Root/Global administrator    |
|                                  |     accounts role assignment is  |
|                                  |     performed at a minimum every |
|                                  |     12 months.                   |
+----------------------------------+----------------------------------+
| -   Leverage role-based access   | -   Demonstrate that cloud       |
|     that are configured with     |     platform built-in roles are  |
|     least privileges. This can   |     used with least privileges.  |
|     include built-in roles or    |     Custom roles can be used but |
|     custom roles that have been  |     rationale should be          |
|     established with only the    |     documented and approved.     |
|     minimum number of privileges |                                  |
|     required to perform the job  |                                  |
|     function.                    |                                  |
+----------------------------------+----------------------------------+
| -   Change default passwords in  | -   Confirm that the default     |
|     accordance with the GC       |     passwords have been changed  |
|     password guidance.           |     for all the built-in         |
|                                  |     accounts for the             |
|                                  |     cloud-service.               |
+----------------------------------+----------------------------------+
| -   Configure the default        | -   Demonstrate that password    |
|     password policy in           |     policy for the cloud         |
|     accordance with [GC Password |     platform has been configured |
|     Guidance](https://www.ca     |     as per the GC Password       |
| nada.ca/en/government/system/dig |     Guidance:                    |
| ital-government/online-security- |                                  |
| privacy/password-guidance.html). |     1.  Require longer passwords |
|                                  |         -- At least 12           |
|                                  |         characters in length     |
|                                  |         without a maximum length |
|                                  |         limit;                   |
|                                  |                                  |
|                                  |     2.  Counter online guessing  |
|                                  |         or brute forcing of      |
|                                  |         passwords using          |
|                                  |         throttling, account      |
|                                  |         lockout policies,        |
|                                  |         monitoring, and          |
|                                  |         multi-factor             |
|                                  |         authentication;          |
|                                  |                                  |
|                                  |     3.  Protect against offline  |
|                                  |         attacks using effecting  |
|                                  |         hashing, salting, and    |
|                                  |         keyed hashing.           |
+----------------------------------+----------------------------------+
| -   Implement password           | -   Confirm that mechanisms,     |
|     protection mechanisms to     |     such as throttling, account  |
|     protect against password     |     lock out policies,           |
|     brute force attacks.         |     monitoring and risk based    |
|                                  |     authentication, to protect   |
|                                  |     against password bruteforce  |
|                                  |     attacks have been            |
|                                  |     implemented                  |
+----------------------------------+----------------------------------+
| -   Establish a guest user       | -   Confirm only the required    |
|     access policy and procedures |     guest user accounts are      |
|     that minimizes the number of |     enabled (The required guest  |
|     guest users and manages      |     user accounts are as per the |
|     their lifecycle where        |     business requirements of the |
|     accounts are deprovisioned   |     service)                     |
|     when access is no longer     |                                  |
|     needed.                      | -   Provide list of              |
|                                  |     non-organizational users     |
| > ***(Note: A guest is someone   |     with elevated privileges.    |
| > who isn\'t an employee,        |                                  |
| > student, or member of your     | -   *Verify that periodic guest  |
| > organization. They don\'t have |     access reviews are performed |
| > an existing account with the   |     periodically.*               |
| > organization's cloud           |                                  |
| > tenant).***                    |                                  |
+----------------------------------+----------------------------------+
| ***Additional Considerations***  |                                  |
+----------------------------------+----------------------------------+
| -   Document a process for       | -   Confirm that the Access      |
|     managing accounts, access    |     Control procedure for        |
|     privileges, and access       |     management of administrative |
|     credentials for              |     accounts have been           |
|     organizational users,        |     documented for the cloud     |
|     non-organizational users (if |     service. The procedure       |
|     required), based on criteria |     should include provision for |
|     listed in Directive on       |     any guest accounts, custom   |
|     Service and Digital Appendix |     accounts, and must reference |
|     G -- Account Management      |     to the Emergency Break Glass |
|     Configuration Requirements   |     procedure.                   |
|     -- Section 3. This process   |                                  |
|     should be approved by Chief  |                                  |
|     Security Officer (CSO) (or   |                                  |
|     delegate) and designated     |                                  |
|     official for cyber security. |                                  |
+----------------------------------+----------------------------------+
| -   ***Enforce just-in-time      | -   ***Confirm that just-in-time |
|     access for privileged user   |     access for all privileged    |
|     accounts to provide          |     user accounts to provide     |
|     time-based and               |     time-based and               |
|     approval-based role          |     approval-based role          |
|     activation to mitigate the   |     activation.***               |
|     risks of excessive,          |                                  |
|     unnecessary, or misused      |                                  |
|     access permissions.***       |                                  |
+----------------------------------+----------------------------------+
| -   ***Enforce attribute-based   | -   ***Provide evidence that     |
|     access control (ABAC) to     |     attribute-based access       |
|     restrict access based on     |     control (ABAC) mechanisms    |
|     combination of               |     are in place to restrict     |
|     authentication factors       |     access based on              |
|     (MFA), , GC issued and       |     attributes/signals such as   |
|     managed devices, device      |     authentication factors       |
|     compliance, sign-in and user |     (MFA), GC issued and managed |
|     risks, and location.***      |     devices, device compliance,  |
|                                  |     sign-in and user risks, and  |
|                                  |     location.***                 |
+----------------------------------+----------------------------------+
| -   ***Leverage tools such as    | -   ***Provide evidence that all |
|     privilege access management  |     privileged user accounts     |
|     systems to enforce access    |     role activation requires     |
|     control to privilege         |     approval, and that privilege |
|     functions by configuring     |     elevation is time-bound      |
|     roles that requires approval |     (temporary activation).***   |
|     for activation and choose    |                                  |
|     one or multiple users or     |                                  |
|     groups as delegated          |                                  |
|     approvers.***                |                                  |
+----------------------------------+----------------------------------+
| -                                | -                                |
+----------------------------------+----------------------------------+
| ***References***                 |                                  |
|                                  |                                  |
| 1.  , subsection 6.2.3           |                                  |
|                                  |                                  |
| 2.  CSE Top 10 \#3               |                                  |
|                                  |                                  |
| 3.  Refer to [User               |                                  |
|     authentication guidance for  |                                  |
|     information technology       |                                  |
|     systems (ITSP.30.031         |                                  |
|     v3)](https://www.c           |                                  |
| yber.gc.ca/en/guidance/user-auth |                                  |
| entication-guidance-information- |                                  |
| technology-systems-itsp30031-v3) |                                  |
|                                  |                                  |
| 4.  Refer to the [ ]{.underline} |                                  |
|     [Guidance on Cloud           |                                  |
|     Authentication for the       |                                  |
|     Government of                |                                  |
|     Canada](https://intranet.ca  |                                  |
| nada.ca/wg-tg/cagc-angc-eng.asp) |                                  |
|                                  |                                  |
| 5.  Refer to the [ ]{.underline} |                                  |
|     [Recommendations for         |                                  |
|     Two-Factor User              |                                  |
|     Authentication Within the    |                                  |
|     Government of Canada         |                                  |
|     Enterprise                   |                                  |
|     Domain](https://intranet.ca  |                                  |
| nada.ca/wg-tg/rtua-rafu-eng.asp) |                                  |
|                                  |                                  |
| 6.  Refer to the [Directive on   |                                  |
|     Service and                  |                                  |
|     Di                           |                                  |
| gital](https://www.tbs-sct.canad |                                  |
| a.ca/pol/doc-eng.aspx?id=32601), |                                  |
|     [Appendix G: Standard on     |                                  |
|     Enterprise Information       |                                  |
|     Technology Service Common    |                                  |
|     Configurat                   |                                  |
| ions](https://www.tbs-sct.canada |                                  |
| .ca/pol/doc-eng.aspx?id=32713) - |                                  |
|     [Account Management          |                                  |
|     Configuration                |                                  |
|     Requirements](https://ww     |                                  |
| w.canada.ca/en/government/system |                                  |
| /digital-government/policies-sta |                                  |
| ndards/enterprise-it-service-com |                                  |
| mon-configurations/account.html) |                                  |
|                                  |                                  |
| 7.  Refer to [ITSP.50.104        |                                  |
|     Guidance on defence in depth |                                  |
|     for cloud-based              |                                  |
|     s                            |                                  |
| ervices,](https://cyber.gc.ca/en |                                  |
| /guidance/itsp50104-guidance-def |                                  |
| ence-depth-cloud-based-services) |                                  |
|     subsection 4.6               |                                  |
|                                  |                                  |
| 8.  [GC Password                 |                                  |
|     Guidance](https://www.c      |                                  |
| anada.ca/en/government/system/di |                                  |
| gital-government/online-security |                                  |
| -privacy/password-guidance.html) |                                  |
+----------------------------------+----------------------------------+
| **Related security controls:**   |                                  |
| AC‑2, AC‑2(1), AC‑2(7) AC‑3,     |                                  |
| AC‑3(7), AC‑3, AC‑4 AC‑5, AC‑6,  |                                  |
| AC‑6(5), IA‑2, IA‑2(1), IA‑2(8), |                                  |
| IA‑2(11), IA‑4, IA‑5, IA‑5(1),   |                                  |
| IA‑5(6)                          |                                  |
+----------------------------------+----------------------------------+

Guardrail \#3 -- Secure endpoints
---------------------------------

+----------------------------------+----------------------------------+
| ***Objective:*** Implement       |                                  |
| increased levels of protection   |                                  |
| for management interfaces.       |                                  |
+==================================+==================================+
| ***Applicable Service Models:    |                                  |
| IaaS, PaaS, SaaS***              |                                  |
+----------------------------------+----------------------------------+
| ***Mandatory Requirements***     | ***Validation***                 |
+----------------------------------+----------------------------------+
| -   **Implement access           | -   Confirm that administrative  |
|     restrictions to ensure the   |     access to cloud environments |
|     use GC issued and managed    |     is from approved and trusted |
|     devices that are patched and |     locations and **GC issued    |
|     managed, in accordance with  |     and** managed devices that   |
|     [GC Endpoint Management      |     enforce the GC endpoint      |
|     Configuration                |     management configuration     |
|     Requirements](https://www.ca |     requirements.                |
| nada.ca/en/government/system/dig |                                  |
| ital-government/policies-standar | ```{=html}                       |
| ds/enterprise-it-service-common- | <!-- -->                         |
| configurations/endpoint.html).** | ```                              |
|                                  | -   ***Demonstrate access        |
|                                  |     configurations and policies  |
|                                  |     are implemented for          |
|                                  |     devices.***                  |
+----------------------------------+----------------------------------+
| ***Additional Considerations***  |                                  |
+----------------------------------+----------------------------------+
| -   ***All administrative tasks  | -   Confirm if dedicated         |
|     should be undertaken on      |     ***administrative            |
|     dedicated administrative     |     workstations*** are utilized |
|     workstations.***             |     to conduct all               |
|                                  |     administrative activities    |
| > ***(Note: A dedicated          |                                  |
| > administrative workstation is  |                                  |
| > a secured physical (thick or   |                                  |
| > thin) client workstation used  |                                  |
| > to perform specific and        |                                  |
| > sensitive administrative tasks |                                  |
| > or tasks requiring privileged  |                                  |
| > access. This device must have  |                                  |
| > no Internet access and         |                                  |
| > services such as email and web |                                  |
| > browsing must be disabled and  |                                  |
| > prohibited)***                 |                                  |
+----------------------------------+----------------------------------+
| ***References***                 |                                  |
|                                  |                                  |
| 1.  , subsection 6.2.3           |                                  |
|                                  |                                  |
| 2.  CSE Top 10 \#2               |                                  |
|                                  |                                  |
| 3.  Refer to the [ ]{.underline} |                                  |
|     [Recommendations for         |                                  |
|     Two-Factor User              |                                  |
|     Authentication Within the    |                                  |
|     Government of Canada         |                                  |
|     Enterprise                   |                                  |
|     Domain](https://intranet.ca  |                                  |
| nada.ca/wg-tg/rtua-rafu-eng.asp) |                                  |
|                                  |                                  |
| 4.  Refer to the [Directive on   |                                  |
|     Service and                  |                                  |
|     Di                           |                                  |
| gital](https://www.tbs-sct.canad |                                  |
| a.ca/pol/doc-eng.aspx?id=32601), |                                  |
|     [Appendix G: Standard on     |                                  |
|     Enterprise Information       |                                  |
|     Technology Service Common    |                                  |
|     Configurat                   |                                  |
| ions](https://www.tbs-sct.canada |                                  |
| .ca/pol/doc-eng.aspx?id=32713) - |                                  |
|     [Endpoint Management         |                                  |
|     Configuration                |                                  |
|     Requirements](https://www    |                                  |
| .canada.ca/en/government/system/ |                                  |
| digital-government/policies-stan |                                  |
| dards/enterprise-it-service-comm |                                  |
| on-configurations/endpoint.html) |                                  |
|                                  |                                  |
| 5.  Refer to [ITSP.50.104        |                                  |
|     Guidance on defence in depth |                                  |
|     for cloud-based              |                                  |
|     s                            |                                  |
| ervices,](https://cyber.gc.ca/en |                                  |
| /guidance/itsp50104-guidance-def |                                  |
| ence-depth-cloud-based-services) |                                  |
|     subsection 4.9.              |                                  |
+----------------------------------+----------------------------------+
| **Related security controls**:   |                                  |
| AC3, AC-3(7), AC-4, AC5, AC6,    |                                  |
| AC6(5), AC6(10), AC19, AC20(3),  |                                  |
| IA2, IA2(1),IA2(11), IA4, IA5,   |                                  |
| IA5(1), SI-4, AU-6, AU-12        |                                  |
+----------------------------------+----------------------------------+

Guardrail \#4 -- Enterprise monitoring accounts
-----------------------------------------------

+----------------------------------+----------------------------------+
| ***Objective:*** Create          |                                  |
| role-based account to enable     |                                  |
| enterprise monitoring and        |                                  |
| visibility                       |                                  |
+==================================+==================================+
| ***Applicable Service Models:    |                                  |
| IaaS, PaaS, SaaS***              |                                  |
+----------------------------------+----------------------------------+
| ***Mandatory Requirements***     | ***Validation***                 |
+----------------------------------+----------------------------------+
| -                                | -   ***Verify that roles         |
|                                  |     required to enable GC        |
| ***Create role-based account to  |     visibility to have been      |
| enable enterprise monitoring and |     provisioned/assigned.***     |
| visibility for cloud             |                                  |
| environments that are procured   |                                  |
| via the GC Cloud Broker or are   |                                  |
| included in scope of centralized |                                  |
| guardrails validation.***        |                                  |
+----------------------------------+----------------------------------+
| -   Review access privileges     | -   ***Confirm alert             |
|     periodically and remove      |     notification to the          |
|     access when it is no longer  |     authorized personnel is      |
|     required.                    |     implemented flagging misuse, |
|                                  |     suspicious sign-in attempts, |
|                                  |     or when changes are made to  |
|                                  |     the privileged and           |
|                                  |     non-privileged accounts.***  |
+----------------------------------+----------------------------------+
| ***Additional Considerations***  |                                  |
+----------------------------------+----------------------------------+
| ***None***                       |                                  |
+----------------------------------+----------------------------------+
| ***References***                 |                                  |
|                                  |                                  |
| 1.  , subsection 6.2.3           |                                  |
|                                  |                                  |
| 2.  CSE Top 10 \#2               |                                  |
+----------------------------------+----------------------------------+
| **Related security controls**:   |                                  |
| AC-3(7), AC-6(5), IA-2(1)        |                                  |
+----------------------------------+----------------------------------+

Guardrail \#5 -- Data location
------------------------------

+----------------------------------+----------------------------------+
| ***Objective:*** Establish       |                                  |
| policies to restrict GC          |                                  |
| sensitive workloads to approved  |                                  |
| geographic locations             |                                  |
+==================================+==================================+
| ***Applicable Service Models:    |                                  |
| IaaS, PaaS, SaaS***              |                                  |
+----------------------------------+----------------------------------+
| ***Mandatory Requirements***     | ***Validation***                 |
+----------------------------------+----------------------------------+
| -   As per Section 4.4.3.14 of   | -   ***Demonstrate that service  |
|     the Directive on Service and |     location is within Canada    |
|     Digital, "Ensuring computing |     (For all PB cloud-services)  |
|     facilities located within    |     where configurable , in      |
|     the geographic boundaries of |     accordance with the          |
|     Canada or within the         |     applicable cloud usage       |
|     premises of a Government of  |     profiles.***                 |
|     Canada department located    |                                  |
|     abroad, such as a diplomatic | -                                |
|     or consular mission, be      |                                  |
|     identified and evaluated as  |                                  |
|     a principal delivery option  |                                  |
|     for all sensitive electronic |                                  |
|     information and data under   |                                  |
|     government control that has  |                                  |
|     been categorized as          |                                  |
|     Protected B, Protected C or  |                                  |
|     is Classified."              |                                  |
+----------------------------------+----------------------------------+
| ***Additional Considerations***  |                                  |
+----------------------------------+----------------------------------+
| ***None***                       |                                  |
+----------------------------------+----------------------------------+
| ***References***                 |                                  |
|                                  |                                  |
| 1.  , subsection 6.2.3           |                                  |
|                                  |                                  |
| 2.  Refer to [Directive on       |                                  |
|     Service and                  |                                  |
|     Di                           |                                  |
| gita](https://www.tbs-sct.canada |                                  |
| .ca/pol/doc-eng.aspx?id=32601)l, |                                  |
|     subsection 4.4.3.14          |                                  |
+----------------------------------+----------------------------------+
| **Related security controls**:   |                                  |
| SA-9(5)                          |                                  |
+----------------------------------+----------------------------------+

Guardrail \#6 -- Protection of data-at-rest 
-------------------------------------------

+----------------------------------+----------------------------------+
| ***Objective:*** Protect data at |                                  |
| rest by default (e.g., storage)  |                                  |
| for cloud-based workloads        |                                  |
+==================================+==================================+
| ***Applicable Service Models:    |                                  |
| IaaS, PaaS, SaaS***              |                                  |
+----------------------------------+----------------------------------+
| ***Mandatory Requirements***     | ***Validation***                 |
+----------------------------------+----------------------------------+
| -   ***Implement an encryption   | -   ***For IaaS and PaaS,        |
|     mechanism to protect the     |     confirm that storage service |
|     confidentiality and          |     encryption is enabled for    |
|     integrity of data when data  |     data at rest (if required    |
|     are at rest in your          |     based on the security risk   |
|     solution\'s storage.***      |     assessment).***              |
|                                  |                                  |
|                                  | -   ***For SaaS, confirm that    |
|                                  |     the CSP has implemented      |
|                                  |     encryption to protect        |
|                                  |     customer data.***            |
+----------------------------------+----------------------------------+
| -   ***Use CSE-approved          | -   ***Cryptographic algorithms  |
|     cryptographic algorithms and |     and protocols configurable   |
|     protocols, in accordance     |     by the consumer are          |
|     with ITSP.40.111 and         |     leveraged in accordance with |
|     ITSP.40.062.***              |     ITSP 40.111 and 40.062.***   |
|                                  |                                  |
|                                  | -   ***For SaaS, confirm that    |
|                                  |     the CSP has implemented      |
|                                  |     algorithms that align with   |
|                                  |     ITSP 40.111 and 40.062.***   |
+----------------------------------+----------------------------------+
| ***Additional Considerations***  |                                  |
+----------------------------------+----------------------------------+
| -   ***Seek guidance from        | -   Confirm that privacy is      |
|     privacy and access to        |     included as part of the      |
|     information officials within |     Departmental SDLC process.   |
|     institutions before storing  |                                  |
|     personal information in      |                                  |
|     cloud-based environments.*** |                                  |
+----------------------------------+----------------------------------+
| -   Leverage an appropriate key  | -   Confirm that a key           |
|     management system for the    |     management strategy has been |
|     cryptographic protection     |     adopted for the cloud        |
|     used in cloud-based          |     tenant.                      |
|     services, in accordance with |                                  |
|     GC Considerations for the    |                                  |
|     Use of Cryptography in       |                                  |
|     Commercial Cloud Services    |                                  |
|     and CCCS guidance on key     |                                  |
|     management at Guidance on    |                                  |
|     cloud                        |                                  |
|     [service](https://www.cyber. |                                  |
| gc.ca/en/guidance/guidance-cloud |                                  |
| -service-cryptography-itsp50106) |                                  |
|     cryptography (ITSP.50.106).  |                                  |
+----------------------------------+----------------------------------+
| ***References***                 |                                  |
|                                  |                                  |
| 1.  , subsection 6.2.4           |                                  |
|                                  |                                  |
| 2.  Refer to the cryptography    |                                  |
|     guidance in                  |                                  |
|     [ITS                         |                                  |
| P.40.111](https://cyber.gc.ca/en |                                  |
| /guidance/cryptographic-algorith |                                  |
| ms-unclassified-protected-and-pr |                                  |
| otected-b-information-itsp40111) |                                  |
|     and                          |                                  |
|     [ITSP.40.062]                |                                  |
| (https://www.cyber.gc.ca/en/guid |                                  |
| ance/guidance-securely-configuri |                                  |
| ng-network-protocols-itsp40062). |                                  |
|                                  |                                  |
| 3.  Refer to the guidance in     |                                  |
|     Guidance on cloud            |                                  |
|     [service](https://www.cyber. |                                  |
| gc.ca/en/guidance/guidance-cloud |                                  |
| -service-cryptography-itsp50106) |                                  |
|     cryptography (ITSP.50.106)   |                                  |
|                                  |                                  |
| 4.  Refer to [ITSP.50.104        |                                  |
|     Guidance on defence in depth |                                  |
|     for cloud-based              |                                  |
|     s                            |                                  |
| ervices,](https://cyber.gc.ca/en |                                  |
| /guidance/itsp50104-guidance-def |                                  |
| ence-depth-cloud-based-services) |                                  |
|     subsection 4.5.              |                                  |
+----------------------------------+----------------------------------+
| **Related security controls:**   |                                  |
| IA-7, SC-12, SC-13, SC-28,       |                                  |
| SC-28(1)                         |                                  |
+----------------------------------+----------------------------------+

Guardrail \#7 -- Protection of data-in-transit
----------------------------------------------

+----------------------------------+----------------------------------+
| ***Objective:*** Protect data    |                                  |
| transiting networks through the  |                                  |
| use of appropriate encryption    |                                  |
| and network safeguards           |                                  |
+==================================+==================================+
| ***Applicable Service Models:    |                                  |
| IaaS, PaaS, SaaS***              |                                  |
+----------------------------------+----------------------------------+
| ***Mandatory Requirements***     | ***Validation***                 |
+----------------------------------+----------------------------------+
| -   **Encrypt data in transit by | -   ***Confirm that TLS v1.2 or  |
|     default (e.g., TLS v1.2,     |     above encryption is          |
|     etc.) to protect the         |     implemented for all cloud    |
|     confidentiality and          |     services (via HTTPS, TLS or  |
|     integrity of data, including |     other mechanism).***         |
|     for all publicly accessible  |                                  |
|     sites and external           | ***(Note: While this is often    |
|     communications as per the GC | the default, cloud platforms and |
|     Website and Services         | cloud services often have        |
|     Configuration Requirements,  | configuration options to select  |
|     and wherever possible for    | the permitted TLS version.)***   |
|     internal zone                |                                  |
|     communication.**             |                                  |
+----------------------------------+----------------------------------+
| -   **Use CSE-approved           | -   ***Cryptographic algorithms  |
|     cryptographic algorithms and |     and protocols configurable   |
|     protocols, in accordance     |     by the consumer are          |
|     with ITSP.40.111 and         |     leveraged in accordance with |
|     ITSP.40.062.**               |     ITSP 40.111 and 40.062.***   |
+----------------------------------+----------------------------------+
| -   **Leverage non-person entity | -   ***Confirm that NPE          |
|     certificates from            |     certificates are issued from |
|     certificate authorities that |     certificate authorities that |
|     align with the               |     align with GC                |
|     Recommendations for TLS      |     recommendations for TLS      |
|     Server Certificates.**       |     server certificates.***      |
+----------------------------------+----------------------------------+
| ***Additional Considerations***  |                                  |
+----------------------------------+----------------------------------+
| ***None***                       |                                  |
+----------------------------------+----------------------------------+
| ***References***                 |                                  |
|                                  |                                  |
| 1.  , subsection 6.2.4           |                                  |
|                                  |                                  |
| 2.  Refer to the [Directive on   |                                  |
|     Service and                  |                                  |
|     Di                           |                                  |
| gital](https://www.tbs-sct.canad |                                  |
| a.ca/pol/doc-eng.aspx?id=32601), |                                  |
|     [Appendix G: Standard on     |                                  |
|     Enterprise Information       |                                  |
|     Technology Service Common    |                                  |
|     Configur                     |                                  |
| ations](https://www.tbs-sct.cana |                                  |
| da.ca/pol/doc-eng.aspx?id=32713) |                                  |
|     -- [Web Sites and Services   |                                  |
|     Management Configuration     |                                  |
|     Requirements](https://www.   |                                  |
| canada.ca/en/government/system/d |                                  |
| igital-government/policies-stand |                                  |
| ards/enterprise-it-service-commo |                                  |
| n-configurations/web-sites.html) |                                  |
|                                  |                                  |
| 3.  Refer to the cryptography    |                                  |
|     guidance in                  |                                  |
|     [ITS                         |                                  |
| P.40.111](https://cyber.gc.ca/en |                                  |
| /guidance/cryptographic-algorith |                                  |
| ms-unclassified-protected-and-pr |                                  |
| otected-b-information-itsp40111) |                                  |
|     and                          |                                  |
|     [ITSP.40.062                 |                                  |
| ](https://www.cyber.gc.ca/en/gui |                                  |
| dance/guidance-securely-configur |                                  |
| ing-network-protocols-itsp40062) |                                  |
|                                  |                                  |
| 4.  Refer to the network         |                                  |
|     security zoning guidance in  |                                  |
|     [ITSG-22](https://cyber.gc   |                                  |
| .ca/en/guidance/baseline-securit |                                  |
| y-requirements-network-security- |                                  |
| zones-government-canada-itsg-22) |                                  |
|     and                          |                                  |
|                                  |                                  |
| [ITSG-38](https://cyber.gc.ca/en |                                  |
| /guidance/network-security-zonin |                                  |
| g-design-considerations-placemen |                                  |
| t-services-within-zones-itsg-38) |                                  |
|                                  |                                  |
| 5.  Refer to the guidance in     |                                  |
|     Guidance on cloud            |                                  |
|     [service](https://www.cyber. |                                  |
| gc.ca/en/guidance/guidance-cloud |                                  |
| -service-cryptography-itsp50106) |                                  |
|     cryptography (ITSP.50.106)   |                                  |
|                                  |                                  |
| 6.  [Government of Canada        |                                  |
|     Recommendations for TLS      |                                  |
|     Server Certificates for GC   |                                  |
|     Public Facing Web            |                                  |
|     Services](htt                |                                  |
| ps://wiki.gccollab.ca/images/9/9 |                                  |
| 2/Recommendations_for_TLS_Server |                                  |
| _Certificates_-_14_May_2021.pdf) |                                  |
|                                  |                                  |
| 7.  Refer to [ITSP.50.104        |                                  |
|     Guidance on defence in depth |                                  |
|     for cloud-based              |                                  |
|     s                            |                                  |
| ervices](https://cyber.gc.ca/en/ |                                  |
| guidance/itsp50104-guidance-defe |                                  |
| nce-depth-cloud-based-services), |                                  |
|     subsection 4.5               |                                  |
+----------------------------------+----------------------------------+
| **Related security controls:**   |                                  |
| IA-7,SC-12, SC-13, SC-28,        |                                  |
| SC-28(1)                         |                                  |
+----------------------------------+----------------------------------+

***Guardrail*** \#8 -- Segment and separate
-------------------------------------------

+----------------------------------+----------------------------------+
| ***Objective:*** Segment and     |                                  |
| separate information based on    |                                  |
| sensitivity of information       |                                  |
+==================================+==================================+
| ***Applicable Service Models:*** |                                  |
| ***IaaS, PaaS***                 |                                  |
|                                  |                                  |
| ***(Note: The following          |                                  |
| guardrail is not applicable for  |                                  |
| SaaS model. Management and       |                                  |
| security of the network is a     |                                  |
| Cloud Service Provider           |                                  |
| responsibility and is included   |                                  |
| as part of the SaaS offering.    |                                  |
| Please refer to [ITSP.50.104     |                                  |
| Guidance on defence in depth for |                                  |
| cloud-based                      |                                  |
| serv                             |                                  |
| ices](https://www.cyber.gc.ca/en |                                  |
| /guidance/itsp50104-guidance-def |                                  |
| ence-depth-cloud-based-services) |                                  |
| Section 4.3 to understand key    |                                  |
| considerations for cloud network |                                  |
| segmentation)***                 |                                  |
+----------------------------------+----------------------------------+
| ***Mandatory Requirements***     | ***Validation***                 |
+----------------------------------+----------------------------------+
| -   Isolate and secure cloud     | -   Confirm that department has  |
|     workloads based on the       |     a target network             |
|     sensitivity of the data.     |     architecture high level      |
|                                  |     design and / or diagram with |
|                                  |     appropriate segmentation     |
|                                  |     between network security     |
|                                  |     zones in alignment with      |
|                                  |     CSE's ITSP.50.104, ITSG-22   |
|                                  |     and ITSG-38.                 |
|                                  |                                  |
|                                  | ```{=html}                       |
|                                  | <!-- -->                         |
|                                  | ```                              |
|                                  | -   Confirm that the department  |
|                                  |     has documented a deployment  |
|                                  |     guide of the cloud platform  |
|                                  |     and associated services.     |
|                                  |     (The document is to capture  |
|                                  |     landing zone if applicable)  |
|                                  |                                  |
|                                  | -   Confirm that CSP             |
|                                  |     segmentation features are    |
|                                  |     leveraged to provide         |
|                                  |     segmentation of Management,  |
|                                  |     Prod, UAT, DEV, and test.    |
|                                  |     (For example, use of         |
|                                  |     subscription, instances, or  |
|                                  |     other cloud provider         |
|                                  |     construct).                  |
+----------------------------------+----------------------------------+
| **Additional Considerations**    |                                  |
+----------------------------------+----------------------------------+
| -   Develop a target network     | -   ***Leverage landing zones    |
|     security design that         |     that include pre-defined,    |
|     considers segmentation via   |     secured, multi-account       |
|     network security zones, in   |     support to allow different   |
|     alignment with ITSP.50.104,  |     workloads and teams to be    |
|     ITSG-22 and ITSG-38.         |     onboarded in an automated    |
|                                  |     manner.***                   |
+----------------------------------+----------------------------------+
| ***References***                 |                                  |
|                                  |                                  |
| 1.  , sub**section 6.2.4**       |                                  |
|                                  |                                  |
| 2.  CSE Top 10 \#5               |                                  |
|                                  |                                  |
| 3.  Refer to the network         |                                  |
|     security zoning guidance in  |                                  |
|     [ITSG-22](https://cyber.gc   |                                  |
| .ca/en/guidance/baseline-securit |                                  |
| y-requirements-network-security- |                                  |
| zones-government-canada-itsg-22) |                                  |
|     and                          |                                  |
|                                  |                                  |
| [ITSG-38](https://cyber.gc.ca/en |                                  |
| /guidance/network-security-zonin |                                  |
| g-design-considerations-placemen |                                  |
| t-services-within-zones-itsg-38) |                                  |
|                                  |                                  |
| 4.  Refer to [ITSP.50.104        |                                  |
|     Guidance on defence in depth |                                  |
|     for cloud-based              |                                  |
|     s                            |                                  |
| ervices](https://cyber.gc.ca/en/ |                                  |
| guidance/itsp50104-guidance-defe |                                  |
| nce-depth-cloud-based-services), |                                  |
|     subsections 4.3, 4.5         |                                  |
+----------------------------------+----------------------------------+
| **Related security controls:     |                                  |
| AC‑4, SC‑7**                     |                                  |
+----------------------------------+----------------------------------+

Guardrail \#9 -- Network security services
------------------------------------------

+----------------------------------+----------------------------------+
| ***Objective:** Establish        |                                  |
| external and internal network    |                                  |
| perimeters and monitor network   |                                  |
| traffic.*                        |                                  |
+==================================+==================================+
| ***Applicable Service Models:    |                                  |
| IaaS, PaaS, SaaS***              |                                  |
+----------------------------------+----------------------------------+
| ***Mandatory Requirements***     | ***Validation***                 |
+----------------------------------+----------------------------------+
| -   Ensure that egress/ingress   | -   ***Confirm policy for        |
|     points to and from GC        |     limiting number of public    |
|     cloud-based environments are |     IPs.***                      |
|     managed and monitored.       |                                  |
+----------------------------------+----------------------------------+
| -   Implement network boundary   | -   ***Confirm policy for        |
|     protection mechanisms for    |     network boundary             |
|     all external facing          |     protection.***               |
|     interfaces that enforce a    |                                  |
|     deny-all or                  |                                  |
|     allow-by-exception policy.   |                                  |
+----------------------------------+----------------------------------+
| -   Perimeter security services  | -   ***Confirm policy for        |
|     such as boundary protection, |     limiting to authorized       |
|     intrusion prevention         |     source IP addresses (e.g.,   |
|     services, proxy services,    |     GC IP addresses).***         |
|     TLS traffic inspection, etc. |                                  |
|     must be enabled based on     |                                  |
|     risk profile, in alignment   |                                  |
|     with GC Secure Connectivity  |                                  |
|     Requirements and CSE         |                                  |
|     guidance.                    |                                  |
+----------------------------------+----------------------------------+
| -   Ensure that access to cloud  | -   ***Confirm that storage      |
|     storage services is          |     accounts are not exposed to  |
|     protected and restricted to  |     the public.***               |
|     authorized security          |                                  |
|     zones/network, users, and    |                                  |
|     services.                    |                                  |
+----------------------------------+----------------------------------+
| ***Additional Considerations***  |                                  |
+----------------------------------+----------------------------------+
| -   ***Use centrally provisioned | -   Confirm if the department is |
|     network security services    |     intending to establish       |
|     where available.***          |     dedicated and secure         |
|                                  |     connections to on-premise    |
|                                  |     resources.                   |
+----------------------------------+----------------------------------+
| ***References***                 |                                  |
|                                  |                                  |
| 1.  , sub**section 6.2.4**       |                                  |
|                                  |                                  |
| 2.  CSE Top 10 \#1               |                                  |
|                                  |                                  |
| 3.  Refer to the network         |                                  |
|     security zoning guidance in  |                                  |
|     [ITSG-22](https://cyber.gc   |                                  |
| .ca/en/guidance/baseline-securit |                                  |
| y-requirements-network-security- |                                  |
| zones-government-canada-itsg-22) |                                  |
|     and                          |                                  |
|                                  |                                  |
| [ITSG-38](https://cyber.gc.ca/en |                                  |
| /guidance/network-security-zonin |                                  |
| g-design-considerations-placemen |                                  |
| t-services-within-zones-itsg-38) |                                  |
|                                  |                                  |
| 4.  Refer to [ITSP.50.104        |                                  |
|     Guidance on defence in depth |                                  |
|     for cloud-based              |                                  |
|     s                            |                                  |
| ervices](https://cyber.gc.ca/en/ |                                  |
| guidance/itsp50104-guidance-defe |                                  |
| nce-depth-cloud-based-services), |                                  |
|     subsection 4.3               |                                  |
+----------------------------------+----------------------------------+
| **Related security controls:     |                                  |
| AC-3, AC‑4, SC‑7, SC‑7(5), SI-4, |                                  |
| SI-4(18)**                       |                                  |
+----------------------------------+----------------------------------+

Guardrail \#10 -- Cyber defense services
----------------------------------------

+----------------------------------+----------------------------------+
| ***Objective:** Establish MOU    |                                  |
| for defensive services and       |                                  |
| threat monitoring protection     |                                  |
| services.*                       |                                  |
+==================================+==================================+
| ***Applicable Service Models:    |                                  |
| IaaS, PaaS, SaaS***              |                                  |
+----------------------------------+----------------------------------+
| ***Mandatory Requirements***     | ***Validation***                 |
+----------------------------------+----------------------------------+
| -   Sign an MOU with Canadian    | -   Confirmation from CCCS that  |
|     Centre for Cyber Security    |     the MOU has been signed by   |
|     (CCCS).                      |     the Department.              |
|     *(<CDOSe                     |                                  |
| rviceDeployments@cyber.gc.ca>.)* |                                  |
+----------------------------------+----------------------------------+
| -   Implement defensive services | -   Confirm that the sensors or  |
|     including HBS, CBS, and NBS  |     other cyber defense services |
|     in accordance with CCCS      |     by CCCS are implemented      |
|     onboarding guidance where    |     where available.             |
|     available.                   |                                  |
+----------------------------------+----------------------------------+
| ***Additional Considerations***  |                                  |
+----------------------------------+----------------------------------+
| ***None***                       |                                  |
+----------------------------------+----------------------------------+
| ***References***                 |                                  |
|                                  |                                  |
| 1)                               |                                  |
|   [SPIN 2017-01](https://www.can |                                  |
| ada.ca/en/treasury-board-secreta |                                  |
| riat/services/access-information |                                  |
| -privacy/security-identity-manag |                                  |
| ement/direction-secure-use-comme |                                  |
| rcial-cloud-services-spin.html), |                                  |
|     subsection 6.3               |                                  |
+----------------------------------+----------------------------------+
| **Related security controls:**   |                                  |
| SI‑4                             |                                  |
+----------------------------------+----------------------------------+

Guardrail \#11 -- Logging and monitoring
----------------------------------------

+----------------------------------+----------------------------------+
| ***Objective:*** Enable logging  |                                  |
| for the cloud environment and    |                                  |
| for cloud-based workloads.       |                                  |
+==================================+==================================+
| ***Applicable Service Models:    |                                  |
| IaaS, PaaS, SaaS***              |                                  |
+----------------------------------+----------------------------------+
| ***Mandatory Requirements***     | ***Validation***                 |
+----------------------------------+----------------------------------+
| -   Implement adequate level of  | -   ***Confirm policy for event  |
|     logging and reporting,       |     logging is implemented.***   |
|     including a security audit   |                                  |
|     log function in all          | -   ***This includes logs for    |
|     information systems.         |     the following:***            |
|                                  |                                  |
|                                  |     1.  ***Sign-in logs          |
|                                  |         (interactive and         |
|                                  |         non-interactive          |
|                                  |         sign-ins, API            |
|                                  |         sign-ins)***             |
|                                  |                                  |
|                                  |     2.  ***Access privilege and  |
|                                  |         group changes (including |
|                                  |         group membership and     |
|                                  |         group privilege          |
|                                  |         assignment)***           |
|                                  |                                  |
|                                  |     3.  ***Changes in            |
|                                  |         configuration of cloud   |
|                                  |         platform***              |
|                                  |                                  |
|                                  |     4.  ***Cloud resource        |
|                                  |         provisioning             |
|                                  |         activities.***           |
+----------------------------------+----------------------------------+
| -   Configure events within the  | -   Confirm if monitoring and    |
|     solution to support security |     auditing is implemented for  |
|     monitoring, in accordance    |     all users.                   |
|     with GC Event Logging        |                                  |
|     Guidance.                    |                                  |
+----------------------------------+----------------------------------+
| -   Ensure that the appropriate  | -   ***Confirm that the security |
|     contact information is       |     contact record within the    |
|     configured so that the CSP   |     account should be completed  |
|     can notify the GC            |     with details of at least two |
|     organization of incidents    |     (if multiple permitted by    |
|     they detect.                 |     cloud platform) appropriate  |
|                                  |     information security         |
|                                  |     personnel.***                |
+----------------------------------+----------------------------------+
| -   Configure an appropriate     | -   ***Confirm that the          |
|     time zone for the audit      |     appropriate time zone has    |
|     records generated by your    |     been set.***                 |
|     solution components.         |                                  |
+----------------------------------+----------------------------------+
| -   Ensure that resources are    | -   Demonstrate that the         |
|     assigned to monitor          |     monitoring use cases for the |
|     cloud-based events.          |     cloud platform have been     |
|                                  |     implemented and have been    |
|                                  |     integrated with the overall  |
|                                  |     security monitoring          |
|                                  |     activities being performed   |
|                                  |     by the department. Evidence  |
|                                  |     could include monitoring run |
|                                  |     book/checklist, system       |
|                                  |     generated report.            |
+----------------------------------+----------------------------------+
| ***Additional Considerations***  |                                  |
+----------------------------------+----------------------------------+
| None                             |                                  |
+----------------------------------+----------------------------------+
| ***References***                 |                                  |
|                                  |                                  |
| 1.  , subsection 6.3.1           |                                  |
|                                  |                                  |
| 2.  CSE Top 10 \#1, 5, 8         |                                  |
|                                  |                                  |
| 3.  Refer to [GC Event Logging   |                                  |
|     Guidance](https://www        |                                  |
| .gcpedia.gc.ca/gcwiki/images/e/e |                                  |
| 3/GC_Event_Logging_Strategy.pdf) |                                  |
|                                  |                                  |
| 4.  Refer to [ITSP.50.104        |                                  |
|     Guidance on defence in depth |                                  |
|     for cloud-based              |                                  |
|     s                            |                                  |
| ervices,](https://cyber.gc.ca/en |                                  |
| /guidance/itsp50104-guidance-def |                                  |
| ence-depth-cloud-based-services) |                                  |
|     subsection 4.8               |                                  |
+----------------------------------+----------------------------------+
| **Related security controls:**   |                                  |
| AU‑12, SI-4, SI-4(7)             |                                  |
+----------------------------------+----------------------------------+

Guardrail \#12 -- Configuration of cloud marketplaces
-----------------------------------------------------

+----------------------------------+----------------------------------+
| ***Objective:*** Restrict        |                                  |
| Third-Party CSP Marketplace      |                                  |
| software to GC-approved          |                                  |
| products.                        |                                  |
+==================================+==================================+
| ***Applicable Service Models:    |                                  |
| IaaS, PaaS, SaaS***              |                                  |
+----------------------------------+----------------------------------+
| ***Mandatory Requirements***     | ***Validation***                 |
+----------------------------------+----------------------------------+
| -   Only GC approved cloud       | -   Confirm that third-party     |
|     marketplace products are to  |     marketplace restrictions     |
|     be consumed. Turning on the  |     have been implemented.       |
|     commercial marketplace is    |                                  |
|     prohibited.                  |                                  |
+----------------------------------+----------------------------------+
| ***Additional Considerations***  |                                  |
+----------------------------------+----------------------------------+
| -   ***Submit requests to add    |                                  |
|     third-party products to      |                                  |
|     marketplace to SSC Cloud     |                                  |
|     Broker.***                   |                                  |
+----------------------------------+----------------------------------+
| -   Ensure that software offered |                                  |
|     through the CSPs or CSP      |                                  |
|     marketplace undergo a        |                                  |
|     software assurance process   |                                  |
|     to ensure that only approved |                                  |
|     products are consumed.       |                                  |
+----------------------------------+----------------------------------+
| ***References***                 |                                  |
|                                  |                                  |
| 1.                               |                                  |
|   [SPIN 2017-01](https://www.can |                                  |
| ada.ca/en/treasury-board-secreta |                                  |
| riat/services/access-information |                                  |
| -privacy/security-identity-manag |                                  |
| ement/direction-secure-use-comme |                                  |
| rcial-cloud-services-spin.html), |                                  |
|     subsection 6.2.5             |                                  |
+----------------------------------+----------------------------------+
| **Related security controls:**   |                                  |
| CM‑5, CM‑8, SA‑12                |                                  |
+----------------------------------+----------------------------------+

Guardrail \#13 -- Plan for continuity 
-------------------------------------

+----------------------------------+----------------------------------+
| ***Objective:*** Ensure that     |                                  |
| there is a plan for continuity   |                                  |
| of access and service that       |                                  |
| accommodates both expected and   |                                  |
| unexpected events.               |                                  |
+==================================+==================================+
| ***Applicable Service Models:    |                                  |
| IaaS, PaaS, SaaS***              |                                  |
+----------------------------------+----------------------------------+
| ***Mandatory Requirements***     | ***Validation***                 |
+----------------------------------+----------------------------------+
| -   Document, implement, and     | -   ***Verify that a break glass |
|     test a break glass emergency |     emergency account management |
|     account management process.  |     procedure has been           |
|                                  |     developed.***                |
|                                  |                                  |
|                                  | -   ***Verify that alerting is   |
|                                  |     in place to report any use   |
|                                  |     of break glass accounts.***  |
|                                  |                                  |
|                                  | -   ***Verify that testing of    |
|                                  |     break glass account took     |
|                                  |     place, and that periodic     |
|                                  |     testing is included in break |
|                                  |     glass emergency account      |
|                                  |     management procedure.***     |
+----------------------------------+----------------------------------+
| -   Obtain signature from        | -   Confirm through attestation  |
|     Departmental Chief           |     that the Departmental Chief  |
|     Information Officer (CIO) in |     Information Officer (CIO) in |
|     collaboration with           |     collaboration with DOCS have |
|     designated official for      |     approved the break glass     |
|     cyber security (DOCS) to     |     emergency account management |
|     confirm acknowledgement and  |     procedure for the cloud      |
|     approval of the break glass  |     service.                     |
|     emergency account management |                                  |
|     procedures.                  |                                  |
+----------------------------------+----------------------------------+
| ***Additional Considerations***  |                                  |
+----------------------------------+----------------------------------+
| -   ***Develop a cloud backup    | -   ***Confirm through           |
|     strategy that takes into     |     attestation that the cloud   |
|     account where GC data is     |     backup strategy procedure is |
|     stored, replicated, or       |     developed and approved by    |
|     backed up by the cloud       |     the business owner.***       |
|     service, in consideration of |                                  |
|     the IT continuity plan for   | -   ***Verify if there are       |
|     the service/application.***  |     scripts that support the     |
|                                  |     ability to restore from code |
|                                  |     (e.g., infrastructure as     |
|                                  |     code).***                    |
+----------------------------------+----------------------------------+
| -   ***Ensure that cloud         | -   Provide a list of all        |
|     workloads are associated     |     software, including          |
|     with the applicable          |     versions, deployed on VMs    |
|     Application ID in the TBS    |     associated with the          |
|     Application Portfolio        |     application IDs from APM.    |
|     Management (APM) tool, in    |                                  |
|     support of the Standard on   |                                  |
|     At-Risk Technology.***       |                                  |
+----------------------------------+----------------------------------+
| -   ***Ensure departmental cyber | -   *Provide a list of all       |
|     security event management    |     software, including          |
|     plans include cloud          |     versions, deployed on VMs    |
|     services, in alignment with  |     associated with the          |
|     the GC Cyber Security Event  |     application IDs from APM.*   |
|     Management Plan.***          |                                  |
+----------------------------------+----------------------------------+
| ***References***                 |                                  |
|                                  |                                  |
| 1.                               |                                  |
|   [SPIN 2017-01](https://www.can |                                  |
| ada.ca/en/treasury-board-secreta |                                  |
| riat/services/access-information |                                  |
| -privacy/security-identity-manag |                                  |
| ement/direction-secure-use-comme |                                  |
| rcial-cloud-services-spin.html), |                                  |
|     [sub-section                 |                                  |
|     6.2.9](https://www.ca        |                                  |
| nada.ca/en/government/system/dig |                                  |
| ital-government/digital-governme |                                  |
| nt-innovations/cloud-services/di |                                  |
| rection-secure-use-commercial-cl |                                  |
| oud-services-spin.html#toc6-2-9) |                                  |
|                                  |                                  |
| 2.  Refer to the                 |                                  |
|                                  |                                  |
|    [template](https://gcconnex.g |                                  |
| c.ca/file/view/55010566/break-gl |                                  |
| ass-emergency-account-procedure- |                                  |
| departments-can-use-to-develop-t |                                  |
| heir-emergency-access-management |                                  |
| -controls-for-cloud?language=en) |                                  |
|     for a break glass emergency  |                                  |
|     account management           |                                  |
|     procedure.                   |                                  |
|                                  |                                  |
| 3.  Refer to the [Department     |                                  |
|     Cyber Security Event         |                                  |
|     Management Plan (CSEMP)      |                                  |
|     Template](https://www.g      |                                  |
| cpedia.gc.ca/gcwiki/images/6/66/ |                                  |
| Department_CSEMP_Template.docx). |                                  |
|                                  |                                  |
| 4.  [Directive on Service and    |                                  |
|     Digital-                     |                                  |
|     Can                          |                                  |
| ada.ca](https://www.tbs-sct.cana |                                  |
| da.ca/pol/doc-eng.aspx?id=32601) |                                  |
+----------------------------------+----------------------------------+
| **Related security controls:**   |                                  |
| AC-1, CP-1,CP-2,CP-9,CA-3        |                                  |
+----------------------------------+----------------------------------+
