# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a collection of custom user patterns for [Fabric](https://github.com/danielmiessler/Fabric), a framework for working with AI prompts. Each pattern is a specialized prompt that can be invoked via the `fabric` CLI tool.

## Repository Structure

Patterns are organized as individual directories, each containing a `system.md` file that defines the prompt:

```
user_patterns/
├── pattern_name/
│   └── system.md          # The prompt definition
├── another_pattern/
│   └── system.md
└── README.md
```

## Pattern File Format

Each `system.md` file contains:
- The complete system prompt that will be sent to the AI
- Instructions for how to process user input
- Expected output format specifications
- Examples demonstrating the pattern's behavior

The `system.md` file is written from the perspective of instructing an AI assistant ("You are...", "When I give you...").

## Using Patterns with Fabric

Patterns can be invoked via the Fabric CLI:
```bash
fabric --pattern pattern_name
```

User input is typically piped to the pattern or provided after invocation.

## Current Patterns

- **hacky_carky**: Czech diacritic correction tool that adds missing háčky and čárky while preserving formatting
- **number_mnemonic**: English Major System mnemonic generator for converting numbers to memorable words/phrases
- **ciselna_mnemotechnika**: Czech version of the Major System mnemonic generator with Czech consonant mappings

## Creating New Patterns

1. Create a new directory with the pattern name (use lowercase, underscores for spaces, no diacritics)
2. Create `system.md` inside the directory
3. Write the prompt from the AI's perspective
4. Include clear input/output format specifications
5. Add examples showing expected behavior

## Language Considerations

Patterns can be in any language. For Czech patterns:
- Use standard Czech grammar and vocabulary in the prompt text
- For directory names, use ASCII-only characters (no háčky/čárky)
- Document any phonetic mappings or special character handling clearly
