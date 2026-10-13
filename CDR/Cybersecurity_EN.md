# CDR Cybersecurity, Lauren Challis

## B1: CIS Controls incorporated into policy documents

*M1: Appropriate level of cybersecurity and consistency | Basis: Art. 15.1*

**Context and Problem Statement**

There was a great deal of information regarding Hansken’s cybersecurity initiatives, but it was neither structured nor centralised, and as a result, compliance with cybersecurity standards could not be demonstrated. A policy framework is therefore required to provide direction in this area; this is also known as an ISMS (Information Security Management System). The long-term goal is to achieve ISO 27001 certification.

**Options considered**
* Establish CIS controls and associated policy documents

**Decision outcome**
Chosen option: B1: CIS Controls; 18 policy documents have been drawn up, one for each CIS control. These are available on Confluence (link). CIS and NIST are widely used standard approaches within the government – with the exception of the Ministry of Justice and Security (JenV) – for regulating cybersecurity. NIST is incorporated into the CIS policy.

**Consequences**
* Good, because: there is structure; a foundation for information security has been laid; you provide people with guidance, whilst also creating a means of enforcement. You can also demonstrate compliance.
* Bad, because: it is more bureaucratic and involves more paperwork. The average developer is not happy about having to read 18 policy documents. Developers now also have to take on additional security tasks that take up more time. In short, it is safer, but from the developers’ point of view, it does not work any better.

## B2: External penetration testing

*M1: Appropriate level of cybersecurity and consistency · M4: Protection against adversarial attacks | Basis: Art. 15.1, 15.5*
A penetration testing policy has been drawn up by the IT security team; this is set out in number 18 of the CIS Control policy documents.

**Context and problem statement**
This is a Ministry of Justice and Security (JenV) policy, and according to the BIO, a penetration test must be carried out following major releases. Penetration tests are carried out to build trust with partners and to verify the organisation’s own system. Furthermore, the penetration test is carried out externally to prevent any bias towards the organisation’s own system and to ensure a fresh perspective on the system’s operation.

**Options considered**
* Periodic external penetration tests, carried out following major changes, once a year, or on request (e.g. from external parties). Findings are reported to the process owner/system owner. There is a policy regarding the timeframes within which identified vulnerabilities must be rectified.

**Chosen option:**
“B2: External penetration tests as the primary attack simulation”, as penetration tests are carried out by an external party. Findings are categorised and followed up within set timeframes. The team lead issues a request to an external party to carry out a penetration test; these external parties include Sopra Steria. The government itself also offers penetration tests (NAME), but these take considerably longer and are more detailed than most commercial penetration tests. Government penetration tests are currently carried out when software needs to be accredited for internal use. Government penetration tests take considerably longer before a consultant can be arranged to visit. The IT security team checks whether the team lead has made this request and is involved from start to finish (from the initial assessment through to the centralised storage of the final penetration test report). The IT security team also ensures that the findings from the report are followed up within a specified timeframe; here, the IT security team acts as the monitoring body.

* Good, because: you have an external check, so you avoid bias. Penetration test auditors are specialists in their field, more so than a random developer. And it serves as external proof that you take cybersecurity seriously. It demonstrates that, as an organisation, you do not rely solely on your own expertise, but also allow an external party to look in to detect any blind spots.
* Bad, because: in the worst-case scenario, a penetration test could cause the system to go offline for a short period. However, it generally takes place in a controlled environment, so the risk of this happening is minimal. There is a risk that the external party carrying out the penetration test may not perform it properly and overlook significant flaws.

---

## B3: CVE scanning

*M1: Appropriate level of cybersecurity and consistency · M2: Resistance to unauthorised use and integrity breaches | Basis: Art. 15.1, 15.5*

**context and problem statement**
There was little to no insight into the current vulnerabilities in the containers in which Hansken is deployed. The Hansken team manages the Kubernetes platforms itself, based on Talos. Within that platform, we run software to perform CVE scanning on the containers. Due to a lack of insight, it was not possible to take corrective action regarding the number of vulnerabilities. CVE scanning on the containers is carried out by the Hansken team using Trivy. Once the partner starts hosting it themselves, they are encouraged to carry out the CVE scanning themselves.

**Options considered**
* Kubescape
* Trivy

**Option chosen:**
"B3: CVE scanning with Trivy. Trivy has been implemented in the current dashboard (Grafana), which is why Trivy was chosen. It is currently being deployed and is expected to go live in Q4 2026. Trivy is an open-source third-party solution. This is not necessarily a negative factor, as it runs locally, but there is a dependency on a third party. To mitigate this risk, Trivy is hosted locally; however, you remain dependent on updates from Trivy’s provider.
If Trivy detects CVEs with a severity rating higher than x(8/9), action must be taken to mitigate the resulting CVEs. (**#TODO: draw up a mitigation process**).

* Good, because: it provides insight into vulnerabilities, which can be addressed, for example, by taking on additional FTEs. Insight enables prioritisation. Makes the application much more secure.
* Bad, because: it can place an additional load on the environment, meaning you need more resources, such as CPU power and extra RAM, to keep the environment running.

---

## B4: OWASP dependency scan

*M1: Appropriate level of cybersecurity and consistency · M10: Protection against side-channel attacks | Basis: Art. 15.1, 15.5*
**Context and problem statement**
Vulnerabilities may arise in the dependencies used in the code. These vulnerabilities must be detected.

In addition to CVE scanning, vulnerabilities in the application dependencies are also systematically identified.

**Considered options**
* OWASP dependency scan, carried out alongside CVE scanning.

**Chosen option:**
“B4: OWASP dependency scan for application dependencies”.
It is a type of CVE scanning, but it focuses on the dependencies used in the code. Hansken downloads the National Vulnerability Database (NVD) once a day; internal code is then run against it to check for vulnerabilities in the dependencies used. The NVD database is downloaded locally (automated via a NIST API key), and on this local server the code is compared against the database of dependencies.


* Good, because: Your dependencies remain up to date; you are more secure; it is reassuring for partners to know that we use secure dependencies; and whatever is written is also tested. It is a lightweight tool.
* Bad, because: We are dependent on NIST; should NIST fail, we are at their mercy.

---

## B5: SAST tooling

*M1: Appropriate level of cybersecurity and consistency · M4: Protection against adversarial attacks | Basis: Art. 15.1, 15.5*

**Context and problem statement**
Software can become vulnerable if the code is poorly written. Potential SQL injections can lead to the disclosure of sensitive data. The four-eyes principle mitigates this, but it remains a manual process, and risks do occur. To reduce these risks, SAST tools are preferred, as they analyse the code and identify vulnerabilities.

**Options considered**
* Sonarqube
* Alternatives not documented.

**Option chosen:**
"B5: Sonarqube.

* Good, because: code becomes more secure; provides an extra set of eyes; is updated immediately based on new vulnerabilities; is too labour-intensive for humans. Hosted locally.
* Bad, because: reliance on Sonarqube, which could fail. It is a commercial provider.

---

## TO DO B6: SBOM

*M2: Resistant to unauthorised use and integrity breaches · M3: Prevent manipulation of datasets | Basis: Art. 15.5 (also relates to Art. 10.5)*

**Context and problem statement**
A register is required to ensure transparency regarding the system’s composition and the data sources used. An SBOM creates a list containing all components, libraries, modules and dependencies, along with their versions.

**Options considered**

**Option chosen:**
On the roadmap

* Good, because:
* Bad, because:

---

## TO DO B7: Container signing

*M2: Resistance to unauthorised use and integrity breaches | Basis: Art. 15.5*

**Context and problem statement**
Something is pushed to the customer, but there must be certainty that the person opening it is indeed the person who should be opening it. So your file is secured so that only the person to whom you send it can open it, rather than the network to which you send it being able to open it all.

**Options considered**

**Option chosen:**
On the roadmap

* Good, because: *not documented — to be specified*
* Bad, because: *not documented — to be specified*

---

## B8: Four-Eyes Principle

*M2: Resistance to unauthorised use and integrity breaches | Basis: Art. 15.5*

**Context and problem statement**
An individual employee may, unintentionally or deliberately, make vulnerable changes. To prevent this, you apply this principle. Jeroen van der Vegt

**Options considered**
* Dual control: changes require approval from multiple people, ensured via Git. Before code can be pushed, it passes through four different environments (development, test, acceptance, production). The person reviewing this is a second developer. One developer writes the code, one developer reviews it. It is then reviewed again during sprint meetings.

**Chosen option:**
“B8: Four-eyes for change management”, which is used to ensure changes are checked by several people. Changes are traceable because development takes place in Git.

* Good, because: it’s good to have two people checking, as people make mistakes. It’s simply a standard double-check.
* Bad, because: Errors can still slip through. But then you have the SAST tooling as a back-up.

---

## B9: SSO without 2FA
*M2: Resistance to unauthorised use and integrity breaches | Basis: Art. 15.5*

**Context and Problem Statement**
Hansken provides a standard Keycloak installation. This does not currently comply with SSO/2FA standards. This is partly because partners manage their own user administration and handle SSO themselves.
**# TO DO: explore options to make the default more secure** On the roadmap.

**Considered options**
*
**Chosen option:**

* Good, because:
* Bad, because:

---

## B10: Audit logging

*M2: Resistance to unauthorised use and integrity breaches | Basis: Art. 15.5*

**Context and problem statement**
Monitoring of system usage is required to investigate anomalous or unauthorised use. Audit logging allows you to see what happened should an error occur in the software. This is currently recorded in Git, which maintains version control, whereby changes are checked for integrity. Integrity means that it can be established that the data has not been manipulated or corrupted by malicious actors or hardware failure.

**Options considered**
* Code is logged in Git
**Option chosen:**
"B10: Audit logging in Git. I&B/IT security must monitor whether the environment in which Git runs remains intact.

* Good, because: cyber logging is in place. IT security is currently setting up the monitoring of the cyber logs.
* Bad, because: cyber logging is not yet being monitored.

---

## NOT RELEVANT B11: Approach to protection against data poisoning

*M3: Preventing manipulation of datasets · M5: Protection against system defects in the AI system itself | Basis: Art. 15.5*

The AI models in Hansken are trained on forensic data. If the training data or the model are manipulated, the results may become unreliable. Question: how is the model protected against manipulation of the training data and the model itself?

* The model is no longer updated. The developers of the model (DBS) are not the same party as those integrating the model into Hansken (NFI).

Chosen option: “B11: Approach to protecting training data and the model against data poisoning”, as the model is no longer being updated. The separation between the modelling party (DBS) and the integrating party (NFI) provides an organisational layer of security. The exact protective measures at DBS have not yet been confirmed (see Outstanding actions, point 2).

* Good, because: *not documented — to be completed*
* Bad, because: *not documented — to be completed*

---

## NOT RELEVANT  B12: Jailbreak detection

*M8: Protection against jailbreak attacks | Basis: Art. 15.5*

Hansken contains a co-pilot component. Jailbreaking may result in the system being used beyond its intended limits. Question: what measures are taken to prevent and detect jailbreaking?

* Software products are deployed on our own hardware to detect jailbreaking.

Chosen option: “B12: Jailbreak detection on our own hardware”, because software products have been deployed on our own hardware for jailbreak detection. Whether OpenHansken and the co-pilot inherently provide for this has not yet been verified (see Outstanding actions, point 3).

* Good, because: *not documented — to be completed*
* Bad, because: *not documented — to be completed*

---

## NOT RELEVANT B13: Social engineering of operators

*M11: Protection against social engineering | Basis: Art. 15.5*

Hansken operators may be deceived through social engineering. Question: what measures protect operators against social engineering?

* A combination of: VGB-B screening, local login, e-learning, MFA and a time-out.

Chosen option: “B13: Social engineering measures for operators”, as the following measures have been implemented: a VGB-B screening, the option to log in locally only, e-learning, MFA and a time-out. The communication policy is still under development (see Outstanding actions, point 4).

* Good, because: *not documented — to be completed*
* Bad, because: *not documented — to be completed*

---

## 2. Measures not applicable

Following assessment, the measures listed below have been deemed not applicable to the architecture and use of Hansken. The rationale is provided for each measure.

## M6: Protection against inversion attacks and model theft

*Rationale:* Not applicable. Hansken is not an open-API system where an attacker can reconstruct the model through repeated model queries. Access to Hansken requires authorisation and is not publicly available.

## M7: Protection against evasion attacks

*Rationale:* Not applicable. Hansken is not a classification or generative system in which input manipulation leads to a different classification or output that benefits the attacker.

## M9: Protection against membership inference

*Justification:* Not applicable. Users are authorised, and Hansken’s closed architecture minimises the risk of membership inference.

## 3. Confirmation of compliance (to be completed by the AI Helpdesk)

| Measure | Description | Basis | Status | Explanation |
|---|---|---|---|---|
| M1 | Appropriate level of cybersecurity and consistency | Art. 15.1 | Partially | CIS Controls mapping in place but not formally assessed. Consistency procedures not yet formally established. |
| M2 | Resistance to unauthorised use and integrity breaches | Art. 15.5 | Partially | CVE, SBOM, container signing, four-eyes principle, SSO and access list in place. No real-time alerts. |
| M3 | Prevention of dataset manipulation | Art. 15.5 | Partial | SBOM and checksum controls in place. Data poisoning protection at DBS still pending (action 2). |
| M4 | Protection against adversarial attacks | Art. 15.5 | Partial | Penetration tests and SAST in place. No adversarial attack exercises or red teaming. |
| M5 | Protection against system defects in the AI system itself | Art. 15.5 | Partially | Partially assessed; dependent on DBS’s response (action 2). |
| M6 | Protection against inversion attacks and model theft | Art. 15.5 | N/A | Not applicable. Hansken is not an open-API system; users are authorised. |
| M7 | Protection against evasion attacks | Art. 15.5 | N/A | Not applicable. No classifying/generative system in which input manipulation leads to different output. |
| M8 | Protection against jailbreak attacks | Art. 15.5 | Partially | Detection available on own hardware. Status of OpenHansken/copilot still pending (action 3). |
| M9 | Protection against membership inference | Art. 15.5 | N/A | Not applicable. Closed architecture; users have authorisation. |
| M10 | Protection against side-channel attacks | Art. 15.5 | Partial | OWASP dependency scan and firewall in place. Full inventory not yet completed. |
| M11 | Protection against social engineering | Art. 15.5 | Addressed | VGB-B, e-learning, MFA, SSO, time-out and local access in place. Communication policy under development (action 4). |

## 4. Outstanding actions + timeline

1. **Formally assess CIS Controls mapping** — the mapping carried out by Hansken against the CIS Controls has not yet been formally validated. Action: have it reviewed by an independent party or an internal assessment framework. **We will do this by date X at the latest. We will update the CDR on date Y.**
2. **Enquire about DBS’s protective measures** — the measures taken by DBS to protect the training data and the model have not yet been confirmed. Action: request written confirmation from DBS.
3. **Check jailbreak detection in OpenHansken and Copilot** — whether OpenHansken and the Copilot component inherently provide for jailbreak detection has not yet been investigated. Action: enquire with the technical owner of Copilot.
4. **Finalise the social engineering communication policy** — the policy for secure communication between clients and supervisory staff is still being developed. Action: finalise and document it as part of the security guidelines.
5. **Confirm the scope of OpenHansken** — whether OpenHansken and the copilot explicitly fall within the scope of this CA must be formally confirmed by the system owner.
