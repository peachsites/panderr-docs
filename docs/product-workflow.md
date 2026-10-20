# Panderr Product Workflow

Panderr is designed around a simple idea: an existing website should be reusable as an asset rather than treated as something that must always be rebuilt from scratch.

## 1. Import or capture

A migration can begin from an existing website or other supported source material. Panderr gathers the available site structure, content, navigation, images, and business information needed for the next step.

## 2. Understand the existing site

Panderr organizes what it finds into a normalized representation of the website so that content, structure, and design decisions can be handled separately.

This separation allows the platform to support multiple outcomes from the same source website.

## 3. Choose the transformation path

### Preserve

Preserve prioritizes fidelity. It is intended for migrations where the customer wants the existing website to remain recognizable and substantially unchanged after moving.

### Improve

Improve keeps the site's identity and core content while allowing Panderr to modernize presentation, structure, usability, and technical implementation.

### Redesign

Redesign treats the existing website as source material. Content, branding, and business information are retained as inputs while Panderr applies a stronger composition and design system.

## 4. Review in Panderr Studio

Panderr Studio is the editing workspace. It brings together website pages and project-level controls in one interface.

Current product areas include:

- Pages
- Design
- Settings
- Preview
- Publish

Project-level design controls can include colors, fonts, buttons, layout and spacing, header and footer behavior, and shared business information.

## 5. Save and preview

Changes are stored as part of the website project so users can move between pages, preview the site, and continue editing without losing project-level settings.

## 6. Publish

The finished website can be published to a Panderr-managed Cloudflare Pages address through Panderr's Cloudflare-backed workflow, or downloaded as website files the customer can upload to any hosting provider. Customers can use their own domain with Panderr Cloud by requesting nameserver and DNS setup information from Panderr and updating their settings with their domain provider; setup is manual, and automated self-service domain connection is not yet implemented.

```text
Import → Understand → Transform → Edit → Preview → Publish
```

## Availability and pricing (public summary)

- **Preview:** Panderr generates a free preview of an existing website's design and content — a generated recreation that shows what Panderr can recreate. No account is needed to view a preview; a free account is required to keep or edit a project. The preview does not verify SEO preservation, redirects, or complete functionality.
- **Website purchase:** $99 one-time for one website project, including 30 days of Studio editing access and website export.
- **Studio (ongoing editing):** $99/year. **Panderr Cloud Hosting:** $29/month or $290/year. Studio and hosting are independent; neither is required to keep a purchased website. New Studio and hosting subscriptions are temporarily unavailable.
- **Publishing:** publish to a Panderr-managed Cloudflare Pages address, or download the website files and host anywhere. Own-domain connection with Panderr Cloud is a manual, guided process (nameserver/DNS information provided on request); automated connection inside Panderr is not yet implemented.
- **Starting points:** migrations can begin at panderr.com, from the WordPress plugin, in ChatGPT, or in Claude (see Integrations & Partnerships). Connectors return a link that starts the process; previewing, editing, purchasing, and publishing happen in Panderr.

The specific implementation behind each stage is proprietary and is not included in this public documentation repository.
