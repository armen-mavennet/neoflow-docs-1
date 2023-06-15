## Compliance

This section is to provide details on data regulations which Neoflow follows to ensure data privacy and security. Please note that, PIPEDA* and Privacy Act** do not apply directly to the use cases, but Neoflow continues to follow the principles to enhance data privacy. This section is meant to serve as a framework for data regulation to be followed, however it will be reviewed by a legal professional before it is finalized.


Neoflow also follows a set of broadly accepted technology standards to methodically ensure appropriate level of security to avoid the following threats:
* Unauthorized access and privilege escalation
* Eavesdropping of information that a particular organization or 3rd party should not have access to
* Tampering of information
* Denial of Service Attacks (DoS)

Neoflow is intended to be deployed on NIST compliant infrastructure and designed to be compliant with

* [FIPS 180-4](https://csrc.nist.gov/publications/detail/fips/180/4/final){:target="_blank"}
* [FIPS 186-5](https://csrc.nist.gov/publications/detail/fips/186/5/draft){:target="_blank"}
* [FIPS 197](https://csrc.nist.gov/publications/detail/fips/197/final){:target="_blank"}


Neoflow Managed Infrastructure is deployed on sandboxed environments and are deployed on AWS.

Self Managed infrastructure may be deployed on any cloud provider/ on-premise infrastructure and the security is the responsibility of the managing organization.

|     | Document      | Description                          |
| ----------- | ----------- | ------------------------------------ |
| ![SOC 2](images/SOC-2-logo.png){: style="height:50px;width:50px"} | [SOC 2 Type 1](/files/Neoflow Inc_Letter of Attestation SOC 2 Type 1.pdf){:target="_blank"}       | Developed by the American Institute of CPAs (AICPA), SOC 2 defines criteria for managing customer data based on five “trust service criteria” — security, availability, processing integrity, confidentiality and privacy. |
| ![SOC 2](images/SOC-2-logo.png){: style="height:50px;width:50px"} | [SOC 2 Type 2](/files/Neoflow Inc_Letter of Attestation SOC 2 Type 1.pdf){:target="_blank"}       | Developed by the American Institute of CPAs (AICPA), SOC 2 defines criteria for managing customer data based on five “trust service criteria” — security, availability, processing integrity, confidentiality and privacy.  |
| ![SAIS](images/ais-logo.png){: style="height:50px"}|[Red Team Attestation](/files/Attestation-Neoflow-Letter-of-Confirmation_Remediation.pdf){:target="_blank"}       | In November 2022, Assured Information Security conducted a functional, operational, and security assessment of Neoflow. Testing and evaluation (T&E) consisted of validating the technology’s overall functionality, identifying potential vulnerabilities in credential workflows and their associated communications, and evaluating the privacy implications associated with the use of the technology.  |


## Common Questions
Neoflow has been built with cybersecurity and data privacy at the core


??? question "What type of information does Neoflow store and manage?"
    Neoflow enables industry participants to store and manage information related to shipments of Crude Oil and Natural Gas (e.g., production, blending, dilution, storage, transportation, border declaration, refinement).
??? question "Who is my data shared with?"
    No data is shared unless explicitly requested by the organization that owns the data. For example, importer requests Neoflow for the shipment information to be shared with CBP once there is intent to import.
??? question "Does Neoflow store PII (Personally identifiable information)?"
    No. Neoflow does not request, store or manage PII.
??? question "Does Neoflow store PHI (Protected health information)?"
    No. Neoflow does not request, store or manage PHI.
??? question "Did Neoflow undergo security testing?"
    Neoflow has successfully completed the U.S. Department of Homeland Security (DHS) platform review process, called Red Team Testing. This process is designed to perform an independent comprehensive review of system architecture, security, scalability and standards compliance (NIIST/FISMA) in order to ensure Neoflow is ready to be operated in production by the U.S. DHS. Please refer to Page 10 of this document for Red Team Assessment Results.
??? question "Does Neoflow have technology controls in place to protect against the OWASP Top 10 attacks?"
    Yes. Neoflow is protected against the OWASP Top 10 attacks through the use of modern frameworks to alleviate a class of attack (for example, SQL injection and XSS), relying on load balancers and AWS shield to protect against DDOS attacks. Neoflow infrastructure is also Highly Available with a multiple Availability Zones setup in accordance with the [AWS well architected framework](https://aws.amazon.com/architecture/well-architected/){:target="_blank"}.
??? question "Does Neoflow have a Disaster Recovery Plan and a Business Continuity Plan?"
    Yes. Neoflow is built with 24-hour RTO and 4-hour RPO SLAs. we are currently finalizing  Disaster Recovery and Business Continuity Plans, and both will be complete prior to the start of the Tech Demo/Pilot. Once complete, it will be shared with current and prospective clients.
??? question "What is the data ownership, security and data sharing model within Neoflow?"
    Proprietary information is held securely and privately with the owner of the data retaining ownership of its information at all times.

    When the data owner chooses to share the data with another organization, the selected data is shared with that organization securely. Sharing of data occurs only at the explicit request of the data owner.
??? question "Will government agencies (e.g., US CBP, CER) have access to data?"
    No entity has access to any data without the express permission of the owner of the data and it is solely at the discretion of the data owner when and what information is shared with CBP.

    Government agencies like CBP will only be able to access the information that they are given permission to access by the owner of the data.  This permission by the owner will be for certain information required to be shared if the owner of the data will be importing the product and claiming USMCA such as pre-arrival information and the information required to make the appropriate Customs entry and USMCA preference.
    
    The parameters around the access given to each agency will be pre-determined and parties using Neoflow will be aware of what information can be shared.
??? question "What data is each party responsible for?"
    Each party owns and is responsible for its own information which cannot be altered by any other party.
    
    Each party’s information is added to the life cycle of the product but cannot be shared with any other party unless expressly shared by the owner or as expressly allowed within the parameters of CBP’s authority to view.
    
    For example, when the producer creates a record of the batch produced, once the ownership is transferred to a downstream participant (e.g., refinery importing the batch into the US), the producer does not have visibility to data that is entered at that point.
??? question "Where is my data stored?"
    Firstly, each organization using our service is set up as an isolated Tenant with a separate AWS account in accordance with AWS Multi Account Best practices. Within each tenant, all private data is encrypted and stored on a private subnet AWS RDS while all shared data is encrypted and stored on the Neoflow core AWS Tenant.
    
    Neoflow relies on AWS Security best Practices and has passed a Red Team Security review by the U.S. DHS. The Red Team attestation letter can be found on page 10 of this document.
??? question "Does anyone from Neoflow have access to my data?"
    At Neoflow, access to production data is limited to two designated Operations and Support employees.
    
    These employees do not access data under normal operations.
    
    Data access is required for deployment and support activities.
    
    Neoflow operates a comprehensive access control mechanism and monitoring system to ensure that access to the data is only granted to authorized personnel. AWS Control Tower is used to enforce access controls and to ensure that your data remains secure.
    
    Neoflow maintains a detailed audit log for all access to production data, which is available upon request.
    
    All policies and procedures regarding production data adhere to SOC 2 Type II standard.
??? question "What are Neoflow policies regarding Data Access and Data Privacy?"
    Neoflow follow the full set of SOC 2 policies and procedures, as evidenced by our SOC 2 Type II audit. This includes (but is not limited to) the following: Information Security Policy, Access Control Policy, Password Policy, Data Classification Policy, Physical Security Policy, Acceptable Use Policy, Backup Policy, Logging and Monitoring Policy, Risk Management Policy, Incident Response Policy, Business Continuity Plan, among other relevant policies.



