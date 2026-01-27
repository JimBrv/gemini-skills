---
name: tender-analysis
description: A skill to analyze tender documents (PDF, Word, Image, Excel) and compare them against product specifications, identifying compliance, gaps, and unique selling points.
---

# Tender Analysis Skill Instructions

This skill is designed to act as a specialized sales engineer assistant for analyzing tender documents and comparing them against your own product's capabilities.

When this skill is activated with tender documents and product specifications (in PDF, Word, Image, or Excel formats):

1.  **Preprocessing (Unified Input Format)**:
    *   **Excel Conversion**: If the input is an **Excel file (.xls, .xlsx)**, automatically **convert it to an image format** (e.g., via screenshot or rendering tool) before proceeding with analysis. This ensures consistent visual processing of tables and layouts.

2.  **Extraction**:
    *   Extract detailed technical specifications, requirements, and parameters from the input files (which are now consistently PDF, Word, or Image).
    *   Extract corresponding technical specifications and capabilities from the product documentation.
    *   **Contextual Keyword Analysis**: actively scan for keywords like **"integration" (集成)**, **"expansion" (扩容)**, **"existing system" (现有系统)**, **"upgrade" (升级)**.
    *   **Proof Requirement Analysis**: actively identify requirements for specific evidence, such as **"product screenshots" (产品截图)**, **"third-party test reports" (第三方检测报告)**, or **"stamped documents" (加盖公章)**.

3.  **Comparison Logic(Strict Line-by-Line)**:
    *   Compare each tender requirement against the product's capabilities STRICT line-by-line.
    *   Determine the compliance level for each parameter (e.g., "Fully Compliant", "Partially Compliant", "Non-Compliant", "Exceeds Requirement").
    *   **Project Continuity Risk Assessment**: If "expansion" or "integration" keywords are found, analyze the context to determine if this implies a lock-in by an incumbent vendor. Flag this as a high-risk factor for new entrants.
    *   **Evidence Compliance**: Treat requirements for "screenshots" or "stamps" as *critical* pass/fail criteria. If the product documentation doesn't explicitly provide these, mark them as "Needs Verification" or "Risk".

4.  **Analysis & Classification**:
    *   **Gap Analysis**: Identify specifications where the product fails to meet the tender requirements.
    *   **Unique Features**: Identify "trap" specs (competitor-unique) or your own unique advantages.
    *   **Incumbency Analysis**: Explicitly state if the tender appears to be an expansion of a specific competitor's existing deployment.

5.  **Output Format (Markdown)**:
    *   **Project Context Warning**: Start with a high-level assessment of whether this is a "New Build" or "Expansion/Integration" project and the associated risks.
    *   Generate a structured comparison table or list.
    *   Each entry must include:
        *   **Tender Requirement**: The specific text from the tender.
        *   **Product Capability**: The relevant product spec.
        *   **Compliance Status**: (Satisfied / Missing / Partial / Risk).
        *   **Evidence Requirement**: Note if screenshots/stamps are needed.
        *   **Analysis/Gap**: A brief explanation of the difference or advantage.
        *   **Exclusivity**: Note if a parameter seems designed for a specific competitor or if it highlights your unique strength.
    *   **Interactive Check**: At the end of the response, ask the user: "Would you like me to save this analysis to a local Markdown file? (Yes/No)"

## Usage
Use this skill when the user provides tender documents and product manuals/specs and asks for a compliance matrix, gap analysis, or bid feasibility assessment.
