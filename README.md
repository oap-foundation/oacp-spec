# Open Agent Commerce Protocol (OACP) Specification

<p align="center">
  <img src="https://img.shields.io/badge/Version-0.1%20(Draft)-blue.svg" alt="Specification v0.1 (Draft)">
  <img src="https://img.shields.io/badge/Status-Public%20Draft%20for%20Discussion-orange.svg" alt="Status: Public Draft for Discussion">
  <img src="https://img.shields.io/badge/Layer-1%20(Application)-green.svg" alt="Layer 1 (Application)">
</p>

This repository contains the official technical specification for the **Open Agent Commerce Protocol (OACP)**.

OACP is a Layer 1 application protocol of the [Open Agent Protocol Framework](https://github.com/oap-foundation/oap-framework). It is designed to run on top of a secure connection established via **OAEP**. OACP standardizes fair, transparent, and legally binding commercial transactions between autonomous AI agents.

## The Problem Solved by OACP

Today's digital commerce is dominated by centralized gatekeepers who dictate the rules, extract exorbitant fees (15-30% "gatekeeper tax"), and create an opaque marketplace where marketing budgets often trump product quality. This stifles innovation and puts small and medium-sized enterprises (SMEs) at a significant disadvantage.

OACP aims to disintermediate these gatekeepers by creating a common, open language for agent-to-agent commerce, enabling a renaissance of fair competition.

## Core Concepts

OACP translates the complex rituals of commerce into a machine-readable, verifiable, and secure protocol.

1.  **Fact-Based Discovery:** Agents search for products and services based on verifiable criteria (e.g., "Show me laptops with an EcoFriendlyCertified VC"), not on manipulated search rankings.
2.  **Semantic Interoperability:** Using standard vocabularies like JSON-LD and [Schema.org](https://schema.org/), OACP ensures that offers and requests are understood unambiguously by all participating agents.
3.  **Transactional Integrity:** OACP defines mechanisms for atomic order/payment linking and a fair, evidence-based dispute resolution framework, replacing the arbitrary policies of today's platforms.
4.  **Legal Certainty:** Transactions are made legally binding through the use of eIDAS-compliant electronic signatures, as established by the underlying OAEP layer.

## Specification Document

The full technical specification is a work in progress and is being developed in this repository.

> **➡️ [Read the full OACP v0.1 Specification (Draft)](/specification/v0.1.md)**
> *(Note: The spec itself should be a separate, more detailed markdown file within this repo, for example in a `/specification` folder.)*

This document details:
*   The core intents (`NegotiateRequest`, `OrderRequest`) and objects (`Product`, `OfferResponse`).
*   The standard transaction flow for a product purchase, from discovery to confirmation.
*   The structure of verifiable product claims.
*   The mechanisms for transactional atomicity (linking with OAPP) and dispute resolution.

## Status: OACP Lighthouse Project

OACP is the first and most critical Layer 1 protocol under development. Its successful implementation is the **"Lighthouse Project"** for the entire OAP ecosystem, designed to deliver the first undeniable proof of the economic superiority of a fair and open system.

The specification is currently a **v0.1 Draft** and serves as a "Strawman Proposal" for discussion with our initial founding partners in e-commerce, finance, and technology integration.

## How to Contribute

We are actively seeking experts in e-commerce, payment systems, supply chain logistics, and law to help shape this standard.

*   **To propose a change or discuss a use case,** please [open a new issue](https://github.com/oap-foundation/oacp-spec/issues/new). We want to ensure OACP solves real-world business problems from day one.
*   **To suggest an editorial change or fix a typo,** feel free to submit a pull request directly.

Please review our main [Contribution Guidelines](https://github.com/oap-foundation/oap-framework/blob/main/CONTRIBUTING.md) before you start.

## Relationship to Other Protocols

OACP is designed to work in concert with other OAP protocols:

*   **Depends on:** [**OAEP**](https://github.com/oap-foundation/oaep-spec) (must have an established OAEP connection).
*   **Works with:** **OAPP (Open Agent Payment Protocol)** for the payment authorization and settlement leg of a transaction. The `paymentRequest` object in an `OrderConfirmation` acts as the handover point to OAPP.

## License

The Open Agent Commerce Protocol Specification is licensed under the [Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/).
