---
name: ai-security-tracker
description: A specialized skill for tracking and analyzing the latest developments in AI Security, including threats, solutions, startups, and standards.
---

# AI Security Tracker

## Description
A specialized skill for tracking and analyzing the latest developments in AI Security, including threats, solutions, startups, and standards.

## Instructions
When the user asks to "track AI security updates" or "analyze AI security trends", perform the following research and synthesis steps using your `google_web_search` tool.

### Step 1: Recent AI Security Incidents (Last 1 Month)
*   **Goal:** Identify recent security events, attacks, and vulnerabilities in the AI domain.
*   **Actions:**
    *   Search for "AI security incidents last month", "LLM jailbreak attacks recent", "AI model extraction attacks", "data poisoning AI recent".
    *   Search for "CVEs AI libraries [current_month] [current_year]".
    *   Look for news on major AI platforms (OpenAI, Anthropic, Google, Hugging Face) regarding security patches, data leaks, or disclosed vulnerabilities.

### Step 2: Major Vendor AI Security Solutions (Global & China)
*   **Goal:** Summarize latest AI security products from world-class vendors, including Top 5 Chinese vendors.
*   **Actions:**
    *   **Global Leaders:** 
    1. Research major players like Palo Alto Networks, Microsoft Security, Google Cloud Security, CrowdStrike, Zscaler, Cloudflare, Wiz.
    2. What startups they acquired, and why they acquired them.
    3. What new products they released, and what are the key features, with the acquired startup capabilities integration.
    *   **China Top 5 security vendors:** Research latest AI security announcements from Qi An Xin (奇安信), Sangfor (深信服), NSFOCUS (绿盟), Venustech (启明星辰), and Topsec (天融信).
    *   **China Top 3 AI vendors:** Research latest AI security announcements from Alibaba Cloud, Bytedance,Tencent Cloud.
    *   Search keywords: "[Company Name] AI security product", "AI Firewall", "AI-SPM", "LLM Security Solution".

### Step 3: Top 10 AI Security Startups (Categorized)
*   **Goal:** Track progress of leading AI security startups and categorize them by their specific niche.
*   **Actions:**
    *   Identify top global startups (e.g., Protect AI, HiddenLayer, Lakera, TrojAI, CalypsoAI, Cranium, Wittra, Lasso Security, Prompt Security, Grip Security).
    *   **Categorization Requirement:** Group findings into these specific domains:
        1.  **AI Development Security:** (Supply chain, code scanning, model vulnerability scanning)
        2.  **AI Deployment/Cloud Security:** (AI-SPM, Shadow AI discovery, Infrastructure security)
        3.  **AI Runtime/Inference Security:** (Prompt injection defense, Firewall, Real-time monitoring)
        4.  **AI Data Security:** (DLP for AI, Privacy enhancing tech, Data poisoning defense)
        5.  **AI Agents Security:** (Agent authorization, Loop detection, Action control)
    *   Search for their latest funding rounds (Series A/B/C) and product releases in the current year.

### Step 4: Standards and Frameworks (Global & China)
*   **Goal:** Update on AI security architecture, frameworks, and compliance standards (Last 3 months).
*   **Actions:**
    *   **Global:** Check updates from NIST (AI RMF), ISO (ISO/IEC 42001), OWASP (Top 10 Agentic/LLM), CSA (Cloud Security Alliance - AI Safety Initiative).
    *   **China:** Check updates from TC260 (全国信安标委), CAICT (中国信通院), and industry standards regarding "Generative AI Security Standard", "AI Model Risk Assessment".

### Output Format
Present the findings in a comprehensive Markdown report titled "**AI Security Landscape Report - [Date]**". Use the following structure:

1.  **⚠️ Recent Security Incidents & Vulnerabilities (Last 1 Month)**
    *   *Event/Vulnerability Name*
    *   *Date*
    *   *Description*: Brief summary of what happened.
    *   *Impact*: Why it matters.

2.  **🛡️ Major Vendor AI Security Solutions**
    *   **Global Leaders:** (Microsoft, Palo Alto, Google, etc.)
    *   **China Top 5:** (Qi An Xin, Sangfor, etc.)
    *   *Format:* Company | Product/Feature | Strategic Focus

3.  **🚀 Top 10 AI Security Startups (By Category)**
    *   **AI Development Security:** [Startup Name] - [Update]
    *   **AI Deployment/Cloud:** [Startup Name] - [Update]
    *   **AI Runtime/Inference:** [Startup Name] - [Update]
    *   **AI Data Security:** [Startup Name] - [Update]
    *   **AI Agents Security:** [Startup Name] - [Update]

4.  **⚖️ Standards & Frameworks Updates (Last 3 Months)**
    *   **Global (NIST, ISO, CSA):**
    *   **China (TC260, CAICT):**
    *   *Details of Update & Relevance*

## Triggers
*   "Analyze AI security trends"
*   "What's new in AI security?"
*   "AI security tracker"
*   "Report on AI security landscape"