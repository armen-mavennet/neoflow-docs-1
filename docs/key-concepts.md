# Key Concepts

The Neoflow platform relies on a set of standard specifications developed under W3C to enable interoperability with decentralized and traditional IT systems.

## Decentralized Identity (DID)

Every organization onboarded on the Neoflow platform are uniquely identified by a Decentralized Identifier (DID) and will rely on DID when publishing data on the network.DID is a standard developed by [DID Working Group](https://www.w3.org/2019/did-wg/) under [W3C DID specification](https://www.w3.org/TR/did-core) which describes DID as below:

> Decentralized identifiers (DIDs) are a new type of identifier that enables verifiable, decentralized digital identity.A DID identifies any subject (e.g., a person, organization, thing, data model, abstract entity, etc.) that the controller of the DID decides that it identifies.In contrast to typical, federated identifiers, DIDs have been designed so that they may be decoupled from centralized registries, identity providers, and certificate authorities.Specifically, while other parties might be used to help enable the discovery of information related to a DID, the design enables the controller of a DID to prove control over it without requiring permission from any other party.DIDs are URIs that associate a DID subject with a DID document allowing trustable interactions associated with that subject.
>
> Each DID document can express cryptographic material, verification methods, or services, which provide a set of mechanisms enabling a DID controller to prove control of the DID.Services enable trusted interactions associated with the DID subject.A DID might provide the means to return the DID subject itself, if the DID subject is an information resource such as a data model.
>
> This document specifies the DID syntax, a common data model, core properties, serialized representations, DID operations, and an explanation of the process of resolving DIDs to the resources that they represent.

## Verifiable Credential (VC) and Verifiable Presentation (VP)

All product and event information is stored in the form of Verifiable Credentials on the Neoflow platform.Verifiable Credentials are a standard developed by [Verifiable Credentials Working Group](https://www.w3.org/2017/vc/WG/) under [W3C VC Data Model](https://www.w3.org/TR/vc-data-model) which describes VC and VP as below:

>In the physical world, a credential might consist of:
>
> - Information related to identifying the subject of the credential (for example, a photo, name, or identification number).
> - Information related to the issuing authority (for example, a city government, national agency, or certification body).
>
> - Information related to the type of credential this is (for example, a Dutch passport, an American driving license, or a health insurance card).
>
> - Information related to specific attributes or properties being asserted by the issuing authority about the subject (for example, nationality, the classes of vehicle entitled to drive, or date of birth).
>
> - Evidence related to how the credential was derived.
>
> - Information related to constraints on the credential (for example, expiration date, or terms of use).
>
>A verifiable credential can represent all of the same information that a physical credential represents.The addition of technologies, such as digital signatures, makes verifiable credentials more tamper-evident and more trustworthy than their physical counterparts.
>
>Data derived from one or more verifiable credentials, issued by one or more issuers, that is shared with a specific verifier.A verifiable presentation is a tamper-evident presentation encoded in such a way that authorship of the data can be trusted after a process of cryptographic verification.Certain types of verifiable presentations might contain data that is synthesized from, but do not contain, the original verifiable credentials (for example, zero-knowledge proofs).
>
>Holders of verifiable credentials can generate verifiable presentations and then share these verifiable presentations with verifiers to prove they possess verifiable credentials with certain characteristics.
>
>Both verifiable credentials and verifiable presentations can be transmitted rapidly, making them more convenient than their physical counterparts when trying to establish trust at a distance.

Neoflow uses [W3C-CCG Traceability Interop profile](https://w3c-ccg.github.io/traceability-interop/draft/) - as an interoperable API specification for issuing, transmitting and verifying the VCs.

## Traceability Vocabulary

The schemas used for the verifiable credentials are the common traceability vocabulary being developed under [W3C-CCG Traceability Vocabulary](https://w3c-ccg.github.io/traceability-vocab/).The vocabularies for relevant value chain documents, such as [crude oil](https://w3c-ccg.github.io/traceability-vocab/#CrudeOilProduct) and [natural gas](https://w3c-ccg.github.io/traceability-vocab/#NaturalGasProduct) certificates of origin, [delivery tickets](https://w3c-ccg.github.io/traceability-vocab/#OGBillOfLading), inspection reports and [in-bonds](https://w3c-ccg.github.io/traceability-vocab/#Inbond) are fully supported on the platform.This enables the platform to be interoperable with the vendors in the value chain using the former mentioned standards.

## Revocation

Revocation means invalidating the status of a verifiable credential by its issuer.If the VC is revoked the information stored in a VC is considered to be invalid.Neoflow is able to support VC revocation based on the [W3C-CCG Status List 2021](https://w3c-ccg.github.io/vc-status-list-2021/) specification.
