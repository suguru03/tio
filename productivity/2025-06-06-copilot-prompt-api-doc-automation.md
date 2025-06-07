# Copilot Prompt for Automatic API Documentation Generation

**Date:** 2025-06-06
**Category:** productivity

> 🇯🇵 [日本語版はこちら](./2025-06-06-copilot-prompt-api-doc-automation.ja.md)

## What I optimized

Created an automated two-script system using Copilot Prompts to keep API documentation up-to-date. When `commit.prompt.md` detects controller changes in git diffs, it automatically triggers `api-doc.prompt.md` to generate documentation updates. This eliminates the manual overhead of maintaining API documentation and ensures docs stay synchronized with code changes.

## How I did it

1. **Created `commit.prompt.md`**: Developed a monitoring script that analyzes git diffs during commit operations to detect controller file changes
2. **Created `api-doc.prompt.md`**: Built a dedicated script responsible for the actual generation and updating of API documentation
3. **Implemented trigger system**: Set up `commit.prompt.md` to automatically execute `api-doc.prompt.md` when controller changes are detected
4. **Integrated into workflow**: Embedded the system into the commit process to ensure documentation updates happen seamlessly alongside code changes

This two-stage system separates concerns between change detection and document generation, creating a maintainable and extensible solution. The `commit.prompt.md` acts as a watcher, while `api-doc.prompt.md` handles the specialized task of generating accurate API documentation.

## Impact

- **Complete automation achieved**: Eliminated all manual API documentation maintenance tasks
- **Real-time synchronization**: Documentation updates happen simultaneously with code changes, maintaining constant accuracy
- **Reduced development friction**: Developers can focus on coding without worrying about documentation overhead
- **Enhanced team productivity**: Consistent, up-to-date documentation reduces confusion and debugging time across the entire development team
- **Improved code review quality**: API changes can be reviewed alongside their documentation, making the impact of changes clearer

## Lessons learned

- **Modular design importance**: Separating functionality allows each script to have a single responsibility, making them easier to maintain
- **Trigger-based automation**: Automation at the right touchpoint (commit time) proves most effective
- **Prompt engineering collaboration**: Connecting multiple prompts enables automation of more complex workflows
- **Developer experience optimization**: Automation that integrates naturally into existing workflows gains the highest adoption
