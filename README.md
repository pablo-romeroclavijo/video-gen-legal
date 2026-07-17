# Reddit Stories — Legal Documents

This page contains the Terms of Service and Privacy Policy for the **Reddit Stories** TikTok content creator application.

---

## Terms of Service

**Last updated: July 2026**

### 1. Acceptance of Terms

By using the Reddit Stories application ("the App"), you agree to be bound by these Terms of Service. If you do not agree to these terms, please do not use the App.

### 2. Description of Service

The App is an automated content creation tool that sources publicly available posts from Reddit, adapts them into short-form video content, and publishes them to TikTok. The App operates under Reddit's API Terms of Service and TikTok's Developer Terms of Service.

### 3. Content and Copyright

- All Reddit posts used by the App are publicly available content sourced via the official Reddit API.
- Content is transformed and adapted for educational and entertainment purposes.
- Original Reddit post authors retain all rights to their original content.
- We do not claim ownership of any source material obtained from Reddit.

### 4. User Responsibilities

Users of this application are responsible for:
- Ensuring compliance with Reddit's API Terms of Service
- Ensuring compliance with TikTok's Terms of Service and Community Guidelines
- Maintaining valid API credentials and tokens
- Any content posted to TikTok accounts under their control

### 5. Prohibited Uses

You may not use the App to:
- Post content that violates Reddit's or TikTok's community guidelines
- Harass, defame, or target specific individuals
- Generate or distribute illegal content
- Circumvent any platform's terms of service

### 6. Disclaimers

THE APP IS PROVIDED "AS IS" WITHOUT WARRANTY OF ANY KIND. WE DO NOT GUARANTEE UNINTERRUPTED SERVICE, ACCURACY OF CONTENT SELECTION, OR CONTINUED AVAILABILITY OF THIRD-PARTY API ACCESS.

### 7. Limitation of Liability

We shall not be liable for any indirect, incidental, special, or consequential damages arising from your use of the App, including but not limited to loss of revenue, data, or business opportunities.

### 8. Changes to Terms

We reserve the right to modify these Terms at any time. Continued use of the App after changes constitutes acceptance of the updated Terms.

### 9. Contact

For questions about these Terms, please open an issue in this repository.

---

## Privacy Policy

**Last updated: July 2026**

### 1. Information We Collect

The App collects and processes the following information:

**Reddit Data:**
- Publicly available post titles, body text, scores, and metadata obtained via the Reddit API
- No private Reddit user data is collected

**TikTok Data:**
- TikTok account access tokens (stored locally in environment variables)
- Video upload status and publish IDs returned by the TikTok API

**System Data:**
- Pipeline run IDs and processing status stored in a private PostgreSQL database
- Asset file paths stored for pipeline coordination

### 2. How We Use Information

The information collected is used solely to:
- Select and adapt Reddit stories into video content
- Generate and upload videos to authorized TikTok accounts
- Track pipeline state to enable resumable, fault-tolerant processing

### 3. Data Storage

- **Reddit content**: Temporarily stored during processing; not retained after video production
- **TikTok tokens**: Stored in local `.env` files on the operator's machine; never transmitted to third parties
- **Pipeline state**: Stored in a private PostgreSQL instance (Neon) accessible only to the operator
- **Generated assets**: Stored in a private Google Cloud Storage bucket accessible only to the operator

### 4. Data Sharing

We do not sell, trade, or share any collected data with third parties. Data is processed solely within the operator's own infrastructure (GCP, Neon PostgreSQL).

### 5. Third-Party Services

The App integrates with the following third-party services, each governed by their own privacy policies:

- **Reddit API**: [Reddit Privacy Policy](https://www.reddit.com/policies/privacy-policy)
- **TikTok API**: [TikTok Privacy Policy](https://www.tiktok.com/legal/privacy-policy)
- **Google Cloud Platform**: [Google Privacy Policy](https://policies.google.com/privacy)
- **Anthropic (Claude AI via Vertex AI)**: [Anthropic Privacy Policy](https://www.anthropic.com/privacy)

### 6. Data Retention

- Processed Reddit content is not retained beyond the video production pipeline
- Pipeline state records are retained for operational purposes and may be deleted by the operator at any time
- Generated video assets are retained in GCS until manually deleted by the operator

### 7. Security

We implement reasonable security measures including:
- Environment variable–based secret management (no hardcoded credentials)
- Private database and storage access with authenticated service accounts
- Non-root container execution in production deployments

### 8. Your Rights

As this application operates on publicly available Reddit content and posts to operator-controlled TikTok accounts, end-user data rights are governed by Reddit's and TikTok's respective policies.

### 9. Changes to This Policy

We may update this Privacy Policy periodically. The "Last updated" date at the top of this page indicates when changes were last made.

### 10. Contact

For privacy-related questions or concerns, please open an issue in this repository.
