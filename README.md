# EUDIW-4-Payments
Monitoring the status of EUDIW-4-Payments (my name of the EUDIW payment functionality).

## Regulatory Status (as of June 2026)
This is a complex topic since:
- Currently there is no [standard](#standardization-status-as-of-june-2026) for EUDIW-based payments
- Financial institutions are reportedly _obliged_ to accept payments using the EUDIW
- None of current Government-driven EUDIW projects appear to support payments

The conclusion is that wallet providers are not forced to implement payment support, leaving financial institutions with the daunting task accepting _an unknown set of proprietary and unique_ wallet solutions.  Since wallet software is provided for free on "app stores", it seems that the only _sustainable_ solution is that banks cater for such developments themselves, like they already do for Wero and as well as for national payment solutions like Swish, BLIK, Bizum, MobilePay, etc.

The EIDIW proponents claim that SCA (Strong Customer Authentication) is a major differentiator.  This is incorrect; the competition without exceptions already supports SCA since this is a mandatory feature since PSD2 (2015).  In fact, the EUDIW-4-Payments project has [multiple challengers](#product-status-as-of-june-2026), including by the European Payments Initiative (nowadays known as "Wero").

## Standardization Status (as of June 2026)
As far as I know, the LSPs (Large Scale Pilots) were supposed to test and verify the usability of the ARF as well as provide feedback to the ARF designers.

However, neither the LSPs nor the ARF designers were tasked with creating a standard for payment authorizations.  The ARF is currently only framework and no concrete implementations have (to date) been supplied.

A standardization activity is characterized by:
- Organization
- Deliverables and time-lines
- Meetings
- Mailing lists
- Chair-persons
- Processes, including voting
- Membership agreements
- Funding model

None of this apply to the _current_ ARF activity.  Comparable standardization activities like
[Secure Payment Confirmation by W3C](https://www.w3.org/TR/secure-payment-confirmation/) typically take at least 3 years
making such endeavors out of scope for most SMEs, unless _external funding_ is provided.

## Product Status (as of June 2026)
Regardless of what the incentives for EUDIW-4-Payments may be, it will by most people be viewed as a "product".  This means that it will be compared with similar solutions including Apple Pay and Wero.

Based on public information, it is not clear what EUDIW-4-Payments brings to the table compared to the competition.  In fact, the only mentioned unique feature (SCA is not), is the ability to mix SCA attestations with arbitrary attributes like age-verification.  However, this use-case appears to be _invalid_ because age-verification is something Merchants must (for certain products and services only), obtain _before_ a payment can be requested.  That is, there seems to be no real-world use-case requiring mixing payments and selectively disclosed attributes.  Associated GitHub issues:
- [Violating "Privacy by Design" principles](https://github.com/eu-digital-identity-wallet/eudi-doc-standards-and-technical-specifications/issues/581)
- [Selective disclosures make no sense for payments](https://github.com/eu-digital-identity-wallet/eudi-doc-standards-and-technical-specifications/issues/574)

## Proposal
Although payment-related use-cases share some characteristics with identity-related use-cases, flows, actors, trust-models, privacy and security considerations are quite different.  Due this I believe that these use-cases would gain by being _separated_.  This does not eliminate the use of a common wallet.

V0.1, Anders Rundgren
