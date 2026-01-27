# Gemini CLI Skills

This directory contains specialized skills for the Gemini CLI agent. Each skill is a self-contained module designed to enhance the agent's capabilities in specific domains.

## Available Skills

### 1. [PDF and Image Analysis](./pdf-image-analysis)
**Purpose:** Deep analysis of technical documentation, network topologies, and security architecture diagrams.
- **Text & Object Recognition:** Extracts text and identifies visual elements/icons.
- **Hierarchical Description:** Breaks down complex layouts into logical zones (e.g., Enterprise Zone, Internet Zone).
- **Relationship Mapping:** Describes data flow, protection logic, and spatial relationships between components.

### 2. [Tender Analysis](./tender-analysis)
**Purpose:** Specialized assistance for sales engineers to analyze tender documents and perform gap analysis against product specifications.
- **Multi-format Support:** Processes PDF, Word, Images, and Excel (auto-converted to images for visual consistency).
- **Compliance Matrix:** Generates strict line-by-line comparisons between requirements and product capabilities.
- **Risk Assessment:** Identifies "trap" specifications and assesses project continuity risks (e.g., vendor lock-in).
- **Evidence Tracking:** Flags requirements for specific proof like screenshots or third-party reports.

## Structure of a Skill

Each skill directory typically contains:
- `SKILL.md`: The core instruction set and definitions for the skill.
- (Optional) Supporting scripts or assets required for the skill's operation.

## Usage

To use a skill, you can ask the Gemini CLI to "Load [skill-name]" or simply provide the relevant files and request the specific analysis (e.g., "Analyze this tender document using the tender-analysis skill").
