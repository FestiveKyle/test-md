-   [Cloud Guardrails](#cloud-guardrails)
    -   [Guardrail #1 – Protect user accounts and identities
        ](#guardrail-1-protect-user-accounts-and-identities)
    -   [Guardrail #2 – Manage access](#guardrail-2-manage-access)
    -   [Guardrail #3 – Secure endpoints](#guardrail-3-secure-endpoints)
    -   [Guardrail #4 – Enterprise monitoring
        accounts](#guardrail-4-enterprise-monitoring-accounts)
    -   [Guardrail #5 – Data location](#guardrail-5-data-location)
    -   [Guardrail #6 – Protection of data-at-rest
        ](#guardrail-6-protection-of-data-at-rest)
    -   [Guardrail #7 – Protection of
        data-in-transit](#guardrail-7-protection-of-data-in-transit)
    -   [**Guardrail** #8 – Segment and
        separate](#guardrail-8-segment-and-separate)
    -   [Guardrail #9 – Network security
        services](#guardrail-9-network-security-services)
    -   [Guardrail #10 – Cyber defense
        services](#guardrail-10-cyber-defense-services)
    -   [Guardrail #11 – Logging and
        monitoring](#guardrail-11-logging-and-monitoring)
    -   [Guardrail #12 – Configuration of cloud
        marketplaces](#guardrail-12-configuration-of-cloud-marketplaces)
    -   [Guardrail #13 – Plan for continuity
        ](#guardrail-13-plan-for-continuity)

# Cloud Guardrails

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

<!-- -->

-   Additional considerations: Additional security controls that are
    > highly recommended and should be taken into consideration. While
    > these are not expected to be implemented within 30 business days,
    > they include best practices that should be considered as
    > departments progress with the establishment of their cloud-based
    > environments.

## Guardrail #1 – Protect user accounts and identities 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>Objective:</strong> Protect user accounts and
identities.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td colspan="2"><strong>Applicable Service Models:</strong> IaaS, PaaS,
SaaS</td>
</tr>
<tr class="even">
<td><strong>Mandatory Requirements</strong></td>
<td><strong>Validation</strong></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Implement strong multi-factor authentication (MFA) for all user
accounts. Use phishing resistant MFA where and when available.</p></li>
</ul>
<p><em>(Note: User accounts and identities include:</em></p>
<ol type="1">
<li><p><em>Root/Global administrator (as it is one that that has
enhanced/highest level of privileges over the control plane and
addresses all aspects of access control).</em></p></li>
<li><p><em>Other Administrative user accounts. Refer to Section 4 of the
“<a
href="https://www.tbs-sct.canada.ca/pol/doc-eng.aspx?id=32601">Directive
on Service and Digital- Canada.ca</a>, <a
href="https://www.tbs-sct.canada.ca/pol/doc-eng.aspx?id=32713">Appendix
G: Standard on Enterprise Information Technology Service Common
Configurations- Canada.ca</a> - <a
href="https://www.canada.ca/en/government/system/digital-government/policies-standards/enterprise-it-service-common-configurations/account.html">Account
Management Configuration Requirements - Canada.ca</a>”</em> <em>for the
definition of privileged accounts.</em></p></li>
<li><p><em>Regular user accounts)</em></p></li>
</ol></td>
<td><ul>
<li><p>Confirm that MFA is implemented as per GC guidance through
screenshots, compliance reports, or compliance check enabled through a
reporting tool for all user accounts.</p></li>
<li><p>Confirm that digital policies are in place to ensure that MFA
configurations are enforced.</p></li>
<li><p>Confirm and report the count of Root/Global administrator
registered (should have at least two and no more <mark>than
five</mark>).</p></li>
</ul></td>
</tr>
<tr class="even">
<td><ul>
<li><p>Configure alerting to ensure the prompt detection of a potential
compromise, in accordance with the GC Event Logging Guidance.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm if monitoring and auditing is implemented for all user
accounts.</p></li>
<li><p>Confirm alert notification to the authorized personnel is
implemented for flagging misuse, suspicious activities , for all user
accounts.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Use separate dedicated accounts for highly privileged roles (e.g.
domain admins, global admins, root, and any domain admin equivalent
access) when administering cloud services to minimize the blast
radius.</p></li>
</ul></td>
<td><ul>
<li><p>Provide evidence that dedicated user accounts are used for
administration (e.g., privileged access).</p></li>
</ul></td>
</tr>
<tr class="even">
<td colspan="2"><strong>Additional Considerations</strong></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>None</strong></td>
</tr>
<tr class="even">
<td colspan="2"><p><strong>References</strong></p>
<ol type="1">
<li><p><a
href="https://www.canada.ca/en/treasury-board-secretariat/services/access-information-privacy/security-identity-management/direction-secure-use-commercial-cloud-services-spin.html"><span>SPIN 2017-01</span></a>,
subsection 6.2.3</p></li>
<li><p>CSE Top 10 #3</p></li>
<li><p>Refer to the <a
href="https://intranet.canada.ca/wg-tg/rtua-rafu-eng.asp">Recommendations
for Two-Factor User Authentication Within the Government of Canada
Enterprise Domain</a></p></li>
<li><p>Refer to the <a
href="https://www.gcpedia.gc.ca/gcwiki/images/9/9e/GC_MFA_Strategy.pdf">GC
Multi-Factor Authentication (MFA) Strategy Paper</a></p></li>
<li><p>Refer to the <a
href="https://www.tbs-sct.canada.ca/pol/doc-eng.aspx?id=32601">Directive
on Service and Digital</a>, <a
href="https://www.tbs-sct.canada.ca/pol/doc-eng.aspx?id=32713">Appendix
G: Standard on Enterprise Information Technology Service Common
Configurations</a> - <a
href="https://www.canada.ca/en/government/system/digital-government/policies-standards/enterprise-it-service-common-configurations/account.html">Account
Management Configuration Requirements</a></p></li>
<li><p>Refer to the <a
href="https://www.gcpedia.gc.ca/gcwiki/images/e/e3/GC_Event_Logging_Strategy.pdf">GC
Event Logging Guidance</a></p></li>
<li><p>Refer to <a
href="https://cyber.gc.ca/en/guidance/itsp50104-guidance-defence-depth-cloud-based-services">ITSP.50.104
Guidance on defence in depth for cloud-based services,</a> subsection
4.6</p></li>
<li><p><a
href="https://www.cyber.gc.ca/en/guidance/user-authentication-guidance-information-technology-systems-itsp30031-v3">User
authentication guidance for information technology systems (ITSP.30.031
v3)</a></p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="2"><p><strong>Related security controls:</strong> AC-2,
AC-2(11), AC-3, AC-5, AC-6, AC- 6(5), AC- 6(10), AC-19, AC – 20 (3),
IA-2, IA-2(1)</p>
<p>IA - 2(2), IA-2(3), IA – 2(11), IA-5(8), SI-4, SI-4(5), SA-4(12),
CM-5.</p></td>
</tr>
</tbody>
</table>

## Guardrail #2 – Manage access

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>Objective:</strong> Establish access control
policies and procedures for management of all accounts.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td colspan="2"><strong>Applicable Service Models:</strong> IaaS, PaaS,
SaaS</td>
</tr>
<tr class="even">
<td><strong>Mandatory Requirements</strong></td>
<td><strong>Validation</strong></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Implement a mechanism for enforcing access authorizations for all
user accounts, based on criteria listed in Directive on Service and
Digital Appendix G – Account Management Configuration Requirements –
Section 3.</p></li>
</ul></td>
<td><ul>
<li><p>Demonstrate access configurations and policies are implemented
for different classes of users (non-privileged, and privileged
users).</p></li>
<li><p>Confirm that the access authorization mechanisms have been
implemented for the following:</p></li>
</ul>
<ol type="1">
<li><p>To uniquely identify and authenticate users to the cloud
service;</p></li>
<li><p>Validating that the least privilege role is assigned;</p></li>
<li><p>Validating that Role Based Access is implemented;</p></li>
<li><p>Terminating of role assignment upon job change or
termination;</p></li>
<li><p>Performing periodic reviews of role assignment (minimum
yearly);</p></li>
<li><p>Disabling default and dormant accounts;</p></li>
<li><p>Avoiding use of user generic accounts.</p></li>
</ol>
<ul>
<li><p>Verify that a review of Root/Global administrator accounts role
assignment is performed at a minimum every 12 months.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><ul>
<li><p>Leverage role-based access that are configured with least
privileges. This can include built-in roles or custom roles that have
been established with only the minimum number of privileges required to
perform the job function.</p></li>
</ul></td>
<td><ul>
<li><p>Demonstrate that cloud platform built-in roles are used with
least privileges. Custom roles can be used but rationale should be
documented and approved.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Change default passwords in accordance with the GC password
guidance.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm that the default passwords have been changed for all the
built-in accounts for the cloud-service.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><ul>
<li><p>Configure the default password policy in accordance with <a
href="https://www.canada.ca/en/government/system/digital-government/online-security-privacy/password-guidance.html">GC
Password Guidance</a>.</p></li>
</ul></td>
<td><ul>
<li><p>Demonstrate that password policy for the cloud platform has been
configured as per the GC Password Guidance:</p>
<ol type="1">
<li><p>Require longer passwords – At least 12 characters in length
without a maximum length limit;</p></li>
<li><p>Counter online guessing or brute forcing of passwords using
throttling, account lockout policies, monitoring, and multi-factor
authentication;</p></li>
<li><p>Protect against offline attacks using effecting hashing, salting,
and keyed hashing.</p></li>
</ol></li>
</ul></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Implement password protection mechanisms to protect against
password brute force attacks.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm that mechanisms, such as throttling, account lock out
policies, monitoring and risk based authentication, to protect against
password bruteforce attacks have been implemented </p></li>
</ul></td>
</tr>
<tr class="even">
<td><ul>
<li><p>Establish a guest user access policy and procedures that
minimizes the number of guest users and manages their lifecycle where
accounts are deprovisioned when access is no longer needed.</p></li>
</ul>
<blockquote>
<p>(Note: A guest is someone who isn't an employee, student, or member
of your organization. They don't have an existing account with the
organization’s cloud tenant).</p>
</blockquote></td>
<td><ul>
<li><p>Confirm only the required guest user accounts are enabled (The
required guest user accounts are as per the business requirements of the
service)</p></li>
<li><p>Provide list of non-organizational users with elevated
privileges.</p></li>
<li><p>Verify that periodic guest access reviews are performed
periodically.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Additional Considerations</strong></td>
</tr>
<tr class="even">
<td><ul>
<li><p>Document a process for managing accounts, access privileges, and
access credentials for organizational users, non-organizational users
(if required), based on criteria listed in Directive on Service and
Digital Appendix G – Account Management Configuration Requirements –
Section 3. This process should be approved by Chief Security Officer
(CSO) (or delegate) and designated official for cyber security.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm that the Access Control procedure for management of
administrative accounts have been documented for the cloud service. The
procedure should include provision for any guest accounts, custom
accounts, and must reference to the Emergency Break Glass
procedure.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Enforce just-in-time access for privileged user accounts to
provide time-based and approval-based role activation to mitigate the
risks of excessive, unnecessary, or misused access permissions.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm that just-in-time access for all privileged user accounts
to provide time-based and approval-based role activation.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><ul>
<li><p>Enforce attribute-based access control (ABAC) to restrict access
based on combination of authentication factors (MFA), , GC issued and
managed devices, device compliance, sign-in and user risks, and
location.</p></li>
</ul></td>
<td><ul>
<li><p>Provide evidence that attribute-based access control (ABAC)
mechanisms are in place to restrict access based on attributes/signals
such as authentication factors (MFA), GC issued and managed devices,
device compliance, sign-in and user risks, and location.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Leverage tools such as privilege access management systems to
enforce access control to privilege functions by configuring roles that
requires approval for activation and choose one or multiple users or
groups as delegated approvers.</p></li>
</ul></td>
<td><ul>
<li><p>Provide evidence that all privileged user accounts role
activation requires approval, and that privilege elevation is time-bound
(temporary activation).</p></li>
</ul></td>
</tr>
<tr class="even">
<td><ul>
<li></li>
</ul></td>
<td><ul>
<li></li>
</ul></td>
</tr>
<tr class="odd">
<td colspan="2"><p><strong>References</strong></p>
<ol type="1">
<li><p><a
href="https://www.canada.ca/en/treasury-board-secretariat/services/access-information-privacy/security-identity-management/direction-secure-use-commercial-cloud-services-spin.html"><span>SPIN 2017-01</span></a>,
subsection 6.2.3</p></li>
<li><p>CSE Top 10 #3</p></li>
<li><p>Refer to <a
href="https://www.cyber.gc.ca/en/guidance/user-authentication-guidance-information-technology-systems-itsp30031-v3">User
authentication guidance for information technology systems (ITSP.30.031
v3)</a></p></li>
<li><p>Refer to the <a
href="https://intranet.canada.ca/wg-tg/cagc-angc-eng.asp">Guidance on
Cloud Authentication for the Government of Canada</a></p></li>
<li><p>Refer to the <a
href="https://intranet.canada.ca/wg-tg/rtua-rafu-eng.asp">Recommendations
for Two-Factor User Authentication Within the Government of Canada
Enterprise Domain</a></p></li>
<li><p>Refer to the <a
href="https://www.tbs-sct.canada.ca/pol/doc-eng.aspx?id=32601">Directive
on Service and Digital</a>, <a
href="https://www.tbs-sct.canada.ca/pol/doc-eng.aspx?id=32713">Appendix
G: Standard on Enterprise Information Technology Service Common
Configurations</a> - <a
href="https://www.canada.ca/en/government/system/digital-government/policies-standards/enterprise-it-service-common-configurations/account.html">Account
Management Configuration Requirements</a></p></li>
<li><p>Refer to <a
href="https://cyber.gc.ca/en/guidance/itsp50104-guidance-defence-depth-cloud-based-services">ITSP.50.104
Guidance on defence in depth for cloud-based services,</a> subsection
4.6</p></li>
<li><p><a
href="https://www.canada.ca/en/government/system/digital-government/online-security-privacy/password-guidance.html">GC
Password Guidance</a></p></li>
</ol></td>
</tr>
<tr class="even">
<td colspan="2"><strong>Related security controls:</strong> AC‑2,
AC‑2(1), AC‑2(7) AC‑3, AC‑3(7), AC‑3, AC‑4 AC‑5, AC‑6, AC‑6(5), IA‑2,
IA‑2(1), IA‑2(8), IA‑2(11), IA‑4, IA‑5, IA‑5(1), IA‑5(6)</td>
</tr>
</tbody>
</table>

## Guardrail #3 – Secure endpoints

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>Objective:</strong> Implement increased levels
of protection for management interfaces.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td colspan="2"><strong>Applicable Service Models:</strong> IaaS, PaaS,
SaaS</td>
</tr>
<tr class="even">
<td><strong>Mandatory Requirements</strong></td>
<td><strong>Validation</strong></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Implement access restrictions to ensure the use GC issued and
managed devices that are patched and managed, in accordance with <a
href="https://www.canada.ca/en/government/system/digital-government/policies-standards/enterprise-it-service-common-configurations/endpoint.html">GC
Endpoint Management Configuration Requirements</a>.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm that administrative access to cloud environments is from
approved and trusted locations and GC issued and managed devices that
enforce the GC endpoint management configuration requirements.</p></li>
</ul>
<ul>
<li><p>Demonstrate access configurations and policies are implemented
for devices.</p></li>
</ul></td>
</tr>
<tr class="even">
<td colspan="2"><strong>Additional Considerations</strong></td>
</tr>
<tr class="odd">
<td><ul>
<li><p><mark> All administrative tasks should be undertaken on dedicated
administrative workstations.</mark></p></li>
</ul>
<blockquote>
<p><mark>(Note: A dedicated administrative workstation is a secured
physical (thick or thin) client workstation used to perform specific and
sensitive administrative tasks or tasks requiring privileged access.
This device must have no Internet access and services such as email and
web browsing must be disabled and prohibited)</mark></p>
</blockquote></td>
<td><ul>
<li><p>Confirm if dedicated <mark>administrative workstations</mark> are
utilized to conduct all administrative activities</p></li>
</ul></td>
</tr>
<tr class="even">
<td colspan="2"><p><strong>References</strong></p>
<ol type="1">
<li><p><a
href="https://www.canada.ca/en/treasury-board-secretariat/services/access-information-privacy/security-identity-management/direction-secure-use-commercial-cloud-services-spin.html"><span>SPIN 2017-01</span></a>,
subsection 6.2.3</p></li>
<li><p>CSE Top 10 #2</p></li>
<li><p>Refer to the <a
href="https://intranet.canada.ca/wg-tg/rtua-rafu-eng.asp">Recommendations
for Two-Factor User Authentication Within the Government of Canada
Enterprise Domain</a></p></li>
<li><p>Refer to the <a
href="https://www.tbs-sct.canada.ca/pol/doc-eng.aspx?id=32601">Directive
on Service and Digital</a>, <a
href="https://www.tbs-sct.canada.ca/pol/doc-eng.aspx?id=32713">Appendix
G: Standard on Enterprise Information Technology Service Common
Configurations</a> - <a
href="https://www.canada.ca/en/government/system/digital-government/policies-standards/enterprise-it-service-common-configurations/endpoint.html">Endpoint
Management Configuration Requirements</a></p></li>
<li><p>Refer to <a
href="https://cyber.gc.ca/en/guidance/itsp50104-guidance-defence-depth-cloud-based-services">ITSP.50.104
Guidance on defence in depth for cloud-based services,</a> subsection
4.9.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Related security controls</strong>: AC3,
AC-3(7), AC-4, AC5, AC6, AC6(5), AC6(10), AC19, AC20(3), IA2,
IA2(1),IA2(11), IA4, IA5, IA5(1), SI-4, AU-6, AU-12</td>
</tr>
</tbody>
</table>

## Guardrail #4 – Enterprise monitoring accounts

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>Objective:</strong> Create role-based account to
enable enterprise monitoring and visibility</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td colspan="2"><strong>Applicable Service Models:</strong> IaaS, PaaS,
SaaS</td>
</tr>
<tr class="even">
<td><strong>Mandatory Requirements</strong></td>
<td><strong>Validation</strong></td>
</tr>
<tr class="odd">
<td><ul>
<li></li>
</ul>
<p>Create role-based account to enable enterprise monitoring and
visibility for cloud environments that are procured via the GC Cloud
Broker or are included in scope of centralized guardrails
validation.</p></td>
<td><ul>
<li><p>Verify that roles required to enable GC visibility to have been
provisioned/assigned.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><ul>
<li><p>Review access privileges periodically and remove access when it
is no longer required.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm alert notification to the authorized personnel is
implemented flagging misuse, suspicious sign-in attempts, or when
changes are made to the privileged and non-privileged accounts.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Additional Considerations</strong></td>
</tr>
<tr class="even">
<td colspan="2"><strong>None</strong></td>
</tr>
<tr class="odd">
<td colspan="2"><p><strong>References</strong></p>
<ol type="1">
<li><p><a
href="https://www.canada.ca/en/treasury-board-secretariat/services/access-information-privacy/security-identity-management/direction-secure-use-commercial-cloud-services-spin.html"><span>SPIN 2017-01</span></a>,
subsection 6.2.3</p></li>
<li><p>CSE Top 10 #2</p></li>
</ol></td>
</tr>
<tr class="even">
<td colspan="2"><strong>Related security controls</strong>: AC-3(7),
AC-6(5), IA-2(1)</td>
</tr>
</tbody>
</table>

## Guardrail #5 – Data location

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>Objective:</strong> Establish policies to
restrict GC sensitive workloads to approved geographic locations</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td colspan="2"><strong>Applicable Service Models:</strong> IaaS, PaaS,
SaaS</td>
</tr>
<tr class="even">
<td><strong>Mandatory Requirements</strong></td>
<td><strong>Validation</strong></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>As per Section 4.4.3.14 of the Directive on Service and Digital,
“Ensuring computing facilities located within the geographic boundaries
of Canada or within the premises of a Government of Canada department
located abroad, such as a diplomatic or consular mission, be identified
and evaluated as a principal delivery option for all sensitive
electronic information and data under government control that has been
categorized as Protected B, Protected C or is Classified.”</p></li>
</ul></td>
<td><ul>
<li><p>Demonstrate that service location is within Canada (For all PB
cloud-services) where configurable , in accordance with the applicable
cloud usage profiles.</p></li>
<li></li>
</ul></td>
</tr>
<tr class="even">
<td colspan="2"><strong>Additional Considerations</strong></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>None</strong></td>
</tr>
<tr class="even">
<td colspan="2"><p><strong>References</strong></p>
<ol type="1">
<li><p><a
href="https://www.canada.ca/en/treasury-board-secretariat/services/access-information-privacy/security-identity-management/direction-secure-use-commercial-cloud-services-spin.html"><span>SPIN 2017-01</span></a>,
subsection 6.2.3</p></li>
<li><p>Refer to <a
href="https://www.tbs-sct.canada.ca/pol/doc-eng.aspx?id=32601">Directive
on Service and Digita</a>l, subsection 4.4.3.14</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Related security controls</strong>: SA-9(5)</td>
</tr>
</tbody>
</table>

## Guardrail #6 – Protection of data-at-rest 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>Objective:</strong> Protect data at rest by
default (e.g., storage) for cloud-based workloads</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td colspan="2"><strong>Applicable Service Models:</strong> IaaS, PaaS,
SaaS</td>
</tr>
<tr class="even">
<td><strong>Mandatory Requirements</strong></td>
<td><strong>Validation</strong></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Implement an encryption mechanism to protect the confidentiality
and integrity of data when data are at rest in your solution's
storage.</p></li>
</ul></td>
<td><ul>
<li><p>For IaaS and PaaS, confirm that storage service encryption is
enabled for data at rest (if required based on the security risk
assessment).</p></li>
<li><p>For SaaS, confirm that the CSP has implemented encryption to
protect customer data.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><ul>
<li><p>Use CSE-approved cryptographic algorithms and protocols, in
accordance with ITSP.40.111 and ITSP.40.062.</p></li>
</ul></td>
<td><ul>
<li><p>Cryptographic algorithms and protocols configurable by the
consumer are leveraged in accordance with ITSP 40.111 and
40.062.</p></li>
<li><p>For SaaS, confirm that the CSP has implemented algorithms that
align with ITSP 40.111 and 40.062.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Additional Considerations</strong></td>
</tr>
<tr class="even">
<td><ul>
<li><p>Seek guidance from privacy and access to information officials
within institutions before storing personal information in cloud-based
environments.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm that privacy is included as part of the Departmental SDLC
process.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Leverage an appropriate key management system for the
cryptographic protection used in cloud-based services, in accordance
with GC Considerations for the Use of Cryptography in Commercial Cloud
Services and CCCS guidance on key management <mark>at Guidance on cloud
<a
href="https://www.cyber.gc.ca/en/guidance/guidance-cloud-service-cryptography-itsp50106">service</a>
cryptography (ITSP.50.106)</mark>.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm that a key management strategy has been adopted for the
cloud tenant.</p></li>
</ul></td>
</tr>
<tr class="even">
<td colspan="2"><p><strong>References</strong></p>
<ol type="1">
<li><p><a
href="https://www.canada.ca/en/treasury-board-secretariat/services/access-information-privacy/security-identity-management/direction-secure-use-commercial-cloud-services-spin.html"><span>SPIN 2017-01</span></a>,
subsection 6.2.4</p></li>
<li><p>Refer to the cryptography guidance in <a
href="https://cyber.gc.ca/en/guidance/cryptographic-algorithms-unclassified-protected-and-protected-b-information-itsp40111">ITSP.40.111</a>
and <a
href="https://www.cyber.gc.ca/en/guidance/guidance-securely-configuring-network-protocols-itsp40062">ITSP.40.062</a>.</p></li>
<li><p>Refer to the guidance in Guidance on cloud <a
href="https://www.cyber.gc.ca/en/guidance/guidance-cloud-service-cryptography-itsp50106">service</a>
cryptography (ITSP.50.106)</p></li>
<li><p>Refer to <a
href="https://cyber.gc.ca/en/guidance/itsp50104-guidance-defence-depth-cloud-based-services">ITSP.50.104
Guidance on defence in depth for cloud-based services,</a> subsection
4.5.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Related security controls:</strong> IA-7, SC-12,
SC-13, SC-28, SC-28(1)</td>
</tr>
</tbody>
</table>

## Guardrail #7 – Protection of data-in-transit

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>Objective:</strong> Protect data transiting
networks through the use of appropriate encryption and network
safeguards</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td colspan="2"><strong>Applicable Service Models:</strong> IaaS, PaaS,
SaaS</td>
</tr>
<tr class="even">
<td><strong>Mandatory Requirements</strong></td>
<td><strong>Validation</strong></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Encrypt data in transit by default (e.g., TLS v1.2, etc.) to
protect the confidentiality and integrity of data, including for all
publicly accessible sites and external communications as per the GC
Website and Services Configuration Requirements, and wherever possible
for internal zone communication.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm that TLS v1.2 or above encryption is implemented for all
cloud services (via HTTPS, TLS or other mechanism).</p></li>
</ul>
<p><em>(Note: While this is often the default, cloud platforms and cloud
services often have configuration options to select the permitted TLS
version.)</em></p></td>
</tr>
<tr class="even">
<td><ul>
<li><p>Use CSE-approved cryptographic algorithms and protocols, in
accordance with ITSP.40.111 and ITSP.40.062.</p></li>
</ul></td>
<td><ul>
<li><p>Cryptographic algorithms and protocols configurable by the
consumer are leveraged in accordance with ITSP 40.111 and
40.062.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Leverage non-person entity certificates from certificate
authorities that align with the Recommendations for TLS Server
Certificates.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm that NPE certificates are issued from certificate
authorities that align with GC recommendations for TLS server
certificates.</p></li>
</ul></td>
</tr>
<tr class="even">
<td colspan="2"><strong>Additional Considerations</strong></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>None</strong></td>
</tr>
<tr class="even">
<td colspan="2"><p><strong>References</strong></p>
<ol type="1">
<li><p><a
href="https://www.canada.ca/en/treasury-board-secretariat/services/access-information-privacy/security-identity-management/direction-secure-use-commercial-cloud-services-spin.html"><span>SPIN 2017-01</span></a>,
subsection 6.2.4</p></li>
<li><p>Refer to the <a
href="https://www.tbs-sct.canada.ca/pol/doc-eng.aspx?id=32601">Directive
on Service and Digital</a>, <a
href="https://www.tbs-sct.canada.ca/pol/doc-eng.aspx?id=32713">Appendix
G: Standard on Enterprise Information Technology Service Common
Configurations</a> – <a
href="https://www.canada.ca/en/government/system/digital-government/policies-standards/enterprise-it-service-common-configurations/web-sites.html">Web
Sites and Services Management Configuration Requirements</a></p></li>
<li><p>Refer to the cryptography guidance in <a
href="https://cyber.gc.ca/en/guidance/cryptographic-algorithms-unclassified-protected-and-protected-b-information-itsp40111">ITSP.40.111</a>
and <a
href="https://www.cyber.gc.ca/en/guidance/guidance-securely-configuring-network-protocols-itsp40062">ITSP.40.062</a></p></li>
<li><p>Refer to the network security zoning guidance in <a
href="https://cyber.gc.ca/en/guidance/baseline-security-requirements-network-security-zones-government-canada-itsg-22">ITSG-22</a>
and <a
href="https://cyber.gc.ca/en/guidance/network-security-zoning-design-considerations-placement-services-within-zones-itsg-38">ITSG-38</a></p></li>
<li><p>Refer to the guidance in <mark>Guidance on cloud</mark> <a
href="https://www.cyber.gc.ca/en/guidance/guidance-cloud-service-cryptography-itsp50106">service</a>
<mark>cryptography (ITSP.50.10</mark>6)</p></li>
<li><p><a
href="https://wiki.gccollab.ca/images/9/92/Recommendations_for_TLS_Server_Certificates_-_14_May_2021.pdf">Government
of Canada Recommendations for TLS Server Certificates for GC Public
Facing Web Services</a></p></li>
<li><p>Refer to <a
href="https://cyber.gc.ca/en/guidance/itsp50104-guidance-defence-depth-cloud-based-services">ITSP.50.104
Guidance on defence in depth for cloud-based services</a>, subsection
4.5</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Related security controls:</strong> IA-7,SC-12,
SC-13, SC-28, SC-28(1)</td>
</tr>
</tbody>
</table>

## **Guardrail** #8 – Segment and separate

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>Objective:</strong> Segment and separate
information based on sensitivity of information</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>Applicable Service Models:</strong> IaaS,
PaaS</p>
<p><em>(Note: The following guardrail is not applicable for SaaS model.
Management and security of the network is a Cloud Service Provider
responsibility and is included as part of the SaaS offering. Please
refer to <a
href="https://www.cyber.gc.ca/en/guidance/itsp50104-guidance-defence-depth-cloud-based-services">ITSP.50.104
Guidance on defence in depth for cloud-based services</a> Section 4.3 to
understand key considerations for cloud network
segmentation)</em></p></td>
</tr>
<tr class="even">
<td><strong>Mandatory Requirements</strong></td>
<td><strong>Validation</strong></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Isolate and secure cloud workloads based on the sensitivity of
the data.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm that department has a target network architecture high
level design and / or diagram with appropriate segmentation between
network security zones in alignment with CSE’s <mark>ITSP.50.104</mark>,
ITSG-22 and ITSG-38.</p></li>
</ul>
<ul>
<li><p>Confirm that the department has documented a deployment guide of
the cloud platform and associated services. (The document is to capture
landing zone if applicable)</p></li>
<li><p>Confirm that CSP segmentation features are leveraged to provide
segmentation of Management, Prod, UAT, DEV, and test. (For example, use
of subscription, instances, or other cloud provider construct).</p></li>
</ul></td>
</tr>
<tr class="even">
<td colspan="2"><strong>Additional Considerations</strong></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Develop a target network security design that considers
segmentation via network security zones, in alignment with
<mark>ITSP.50.104</mark>, ITSG-22 and ITSG-38.</p></li>
</ul></td>
<td><ul>
<li><p>Leverage landing zones that include pre-defined, secured,
multi-account support to allow different workloads and teams to be
onboarded in an automated manner.</p></li>
</ul></td>
</tr>
<tr class="even">
<td colspan="2"><p><strong>References</strong></p>
<ol type="1">
<li><p><a
href="https://www.canada.ca/en/treasury-board-secretariat/services/access-information-privacy/security-identity-management/direction-secure-use-commercial-cloud-services-spin.html"><span>SPIN 2017-01</span></a>,
subsection 6.2.4</p></li>
<li><p>CSE Top 10 #5</p></li>
<li><p>Refer to the network security zoning guidance in <a
href="https://cyber.gc.ca/en/guidance/baseline-security-requirements-network-security-zones-government-canada-itsg-22">ITSG-22</a>
and <a
href="https://cyber.gc.ca/en/guidance/network-security-zoning-design-considerations-placement-services-within-zones-itsg-38">ITSG-38</a></p></li>
<li><p>Refer to <a
href="https://cyber.gc.ca/en/guidance/itsp50104-guidance-defence-depth-cloud-based-services">ITSP.50.104
Guidance on defence in depth for cloud-based services</a>, subsections
4.3, 4.5</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Related security controls:</strong> AC‑4,
SC‑7</td>
</tr>
</tbody>
</table>

## Guardrail #9 – Network security services

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>Objective:</strong> Establish external and
internal network perimeters and monitor network traffic.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td colspan="2"><strong>Applicable Service Models:</strong> IaaS, PaaS,
SaaS</td>
</tr>
<tr class="even">
<td><strong>Mandatory Requirements</strong></td>
<td><strong>Validation</strong></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Ensure that egress/ingress points to and from GC cloud-based
environments are managed and monitored.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm policy for limiting number of public IPs.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><ul>
<li><p>Implement network boundary protection mechanisms for all external
facing interfaces that enforce a deny-all or allow-by-exception
policy.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm policy for network boundary protection.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Perimeter security services such as boundary protection,
intrusion prevention services, proxy services, TLS traffic inspection,
etc. must be enabled based on risk profile, in alignment with GC Secure
Connectivity Requirements and <mark>CSE guidance</mark>.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm policy for limiting to authorized source IP addresses
(e.g., GC IP addresses).</p></li>
</ul></td>
</tr>
<tr class="even">
<td><ul>
<li><p>Ensure that access to cloud storage services is protected and
restricted to authorized security zones/network, users, and
services.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm that storage accounts are not exposed to the
public.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Additional Considerations</strong></td>
</tr>
<tr class="even">
<td><ul>
<li><p>Use centrally provisioned network security services where
available.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm if the department is intending to establish dedicated and
secure connections to on-premise resources.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td colspan="2"><p><strong>References</strong></p>
<ol type="1">
<li><p><a
href="https://www.canada.ca/en/treasury-board-secretariat/services/access-information-privacy/security-identity-management/direction-secure-use-commercial-cloud-services-spin.html"><span>SPIN 2017-01</span></a>,
subsection 6.2.4</p></li>
<li><p>CSE Top 10 #1</p></li>
<li><p>Refer to the network security zoning guidance in <a
href="https://cyber.gc.ca/en/guidance/baseline-security-requirements-network-security-zones-government-canada-itsg-22">ITSG-22</a>
and <a
href="https://cyber.gc.ca/en/guidance/network-security-zoning-design-considerations-placement-services-within-zones-itsg-38">ITSG-38</a></p></li>
<li><p>Refer to <a
href="https://cyber.gc.ca/en/guidance/itsp50104-guidance-defence-depth-cloud-based-services">ITSP.50.104
Guidance on defence in depth for cloud-based services</a>, subsection
4.3</p></li>
</ol></td>
</tr>
<tr class="even">
<td colspan="2"><strong>Related security controls:</strong> AC-3, AC‑4,
SC‑7, SC‑7(5), SI-4, SI-4(18)</td>
</tr>
</tbody>
</table>

## Guardrail #10 – Cyber defense services

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>Objective:</strong> Establish MOU for defensive
services and threat monitoring protection services.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td colspan="2"><strong>Applicable Service Models:</strong> IaaS, PaaS,
SaaS</td>
</tr>
<tr class="even">
<td><strong>Mandatory Requirements</strong></td>
<td><strong>Validation</strong></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Sign an MOU with Canadian Centre for Cyber Security (CCCS).
<em>(<a
href="mailto:CDOServiceDeployments@cyber.gc.ca">CDOServiceDeployments@cyber.gc.ca</a>.)</em></p></li>
</ul></td>
<td><ul>
<li><p>Confirmation from CCCS that the MOU has been signed by the
Department.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><ul>
<li><p>Implement defensive services including HBS, CBS, and NBS in
accordance with CCCS onboarding guidance where available.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm that the sensors or other cyber defense services by CCCS
are implemented where available.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Additional Considerations</strong></td>
</tr>
<tr class="even">
<td colspan="2"><strong>None</strong></td>
</tr>
<tr class="odd">
<td colspan="2"><p><strong>References</strong></p>
<ol type="1">
<li><p><a
href="https://www.canada.ca/en/treasury-board-secretariat/services/access-information-privacy/security-identity-management/direction-secure-use-commercial-cloud-services-spin.html">SPIN 2017-01</a>,
subsection 6.3</p></li>
</ol></td>
</tr>
<tr class="even">
<td colspan="2"><strong>Related security controls:</strong> SI‑4</td>
</tr>
</tbody>
</table>

## Guardrail #11 – Logging and monitoring

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>Objective:</strong> Enable logging for the cloud
environment and for cloud-based workloads.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td colspan="2"><strong>Applicable Service Models:</strong> IaaS, PaaS,
SaaS</td>
</tr>
<tr class="even">
<td><strong>Mandatory Requirements</strong></td>
<td><strong>Validation</strong></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Implement adequate level of logging and reporting, including a
security audit log function in all information systems.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm policy for event logging is implemented.</p></li>
<li><p>This includes logs for the following:</p>
<ol type="1">
<li><p>Sign-in logs (interactive and non-interactive sign-ins, API
sign-ins)</p></li>
<li><p>Access privilege and group changes (including group membership
and group privilege assignment)</p></li>
<li><p>Changes in configuration of cloud platform</p></li>
<li><p>Cloud resource provisioning activities.</p></li>
</ol></li>
</ul></td>
</tr>
<tr class="even">
<td><ul>
<li><p>Configure events within the solution to support security
monitoring, in accordance with GC Event Logging Guidance.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm if monitoring and auditing is implemented for all
users.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Ensure that the appropriate contact information is configured so
that the CSP can notify the GC organization of incidents they
detect.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm that the security contact record within the account
should be completed with details of at least two (if multiple permitted
by cloud platform) appropriate information security personnel.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><ul>
<li><p>Configure an appropriate time zone for the audit records
generated by your solution components.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm that the appropriate time zone has been set.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Ensure that resources are assigned to monitor cloud-based
events.</p></li>
</ul></td>
<td><ul>
<li><p>Demonstrate that the monitoring use cases for the cloud platform
have been implemented and have been integrated with the overall security
monitoring activities being performed by the department. Evidence could
include monitoring run book/checklist, system generated report.</p></li>
</ul></td>
</tr>
<tr class="even">
<td colspan="2"><strong>Additional Considerations</strong></td>
</tr>
<tr class="odd">
<td colspan="2">None</td>
</tr>
<tr class="even">
<td colspan="2"><p><strong>References</strong></p>
<ol type="1">
<li><p><a
href="https://www.canada.ca/en/treasury-board-secretariat/services/access-information-privacy/security-identity-management/direction-secure-use-commercial-cloud-services-spin.html"><span>SPIN 2017-01</span></a>,
subsection 6.3.1</p></li>
<li><p>CSE Top 10 #1, 5, 8</p></li>
<li><p>Refer to <a
href="https://www.gcpedia.gc.ca/gcwiki/images/e/e3/GC_Event_Logging_Strategy.pdf">GC
Event Logging Guidance</a></p></li>
<li><p>Refer to <a
href="https://cyber.gc.ca/en/guidance/itsp50104-guidance-defence-depth-cloud-based-services">ITSP.50.104
Guidance on defence in depth for cloud-based services,</a> subsection
4.8</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Related security controls:</strong> AU‑12, SI-4,
SI-4(7)</td>
</tr>
</tbody>
</table>

## Guardrail #12 – Configuration of cloud marketplaces

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>Objective:</strong> Restrict Third-Party CSP
Marketplace software to GC-approved products.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td colspan="2"><strong>Applicable Service Models:</strong> IaaS, PaaS,
SaaS</td>
</tr>
<tr class="even">
<td><strong>Mandatory Requirements</strong></td>
<td><strong>Validation</strong></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Only GC approved cloud marketplace products are to be consumed.
Turning on the commercial marketplace is prohibited.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm that third-party marketplace restrictions have been
implemented.</p></li>
</ul></td>
</tr>
<tr class="even">
<td colspan="2"><strong>Additional Considerations</strong></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Submit requests to add third-party products to marketplace to SSC
Cloud Broker.</p></li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td><ul>
<li><p>Ensure that software offered through the CSPs or CSP marketplace
undergo a software assurance process to ensure that only approved
products are consumed.</p></li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td colspan="2"><p><strong>References</strong></p>
<ol type="1">
<li><p><a
href="https://www.canada.ca/en/treasury-board-secretariat/services/access-information-privacy/security-identity-management/direction-secure-use-commercial-cloud-services-spin.html">SPIN 2017-01</a>,
subsection 6.2.5</p></li>
</ol></td>
</tr>
<tr class="even">
<td colspan="2"><strong>Related security controls:</strong> CM‑5, CM‑8,
SA‑12</td>
</tr>
</tbody>
</table>

## Guardrail #13 – Plan for continuity 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>Objective:</strong> Ensure that there is a plan
for continuity of access and service that accommodates both expected and
unexpected events.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td colspan="2"><strong>Applicable Service Models:</strong> IaaS, PaaS,
SaaS</td>
</tr>
<tr class="even">
<td><strong>Mandatory Requirements</strong></td>
<td><strong>Validation</strong></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Document, implement, and test a break glass emergency account
management process.</p></li>
</ul></td>
<td><ul>
<li><p>Verify that a break glass emergency account management procedure
has been developed.</p></li>
<li><p>Verify that alerting is in place to report any use of break glass
accounts.</p></li>
<li><p>Verify that testing of break glass account took place, and that
periodic testing is included in break glass emergency account management
procedure.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><ul>
<li><p>Obtain signature from Departmental Chief Information Officer
(CIO) <mark>in collaboration with designated official for cyber security
(DOCS)</mark> to confirm acknowledgement and approval of the break glass
emergency account management procedures.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm through attestation that the Departmental Chief
Information Officer (CIO) <mark>in collaboration with DOCS</mark> have
approved the break glass emergency account management procedure for the
cloud service.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Additional Considerations</strong></td>
</tr>
<tr class="even">
<td><ul>
<li><p>Develop a cloud backup strategy that takes into account where GC
data is stored, replicated, or backed up by the cloud service, in
consideration of the IT continuity plan for the
service/application.</p></li>
</ul></td>
<td><ul>
<li><p>Confirm through attestation that the cloud backup strategy
procedure is developed and approved by the business owner.</p></li>
<li><p>Verify if there are scripts that support the ability to restore
from code (e.g., infrastructure as code).</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><ul>
<li><p>Ensure that cloud workloads are associated with the applicable
Application ID in the TBS Application Portfolio Management (APM) tool,
in support of the Standard on At-Risk Technology.</p></li>
</ul></td>
<td><ul>
<li><p>Provide a list of all software, including versions, deployed on
VMs associated with the application IDs from APM.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><ul>
<li><p>Ensure departmental cyber security event management plans include
cloud services, in alignment with the GC Cyber Security Event Management
Plan.</p></li>
</ul></td>
<td><ul>
<li><p>Provide a list of all software, including versions, deployed on
VMs associated with the application IDs from APM.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td colspan="2"><p><strong>References</strong></p>
<ol type="1">
<li><p><a
href="https://www.canada.ca/en/treasury-board-secretariat/services/access-information-privacy/security-identity-management/direction-secure-use-commercial-cloud-services-spin.html">SPIN 2017-01</a>,
<a
href="https://www.canada.ca/en/government/system/digital-government/digital-government-innovations/cloud-services/direction-secure-use-commercial-cloud-services-spin.html#toc6-2-9">sub-section
6.2.9</a></p></li>
<li><p>Refer to the <a
href="https://gcconnex.gc.ca/file/view/55010566/break-glass-emergency-account-procedure-departments-can-use-to-develop-their-emergency-access-management-controls-for-cloud?language=en">template</a>
for a break glass emergency account management procedure.</p></li>
<li><p>Refer to the <a
href="https://www.gcpedia.gc.ca/gcwiki/images/6/66/Department_CSEMP_Template.docx">Department
Cyber Security Event Management Plan (CSEMP) Template</a>.</p></li>
<li><p><a
href="https://www.tbs-sct.canada.ca/pol/doc-eng.aspx?id=32601"><mark>Directive
on Service and Digital- Canada.ca</mark></a></p></li>
</ol></td>
</tr>
<tr class="even">
<td colspan="2"><strong>Related security controls:</strong> AC-1,
CP-1,CP-2,CP-9,CA-3</td>
</tr>
</tbody>
</table>
