Version: NAFATH-V1


Track: Cybersecurity

Overview
Launching a national digital login service requires seamlessly integrating multiple technical domains to deliver a secure and unified user experience. Software architecture establishes standardized authentication and authorization flows, while artificial intelligence models continuously analyze session patterns to flag suspicious login attempts in real time. Mobile application frameworks enforce strict runtime permission controls on user devices to safeguard sensitive APIs. Underlying networking protocols protect domain name resolution against pervasive eavesdropping and tampering. Robust cybersecurity principles guarantee verifiable, phishing-resistant authentication methods, and data governance frameworks ensure strict compliance with national privacy legislation during collection and storage. Ultimately, implementing robust cybersecurity measures remains the cornerstone of defending national identity infrastructure against sophisticated credential harvesting attacks.

## Software

OAuth 2.0 is an authorization framework designed to grant delegated access to resources without sharing credentials, using access tokens. OpenID Connect (OIDC) is an identity layer built on top of OAuth 2.0 that introduces an ID token to authenticate users and verify their identity. Therefore, OIDC is specifically designed for user login and authentication, while OAuth 2.0 is designed for authorization and delegated resource access.

Resource: OpenID Foundation - OpenID Connect Core 1.0 - https://openid.net/specs/openid-connect-core-1_0.html

## AI

Using the NIST AI Risk Management Framework (NIST AI 100-1), the authority must manage risks related to validity, reliability, bias, and fairness to prevent high false-positive rates that lock out legitimate citizens. Additionally, privacy and confidentiality risks must be addressed to protect citizen data during behavioral anomaly detection, alongside security and resilience against adversarial evasion attacks targeting the login anomaly classifier.

Resource: NIST - Artificial Intelligence Risk Management Framework (NIST AI 100-1) - https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.100-1.pdf

## Mobile

Android's runtime permission model restricts apps from accessing sensitive data (such as contacts or storage) and dangerous system features at install time. Instead, the login app must explicitly request permissions from the user at runtime the exact moment a specific feature or protected data is required. If the user denies permission, the app must handle the limitation gracefully without crashing while preserving core functionality.

Resource: Android Developers - Permissions overview - https://developer.android.com/guide/topics/permissions/overview

## Networking

DNS over HTTPS (DoH) resolves domain names via the encrypted HTTPS protocol rather than plain text UDP/TCP. It protects users against pervasive surveillance, tracking, and on-path manipulation or spoofing of DNS queries by local networks or ISPs. However, DoH does not protect the final IP address visited after the connection is established, nor does it secure endpoints against malware or local device compromise.

Resource: IETF - RFC 8484: DNS Queries over HTTPS (DoH) - https://www.rfc-editor.org/rfc/rfc8484

## Cybersecurity

An authentication method is phishing-resistant if it cryptographically binds credentials to the specific origin or domain being accessed, ensuring they cannot be intercepted or replayed by a fraudulent site. FIDO2 / WebAuthn hardware security keys and passkeys qualify as phishing-resistant. Conversely, SMS one-time passwords (OTPs), voice calls, push notifications, and software-based TOTP apps do not qualify because users can still be tricked into entering them on rogue phishing portals.

Resource: NIST - Special Publication 800-63B: Digital Identity Guidelines - https://pages.nist.gov/800-63-3/sp800-63b.html

## Data

Under Oman’s Personal Data Protection Law (Royal Decree No. 6/2022), the authority must obtain explicit, lawful consent from citizens before collecting personal data, clearly stating the processing purpose. It is obligated to ensure data accuracy, implement strict technical and organizational security measures to prevent unauthorized access or breach, restrict retention periods, and respect data subjects' rights to access, rectify, or erase their stored personal information.

Resource: Ministry of Transport, Communications and Information Technology - Personal Data Protection Law - https://www.mtcit.gov.om/ITAPortal/Data/English/DocLibrary/202361111512411/Royal-Decree-No-6-2022-Promulgating-the-Personal-Data-Protection-Law.pdf

## Misconception in My Track

A common misconception in cybersecurity is that multi-factor authentication methods like SMS OTPs and push notifications are fully phishing-resistant because they require a second factor beyond a password. However, the correct version is that these methods are vulnerable to real-time Adversary-in-the-Middle (AiTM) proxy attacks where attackers intercept codes or approve prompts on fake login portals. True phishing-resistance requires cryptographic binding to the origin domain, which is only achieved by FIDO2/WebAuthn authenticators. This distinction is explicitly detailed in NIST SP 800-63B guidelines regarding authenticators resistant to verifier impersonation.

## Open Question

How can government authorities balance the strict user adoption requirements of phishing-resistant passkeys with the practical accessibility challenges faced by elderly citizens using legacy mobile devices?
