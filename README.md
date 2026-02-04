# Gemini CLI Skills

This directory contains specialized skills for the Gemini CLI agent. Each skill is a self-contained module designed to enhance the agent's capabilities in specific domains.

## Available Skills

### 1. [Deep Research Synthesis](./deep-research-synthesis)
**Purpose:** Autonomous, multi-step research on complex topics, combining the reasoning of OpenAI's Deep Research with the citation rigor of Perplexity.
- **Iterative Planning:** Clarifies ambiguous queries and builds a structured research roadmap.
- **Deep Context Loading:** Ingests full documents/webpages rather than short snippets for cross-doc analysis.
- **Strict Grounding:** Produces professional reports with sentence-level citations.

### 2. [PDF and Image Analysis](./pdf-image-analysis)
**Purpose:** Deep analysis of technical documentation, network topologies, and security architecture diagrams.
- **Text & Object Recognition:** Extracts text and identifies visual elements/icons.
- **Hierarchical Description:** Breaks down complex layouts into logical zones (e.g., Enterprise Zone, Internet Zone).
- **Relationship Mapping:** Describes data flow, protection logic, and spatial relationships between components.

### 3. [Tender Analysis](./tender-analysis)
**Purpose:** Specialized assistance for sales engineers to analyze tender documents and perform gap analysis against product specifications.
- **Multi-format Support:** Processes PDF, Word, Images, and Excel (auto-converted to images for visual consistency).
- **Compliance Matrix:** Generates strict line-by-line comparisons between requirements and product capabilities.
- **Risk Assessment:** Identifies "trap" specifications and assesses project continuity risks (e.g., vendor lock-in).
- **Evidence Tracking:** Flags requirements for specific proof like screenshots or third-party reports.

## Installation

You can install these skills using the `gemini skills install` command.

### From Local Directory

If you have this repository cloned locally:

```bash
# Install Deep Research Synthesis
gemini skills install ./gemini-skills/deep-research-synthesis

# Install Tender Analysis
gemini skills install ./gemini-skills/tender-analysis

# Install PDF & Image Analysis
gemini skills install ./gemini-skills/pdf-image-analysis
```

To install specifically for the current workspace (project):
```bash
gemini skills install ./gemini-skills/deep-research-synthesis --scope workspace
```

### From GitHub

You can install skills directly from the remote repository without cloning:

```bash
# Replace <username/repo> with your actual GitHub repository path

# Install Deep Research Synthesis
gemini skills install https://github.com/<username/repo>.git --path gemini-skills/deep-research-synthesis

# Install Tender Analysis
gemini skills install https://github.com/<username/repo>.git --path gemini-skills/tender-analysis

# Install PDF & Image Analysis
gemini skills install https://github.com/<username/repo>.git --path gemini-skills/pdf-image-analysis
```

## Structure of a Skill

Each skill directory typically contains:
- `SKILL.md`: The core instruction set and definitions for the skill.
- (Optional) Supporting scripts or assets required for the skill's operation.

## Usage

Once installed, you can activate a skill by name or by context.

**Example:**
> "Analyze this tender document using the tender-analysis skill."

To view all installed skills:
```bash
gemini skills list
```
