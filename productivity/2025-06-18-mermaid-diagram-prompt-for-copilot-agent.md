# Creating Standard Mermaid Diagram Prompt for Copilot Agent

**Date:** 2025-06-18
**Category:** productivity

> 🇯🇵 [日本語版はこちら](./2025-06-18-mermaid-diagram-prompt-for-copilot-agent.ja.md)

## What I optimized

I created a standardized prompt for generating Mermaid diagrams through Copilot Agent, specifically designed for documentation repositories. This optimization addresses the challenge of creating consistent, theme-aware diagrams that work well in both light and dark modes.

## How I did it

1. **Transitioned from Wiki to Repository-based Documentation**
   - Moved away from traditional wiki systems to leverage Copilot Agent's capabilities
   - Set up a repository structure that allows for better prompt integration

2. **Developed Theme-Aware Diagram Generation**
   - Initially attempted to create a single diagram that works for both light and dark modes
   - Discovered this approach was complex and less effective
   - Pivoted to generating separate diagrams optimized for each theme

3. **Created Standardized Prompt Structure**
   - Designed prompts that consistently generate appropriate Mermaid syntax
   - Incorporated theme-specific styling and color schemes
   - Ensured diagrams maintain readability across different viewing environments

4. **Implemented Dual-Output System**
   - Script generates two versions of each diagram: light mode and dark mode
   - Each version is optimized for its respective theme
   - Maintains consistency in structure while adapting visual elements

## Impact

- **Improved Documentation Quality**: Diagrams are now consistently formatted and theme-appropriate
- **Enhanced Readability**: Users get optimal viewing experience regardless of their preferred theme
- **Reduced Manual Work**: Automated diagram generation eliminates repetitive formatting tasks
- **Better Copilot Integration**: Leverages AI capabilities more effectively than traditional wiki systems
- **Scalable Process**: Standardized prompts ensure consistent output across different documentation projects

## Lessons learned

- **Theme Complexity**: Attempting to create universal diagrams for both themes proved more challenging than creating separate, optimized versions
- **Tool Selection Matters**: Moving from wiki to repository-based documentation unlocked better AI integration possibilities
- **Standardization Benefits**: Having consistent prompt templates significantly improves output quality and reduces iteration time
- **Separation of Concerns**: Handling light and dark modes separately allows for better optimization of each variant
- **AI Tool Evolution**: Copilot Agent provides more sophisticated capabilities than traditional documentation tools when properly leveraged
