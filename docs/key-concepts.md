# Key Concepts

The Neoflow platform relies on a set of standard specifications developed under W3C to enable interoperability with decentralized and traditional IT systems.

## Decentralized Identity (DID)

Organizations interacting with the Neoflow platform use Decentralized Identifiers (DIDs) as their Organizational Identifiers Decentralized identifiers  are a type of digital identity that allow individuals, organizations, and things to have control over their own digital identity, without relying on centralized authorities or third-party intermediaries. In supply chains, DIDs can be used to securely and verifiably track the movement of goods from one stage of the supply chain to another. This provides a number of benefits, including increased transparency, security, and efficiency.

One of the main advantages of using DIDs on supply chains is that they provide a secure and tamper-proof record of each stage of the supply chain. This can help to prevent fraud, counterfeiting, and other forms of supply chain malpractice. DIDs can also be used to ensure that goods are produced and transported in compliance with relevant regulations and standards, which can help to increase consumer trust and confidence in the supply chain.

In addition to these benefits, DIDs can also help to increase efficiency in supply chains by reducing the need for intermediaries and middlemen. By providing a secure and transparent record of each stage of the supply chain, DIDs can help to streamline the process of tracking and verifying goods as they move from one stage to another. This can help to reduce costs, increase speed, and improve overall supply chain performance.

## Verifiable Credential (VC) and Verifiable Presentation (VP)

Verifiable credentials are digital representations of a person or organization's identity, qualifications, or other attributes that have been cryptographically signed by a trusted issuer. They can be used to securely and verifiably attest to a wide range of information, from a person's age or vaccination status to a company's compliance with environmental or labor standards.

Neoflow uses verifiable credentials to verify the identity and qualifications of suppliers, as well as the authenticity and provenance of products as they move through the supply chain. By attaching verifiable credentials to each stage of the supply chain, from raw materials to finished products, it becomes possible to track the movement of goods and ensure that they meet the necessary quality and safety standards.

Verifiable credentials can also help to address some of the major challenges in supply chain traceability, such as the lack of trust and coordination between different parties. By enabling the secure and transparent sharing of information between suppliers, manufacturers, distributors, and retailers, verifiable credentials can help to build trust and facilitate more effective collaboration. This can lead to a more efficient and resilient supply chain, as well as increased consumer confidence and loyalty.

## Traceability Vocabulary and Interoperability Profile

The schemas used for the verifiable credentials are defined in the traceability vocabulary being developed under [W3C-CCG Traceability Vocabulary](https://w3c-ccg.github.io/traceability-vocab/).The vocabularies for relevant value chain documents, such as [crude oil](https://w3c-ccg.github.io/traceability-vocab/#CrudeOilProduct) and [natural gas](https://w3c-ccg.github.io/traceability-vocab/#NaturalGasProduct) certificates of origin, [delivery tickets](https://w3c-ccg.github.io/traceability-vocab/#OGBillOfLading), inspection reports and events are fully supported on the platform.

Neoflow uses the [W3C-CCG Traceability Interop profile](https://w3c-ccg.github.io/traceability-interop/draft/) - as an interoperable API specification for issuing, transmitting and verifying the Verifiable Credentials.
