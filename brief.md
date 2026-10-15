Version: NAFATH-V1


Track: Cybersecurity

Overview
Launching a national digital login service requires seamlessly integrating multiple technical domains to deliver a secure and unified user experience. Software architecture establishes standardized authentication and authorization flows, while artificial intelligence models continuously analyze session patterns to flag suspicious login attempts in real time. Mobile application frameworks enforce strict runtime permission controls on user devices to safeguard sensitive APIs. Underlying networking protocols protect domain name resolution against pervasive eavesdropping and tampering. Robust cybersecurity principles guarantee verifiable, phishing-resistant authentication methods, and data governance frameworks ensure strict compliance with national privacy legislation during collection and storage. Together, these six interdependent components build a highly resilient and trustworthy identity infrastructure for citizens accessing government services.

## Software

OAuth 2.0 is an authorization framework designed to grant delegated access to resources without sharing credentials, using access tokens. OpenID Connect (OIDC) is an identity layer built on top of OAuth 2.0 that introduces an ID token to authenticate users and verify their identity. Therefore, OIDC is specifically designed for user login and authentication, while OAuth 2.0 is designed for authorization and delegated resource access.

Resource: OpenID Foundation - OpenID Connect Core 1.0 - https://openid.net/specs/openid-connect-core-1_0.html

## AI

Using the NIST AI Risk Management Framework (NIST AI 100-1), the authority must manage risks related to validity, reliability, bias, and fairness to prevent high false-positive rates that lock out legitimate citizens. Additionally, privacy and confidentiality risks must be addressed to protect citizen data during behavioral anomaly detection, alongside security and resilience against adversarial evasion attacks targeting the login anomaly classifier.

Resource: NIST - Artificial Intelligence Risk Management Framework (NIST AI 100-1) - https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.100-1.pdf

## Mobile

Android's runtime permission model restricts apps from accessing sensitive data (such as contacts or storage) and dangerous system features at install time. Instead, the login app must explicitly request permissions from the user at runtime the exact moment a specific feature or protected data is required. If the user denies permission, the app must handle the limitation gracefully without crashing while preserving core functionality.

Resource: Android Developers - Permissions overview - https://developer.android.com/guide/topics/permissions/overview

Networking

Cybersecurity

Data

Misconception in My Track

Open Question
