---
name: deep-research-synthesis
description: An autonomous agentic skill for executing deep, multi-step research on complex topics. It combines iterative planning, broad and deep information gathering, and long-context synthesis to produce citation-rich, professional reports.
---

# Deep Research Synthesis Skill Instructions

This skill transforms the agent into a "Lead Researcher" capable of handling ambiguous, high-level queries by breaking them down, gathering vast amounts of information, and synthesizing it into a cohesive output.

## Core Philosophy
*   **Plan First:** Never start searching blindly. Understand the "Why" and "What" before the "How".
*   **Context is King:** Leverage the large context window. Prefer reading full documents/pages over short snippets whenever possible.
*   **Citation is Mandatory:** Every claim must be grounded. Hallucination is the enemy.

## Workflow Stages

### Phase 1: Clarification & Planning (The "Interactive Planner")
1.  **Analyze the Request:** Identify the user's core intent. Is it a market analysis, a technical deep dive, or a comparative study?
2.  **Ambiguity Check:** If the request is too vague (e.g., "Analyze AI"), **STOP** and ask 3-5 specific clarifying questions (e.g., "Which specific sector?", "What is the time horizon?", "Technical or Business focus?").
3.  **Generate Outline:** Once clarified, create a structured **Research Outline**. This acts as the "map" for the investigation.
    *   *Output:* A hierarchical list of sections and sub-sections to be researched.

### Phase 2: Execution (The "Research Loop")
For each section in the Outline, execute the following loop:
1.  **Formulate Queries:** Generate specific, targeted search queries. Avoid generic terms. Use advanced operators (e.g., `site:`, `filetype:pdf`) if supported/needed.
2.  **Broad Scan:** Use `google_web_search` to find high-quality sources.
3.  **Deep Dive (The "Context Loader"):**
    *   Identify high-value URLs from the scan.
    *   Use `web_fetch` (or `read_file` for local docs) to ingest the **FULL content** of these sources.
    *   *Crucial:* Do not just summarize immediately. Store the raw content (or detailed extracts) in the context window to allow for cross-reference later.
4.  **Self-Correction:** Check if the gathered info actually answers the section's questions.
    *   *If Yes:* Proceed.
    *   *If No:* Refine the search queries and repeat (up to 3 iterations per section).

### Phase 3: Synthesis & Reporting (The "Writer")
1.  **Global Analysis:** Review *all* gathered context across all sections. Look for patterns, contradictions, or connections that weren't visible in individual searches.
2.  **Drafting:** Write the report section by section.
    *   **Style:** Professional, objective, dense (high information-to-word ratio).
    *   **Structure:** Executive Summary -> Methodology -> Detailed Analysis -> Risks/Opportunities -> Conclusion.
3.  **Strict Grounding:**
    *   Append a `[Source: URL/Title]` citation to every specific claim or data point.
    *   Create a "References" section at the end.

## Tools Strategy
*   **`google_web_search`**: For discovery and fact-checking.
*   **`web_fetch`**: For deep reading of identified articles/reports.
*   **`read_file`**: For incorporating local user files (PDFs, Excel) into the research.

## Usage Example
> User: "Analyze the impact of solid-state batteries on the EV market by 2030."
>
> **Agent Action:**
> 1.  **Plan:** Define "Solid-state tech maturity", "Key players (Toyota, QuantumScape)", "Cost projections", "Market adoption rates".
> 2.  **Search:** Query "solid-state battery roadmap 2030", "solid-state battery cost analysis 2025".
> 3.  **Fetch:** Read full reports from McKinsey, BloombergNEF summaries, or technical papers found.
> 4.  **Synthesize:** Produce a report comparing different chemistry paths and their specific timeline impacts.
