---
name: pdf-image-analysis
description: A skill to analyze PDF and image files, identifying text and objects, and providing detailed descriptions of their relationships, especially for technical diagrams and security architectures.
---

# PDF and Image Analysis Skill Instructions

This skill is designed to process PDF documents and image files to extract and interpret their content, focusing on technical diagrams, network architectures, and complex logical layouts.

When this skill is activated:

1.  **Recognition Phase**:
    *   Identify and extract all visible text present in the file.
    *   Identify objects, visual elements, icons, and structural blocks (e.g., regions, zones, network segments).

2.  **Detailed Description Phase (Hierarchical & Functional)**:
    *   **Structure**: Break down the description by major regions or logical sections (e.g., Enterprise Zone, Internet Zone).
    *   **Nomenclature**: Explicitly list the specific names of every region, sub-region, and individual component/product identified.
    *   **Rich Descriptions**: For each identified component or sub-region, provide a detailed **3-4 sentence description**. 
    *   **Contextual Depth**: Descriptions must be grounded in:
        *   **Location/Zone**: Where it sits in the hierarchy.
        *   **Action/Role**: Its primary defensive or functional role.
        *   **Context & Logic**: How it relates to its neighbors and the overall security/logic posture.
        *   **Traffic Interaction**: Its position in the traffic path (e.g., "inline in the ingress path", "out-of-band monitoring").

3.  **Relationship Mapping Phase**:
    *   **Traffic Flow & Logic**: Describe how data/logic flows between elements (e.g., "Traffic enters via X, is scrubbed by Y, and forwarded to Z").
    *   **Protection & Management**: Identify which components protect or manage others (e.g., "The WAF protects the web server pool," "The management zone controls all edge devices").
    *   **Spatial/Hierarchical**: Describe containment relationships and logical boundaries.

## Usage
Use this skill for deep analysis of technical documentation, especially network topologies, security architecture diagrams, or any complex layout where components' functional relationships and positioning are critical.
