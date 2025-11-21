# Open Agent Commerce Protocol (OACP) Specification

[![Specification v0.1 (Draft)](https://img.shields.io/badge/Version-0.1%20(Draft)-blue.svg)](https://github.com/oap-foundation/oacp-spec/blob/main/specification/v0.1.md)
[![Status: Public Draft for Discussion](https://img.shields.io/badge/Status-Public%20Draft%20for%20Discussion-orange.svg)](https://github.com/oap-foundation/oacp-spec/discussions)
[![Layer 1 (Application Protocol)](https://img.shields.io/badge/Layer-1%20(Application)-lightgrey.svg)](https://github.com/oap-foundation/oap-framework)

This repository contains the official technical specification for the **Open Agent Commerce Protocol (OACP)**.

OACP is a Layer 1 Application Protocol within the [Open Agent Protocol Framework](https://github.com/oap-foundation/oap-framework). While [OAEP](https://github.com/oap-foundation/oaep-spec) handles the trust and connection layer, **OACP** defines the standard for autonomous agents to conduct economic activity: finding products, negotiating prices, placing orders, and settling payments without centralized intermediaries.

## The Problem Solved by OACP

Current digital commerce is siloed within centralized platforms (Amazon, Uber, App Stores) that extract high fees and control user data. AI agents currently lack a standardized way to "do business" with each other across these silos.

OACP provides a universal language for **Agent-to-Agent (A2A) Commerce**. It allows an agent representing a buyer to seamlessly transact with an agent representing a seller, regardless of the underlying platform or payment rails.

## Core Concepts

OACP standardizes the lifecycle of a digital transaction:

1.  **Discovery & Intent:** How an agent broadcasts what it is looking for (an `Intent`) or what it offers.
2.  **Negotiation:** A structured message flow to agree on terms (e.g., `Offer`, `CounterOffer`, `Acceptance`).
3.  **Contract:** The creation of a cryptographically signed agreement (`SmartInvoice`) that binds both agents.
4.  **Settlement:** Agnostic integration with payment rails (Crypto, Lightning, Fiat/Stripe) to prove payment completion (`PaymentReceipt`).

## Specification Document

The full technical specification is a work in progress and is being developed in this repository.

> **➡️ [Read the full OACP v0.1 Specification (Draft)](/specification/v0.1.md)**
> *(Note: The spec itself is located in the `/specification` folder.)*

This document details:
*   The JSON schemas for commerce objects (`Product`, `Order`, `Invoice`).
*   The state machine for transaction lifecycles (Pending -> Paid -> Delivered).
*   Error handling for disputes and refunds.

## Reference Implementations

To help developers build compliant commerce agents, we provide official reference implementations.

### PHP
*   **[oap-foundation/oacp-php](https://github.com/oap-foundation/oacp-php)**
    *   The first reference implementation of OACP v0.1.
    *   Includes classes for creating Offers, validating Invoices, and managing the transaction state machine.

## Status: Public Draft for Discussion

This specification is at a very early stage (**v0.1 Draft**). It is published as a "Strawman Proposal" to serve as a concrete basis for technical discussion with the developer and e-commerce community. We explicitly invite feedback, critique, and proposals for improvement.

## How to Contribute

We are looking for contributions from e-commerce experts, payment engineers, and agent developers.

*   **To propose a change,** please [open a new issue](https://github.com/oap-foundation/oacp-spec/issues/new) to discuss your idea.
*   **To fix a typo or improve wording,** please submit a pull request directly.

Please review our main [Contribution Guidelines](https://github.com/oap-foundation/oap-framework/blob/main/CONTRIBUTING.md) before you start.

## License

The Open Agent Commerce Protocol Specification is licensed under the [Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/).
