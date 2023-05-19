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
registered (should have at least two and no more than five).</p></li>
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
href="https://www.canada.ca/en/treasury-board-secretariat/services/access-information-privacy/security-identity-management/direction-secure-use-commercial-cloud-services-spin.html"><span>SPIN 2017-01</span></a>,
subsection 6.2.3</p></li>
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