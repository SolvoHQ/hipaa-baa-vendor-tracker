# HIPAA BAA Vendor Tracker

An open, cited, date-stamped dataset of whether common AI tools will sign a HIPAA Business Associate Agreement (BAA) and are usable with Protected Health Information (PHI). Every verdict is sourced from the vendor's own BAA, DPA, or compliance documentation and carries the date it was last verified. The goal is a single, honest reference you can check before pasting patient data into a tool that was never cleared for it.

**At a glance (34 tools tracked):** ✅ 1 sign a BAA · 🟡 12 on a qualifying tier / on request · ❌ 21 will not sign or prohibit PHI.

> ### 📍 Canonical, continuously-updated source
> This repository is a periodic snapshot. The full, continuously-updated version — with a detail page per vendor, the underlying policy quotes, and verification history — lives at **[BAA Atlas → AI tools & HIPAA](https://baa-atlas.vercel.app/ai/hipaa)**.
> If a verdict here looks stale, the live page is the source of truth.

## Will it sign a BAA?

| Tool | Vendor | BAA status | PHI-eligible | Tier / plan detail | Last verified | Source |
|------|--------|------------|--------------|--------------------|---------------|--------|
| ChatGPT | OpenAI | 🟡 BAA on enterprise/qualifying tier only | Conditional | BAA available on ChatGPT Enterprise, the API platform, and the new ChatGPT for Healthcare (launched Jan 2026). Free, Plus and Pro consumer plans are excluded and cannot get a BAA. | 2026-06-01 | [vendor policy](https://openai.com/enterprise-privacy/) |
| Claude | Anthropic | 🟡 BAA on enterprise/qualifying tier only | Conditional | A BAA is available on Claude for Enterprise (and commercial/API agreements). Consumer Claude (Free, Pro, Max) is not BAA-covered. | 2026-06-01 | [vendor policy](https://www.anthropic.com/legal/commercial-terms) |
| Google Gemini | Google | ✅ Signs a BAA | Conditional | Gemini for Workspace is a HIPAA-covered service under the Google Workspace BAA. A Workspace admin must accept the BAA in the Admin console; the free consumer Gemini app is not covered. | 2026-06-01 | [vendor policy](https://workspace.google.com/security/ai-privacy/) |
| GitHub Copilot | GitHub (Microsoft) | ❌ Will not sign / prohibits PHI | No | GitHub Copilot is explicitly outside Microsoft's HIPAA BAA scope — it is not a BAA-covered service even on enterprise GitHub plans. | 2026-06-01 | [vendor policy](https://github.com/customer-terms/github-data-protection-agreement) |
| Microsoft 365 Copilot | Microsoft | 🟡 BAA on enterprise/qualifying tier only | Conditional | Covered by Microsoft's HIPAA BAA when run inside an eligible Microsoft 365 enterprise tenant (E3/E5, Business Premium). Consumer and unlicensed add-on tiers are excluded. | 2026-06-01 | [vendor policy](https://learn.microsoft.com/en-us/microsoft-365/copilot/enterprise-data-protection) |
| Notion AI | Notion | 🟡 BAA on enterprise/qualifying tier only | No | Notion signs a BAA only on the Enterprise plan (100+ members), and the Notion AI add-on is explicitly carved out of that BAA — so PHI may never be processed through Notion AI even on an Enterprise BAA. | 2026-06-01 | [vendor policy](https://www.notion.com/help/hipaa) |
| Slack AI | Slack (Salesforce) | 🟡 BAA on enterprise/qualifying tier only | Conditional | Slack signs a BAA only for Enterprise Grid; once configured for HIPAA, PHI may appear in messages and file uploads that Slack AI operates on within Slack's trust boundary, while third-party marketplace apps stay excluded. | 2026-06-01 | [vendor policy](https://slack.com/help/articles/360020685594-Slack-and-HIPAA) |
| Grammarly | Grammarly | 🟡 BAA on enterprise/qualifying tier only | Conditional | Grammarly enters a BAA only on Grammarly Business Enterprise plans with a 100-seat minimum; individual and smaller paid plans are not BAA-eligible and must not handle PHI. | 2026-06-01 | [vendor policy](https://support.grammarly.com/hc/en-us/articles/4403227220237-Is-Grammarly-HIPAA-compliant) |
| Otter.ai | Otter.ai | 🟡 BAA on enterprise/qualifying tier only | Conditional | A BAA is available on Otter Enterprise only. Basic, Pro and Business plans cannot execute a BAA. | 2026-06-01 | [vendor policy](https://otter.ai/privacy-policy) |
| Zoom AI Companion | Zoom | ❌ Will not sign / prohibits PHI | No | Zoom signs a BAA for Meetings, Phone and Team Chat on eligible plans, but AI Companion's generative features (notes, summaries, transcription, chatbot) are excluded from standard BAA coverage and are auto-restricted when a BAA is active. | 2026-06-01 | [vendor policy](https://www.zoom.com/en/trust/legal-compliance/hipaa-ready/) |
| Perplexity AI | Perplexity | ❌ Will not sign / prohibits PHI | No | Perplexity does not sign a BAA — not even on Enterprise Pro. There is no HIPAA-covered Perplexity tier. | 2026-06-01 | [vendor policy](https://www.perplexity.ai/hub/legal/perplexity-enterprise-data-processing-addendum) |
| Microsoft Copilot | Microsoft | ❌ Will not sign / prohibits PHI | No | Consumer Microsoft Copilot (the free / web Copilot) is excluded from Microsoft's HIPAA BAA — only Microsoft 365 enterprise Copilot is covered. | 2026-06-01 | [vendor policy](https://support.microsoft.com/en-us/topic/privacy-faq-for-microsoft-copilot-27b3a435-8dc9-4b55-9a4b-58eeb9647a7f) |
| Grok | xAI | 🟡 BAA on request | Conditional | xAI can sign a BAA for Enterprise customers after a BAA questionnaire, and PHI must be sent only via xAI's ZDR-enabled API; consumer Grok has no BAA. | 2026-06-01 | [vendor policy](https://docs.x.ai/developers/faq/security) |
| Meta AI | Meta | ❌ Will not sign / prohibits PHI | No | Meta does not sign a HIPAA BAA for any of its products, including Meta AI; it is a consumer service not designed for PHI and has faced enforcement over health-data handling. | 2026-06-01 | [vendor policy](https://www.facebook.com/privacy/genai) |
| DeepSeek | DeepSeek | ❌ Will not sign / prohibits PHI | No | DeepSeek publishes no HIPAA BAA and offers no HIPAA-compliant tier; data is stored in the People's Republic of China and the product carries no compliance or transparency guarantees for healthcare use. | 2026-06-01 | [vendor policy](https://cdn.deepseek.com/policies/en-US/deepseek-privacy-policy.html) |
| Mistral Le Chat | Mistral AI | ❌ Will not sign / prohibits PHI | No | Mistral does not publish a HIPAA BAA for Le Chat (including Le Chat Enterprise); a GDPR DPA and API Zero Data Retention exist but are not a BAA. HIPAA-grade use is only attainable by self-hosting the open-weight models yourself. | 2026-06-01 | [vendor policy](https://help.mistral.ai/en/collections/789670-regulatory-compliance-and-certification) |
| Character.AI | Character.AI | ❌ Will not sign / prohibits PHI | No | Character.AI is a consumer entertainment chatbot with no HIPAA BAA and no healthcare/enterprise compliance tier; users are advised not to share sensitive or medical data. | 2026-06-01 | [vendor policy](https://support.character.ai/hc/en-us/articles/39030432883099-Privacy-Policy) |
| Poe | Quora | ❌ Will not sign / prohibits PHI | No | Poe (by Quora) is a consumer multi-model chatbot aggregator with no HIPAA BAA; its privacy policy warns against sharing sensitive information and shares chats with third-party model providers and bot developers. | 2026-06-01 | [vendor policy](https://poe.com/pages/privacy) |
| Cursor | Anysphere | ❌ Will not sign / prohibits PHI | No | Cursor (Anysphere) does not publicly offer a BAA on any plan — Free, Pro, Business or Enterprise — and its terms contain no HIPAA provisions; healthcare teams are directed to contact sales but no BAA is documented. | 2026-06-01 | [vendor policy](https://cursor.com/security) |
| Tabnine | Tabnine | 🟡 BAA on request | Conditional | Tabnine fits HIPAA workflows via its Enterprise self-hosted, VPC, on-prem and air-gapped deployments with zero code retention, where customer code never reaches Tabnine's servers; a BAA is handled through enterprise engagement rather than a self-serve click-through. | 2026-06-01 | [vendor policy](https://docs.tabnine.com/main/welcome/readme/security) |
| Codeium / Windsurf | Codeium | 🟡 BAA on enterprise/qualifying tier only | Conditional | Windsurf/Codeium's security page states it is maintained HIPAA-compliant and will entertain a BAA for significant (enterprise) implementations with zero-data-retention by default on Teams/Enterprise; the standard MSA, however, disclaims that the Offerings meet HIPAA, so a BAA must be separately negotiated. | 2026-06-01 | [vendor policy](https://windsurf.com/security) |
| Replit AI | Replit | ❌ Will not sign / prohibits PHI | No | Replit does not offer a BAA or advertise HIPAA eligibility, and its 2026 Commercial Agreement and DPA add no HIPAA/BAA terms; it also lacks HIPAA controls such as PHI-safe isolation, audit logs and breach alerting. | 2026-06-01 | [vendor policy](https://replit.com/dpa) |
| Amazon Q Developer | Amazon Web Services | ❌ Will not sign / prohibits PHI | No | AWS signs a single BAA covering eligible services, but Amazon Q Developer is NOT on the AWS HIPAA Eligible Services Reference list (only Amazon Q Business is); AWS states Q Developer is not designed to transmit, store or process ePHI. | 2026-06-01 | [vendor policy](https://aws.amazon.com/compliance/hipaa-eligible-services-reference/) |
| Sourcegraph Cody | Sourcegraph | ❌ Will not sign / prohibits PHI | No | Sourcegraph's published compliance program covers SOC 2 Type II, ISO 27001, GDPR and CCPA but lists no HIPAA attestation and offers no BAA; Cody is a developer code-AI product not positioned for PHI. | 2026-06-01 | [vendor policy](https://sourcegraph.com/security) |
| Jasper | Jasper | ❌ Will not sign / prohibits PHI | No | The Jasper marketing platform's security documentation advises against entering protected health information and offers no BAA; the separately-owned, unrelated 'Jasper Health' company is the only Jasper-named entity that signs BAAs. | 2026-06-01 | [vendor policy](https://www.jasper.ai/trust) |
| Copy.ai | Copy.ai | ❌ Will not sign / prohibits PHI | No | Copy.ai is a marketing/GTM writing tool whose public security and trust materials address general data privacy (SOC 2 / GDPR / CCPA style) but contain no HIPAA compliance statement or BAA offering. | 2026-06-01 | [vendor policy](https://www.copy.ai/security) |
| QuillBot | QuillBot (Course Hero/Learneo) | ❌ Will not sign / prohibits PHI | No | QuillBot's Trust Center commits to GDPR, CCPA and PCI DSS but lists no HIPAA compliance or BAA offering; third-party aggregator claims of 'HIPAA compliant' are not corroborated by QuillBot's first-party documentation. | 2026-06-01 | [vendor policy](https://quillbot.com/trust-center) |
| Google NotebookLM | Google | ❌ Will not sign / prohibits PHI | No | NotebookLM is absent from Google Workspace's 'HIPAA Included Functionality' list, so it is not covered by the Google Workspace HIPAA BAA; the free consumer app is likewise out of scope. | 2026-06-01 | [vendor policy](https://workspace.google.com/terms/2015/1/hipaa_functionality/) |
| Midjourney | Midjourney | ❌ Will not sign / prohibits PHI | No | Midjourney is a consumer creative image-generation service with no security/compliance program and no BAA offering on any tier; it does not execute HIPAA BAAs. | 2026-06-01 | [vendor policy](https://docs.midjourney.com/hc/en-us/articles/32083472637453-Privacy-Policy) |
| Adobe Firefly | Adobe | ❌ Will not sign / prohibits PHI | No | Adobe acts as a Business Associate only for designated HIPAA-Ready Services (e.g. Acrobat Sign Enterprise and select Document/Experience Cloud capabilities); Firefly is a creative generative-AI app and is not a HIPAA-Ready Service, so no Firefly BAA is available. | 2026-06-01 | [vendor policy](https://www.adobe.com/trust/compliance/hipaa-hds/hipaa-ready.html) |
| Canva (Magic Studio) | Canva | ❌ Will not sign / prohibits PHI | No | Canva does not sign a BAA on any plan, including Canva Enterprise; its Trust Center offers only GDPR-oriented Data Processing Addendums, not a HIPAA BAA. | 2026-06-01 | [vendor policy](https://www.canva.com/trust/privacy/) |
| ElevenLabs | ElevenLabs | 🟡 BAA on enterprise/qualifying tier only | Conditional | ElevenLabs executes a BAA only for Enterprise subscriptions, which must run a HIPAA-compliant configuration with Zero Retention Mode enabled; customers contact Sales to sign the BAA before handling PHI. | 2026-06-01 | [vendor policy](https://elevenlabs.io/docs/conversational-ai/legal/hipaa) |
| Fireflies.ai | Fireflies.ai | 🟡 BAA on request | Conditional | HIPAA compliance and a BAA are available on request for qualifying (paid) plans, executed via Fireflies' Data Processing Agreement. | 2026-06-01 | [vendor policy](https://fireflies.ai/security) |
| Descript | Descript | ❌ Will not sign / prohibits PHI | No | Descript's published compliance program (security page, SecurityPal trust center) covers SOC 2 Type II, GDPR, CCPA and Privacy by Design but lists no HIPAA attestation and offers no BAA on any plan, including Enterprise. | 2026-06-01 | [vendor policy](https://www.descript.com/security) |

## Status legend

| Symbol | Meaning |
|--------|---------|
| ✅ Signs a BAA | Vendor offers a HIPAA BAA on a generally-available basis. |
| 🟡 BAA on enterprise/qualifying tier only | A BAA exists, but only on an enterprise / qualifying plan (often with seat or tier minimums). |
| 🟡 BAA on request | A BAA is available through sales / a questionnaire, not self-serve. |
| ❌ Will not sign / prohibits PHI | No BAA on any tier, or the product is explicitly carved out of the vendor's BAA. |
| ❓ Unverified | No sourced verdict yet. |

**PHI-eligible** is *Conditional* when PHI is allowed only under specific conditions (a signed BAA, a particular tier, or a ZDR-enabled API) — read the tier/plan detail and the source before relying on it.

## Methodology

- Every verdict is derived from the vendor's **own** BAA, DPA, HIPAA, or compliance documentation (linked in the Source column), not from third-party summaries where a primary source exists.
- Each row is **date-stamped** (`Last verified`). A verdict is only as current as that date — vendors change BAA scope, so re-check the source for anything high-stakes.
- An **unverified** entry never outranks a sourced verdict; we would rather show `❓ Unverified` than guess.
- A BAA covering a vendor's core product does **not** automatically cover its AI add-on. Several tools here (e.g. AI features carved out of an otherwise HIPAA-ready product) are marked ❌ for exactly that reason.
- This is a documentation reference, **not legal advice**. Confirm coverage in your own executed agreement before processing PHI.

## Files

- [`baa-verdicts.csv`](./baa-verdicts.csv) — machine-readable mirror (CSV).
- [`baa-verdicts.json`](./baa-verdicts.json) — machine-readable mirror (JSON).

Both mirrors carry: `tool, vendor, baa_status, phi_eligible, baa_tier_detail, baa_last_verified, source_url`.

## About / disclosure

Maintained by the team behind **[BAA Atlas](https://baa-atlas.vercel.app/ai/hipaa)** (baa-atlas.vercel.app) — an independent tracker of AI-tool HIPAA and data-training posture. This repo is the open-data snapshot; the live site has the per-vendor detail pages and is updated more frequently.

## License

Data in this repository is licensed under **[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)** — you may reuse it with attribution to BAA Atlas (baa-atlas.vercel.app). See [LICENSE](./LICENSE). Any code in this repo is MIT-licensed.
