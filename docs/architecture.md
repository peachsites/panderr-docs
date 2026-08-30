# High-Level Architecture

This document intentionally describes Panderr at a high level. It is meant for partners, reviewers, and technical evaluators who need to understand the product model without exposing private implementation details.

## System model

Panderr separates website migration into distinct layers so that importing a website, understanding it, deciding how it should change, editing it, and publishing it are not treated as one monolithic operation.

```text
Source Website
     ↓
Inspection / Capture
     ↓
Normalized Website Model
     ↓
Transformation Decisions
     ↓
Rendered Website
     ↓
Panderr Studio
     ↓
Publishing Pipeline
```

## Core layers

### Inspection and capture

The inspection layer gathers the website information required to understand the source property, such as navigational structure, page content, images, headings, and other available site signals.

### Normalized website model

Captured information is normalized so Panderr can reason about the website independently of the source platform's implementation details.

This supports the distinction between preserving an existing website and redesigning it.

### Transformation layer

Panderr applies one of three product intents:

- Preserve
- Improve
- Redesign

The transformation layer determines how closely the output should follow the original site versus how much composition and modernization should be introduced.

### Presentation and editing

The website is rendered into an editable project that can be reviewed in Panderr Studio. Studio exposes user-facing controls while keeping the underlying editing and project model abstracted from the customer.

### Publishing

Panderr prepares the final website for publishing through its deployment workflow. Cloudflare infrastructure is used across the Panderr application and deployment stack.

## Project-level design model

Panderr supports shared design and site settings so common changes do not have to be repeated manually across every page. Examples include:

- brand colors
- fonts
- buttons
- layout and spacing
- header and footer settings
- business information

## Architecture principles

Panderr's architecture is guided by a few product principles:

1. **Migration fidelity and redesign should be separate concerns.** A user who wants to preserve a website should not be forced through a template-first redesign path.
2. **Project data should remain portable across the editing and publishing workflow.**
3. **The editing experience belongs to Panderr.** Underlying implementation tools should not dictate the customer-facing workflow.
4. **Publishing should be a continuation of the migration process, not a separate technical project for the customer.**

## What is intentionally not public

This repository does not document internal APIs, proprietary migration heuristics, project schemas, authentication architecture, infrastructure credentials, security controls, or source code for Panderr's production application.
