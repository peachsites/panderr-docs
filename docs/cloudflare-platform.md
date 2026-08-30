# Cloudflare Platform

Panderr uses Cloudflare infrastructure as part of both the product application and the website publishing workflow.

This document provides a public, high-level overview of that relationship without exposing private infrastructure configuration.

## Why Cloudflare fits Panderr

Panderr is designed to help users move, modernize, edit, and publish websites. That requires infrastructure that can support fast global delivery, application logic, project data, asset storage, and a straightforward publishing path.

Cloudflare's developer platform provides services that align with those needs.

## Current platform usage

Panderr's implementation uses services within the Cloudflare ecosystem, including:

### Cloudflare Pages

Used as part of website deployment and publishing workflows for static and application-backed website output.

### Cloudflare Workers

Used for serverless application logic and API functionality supporting the Panderr application and publishing experience.

### Cloudflare D1

Used for structured application and project-related data where relational storage is appropriate.

### Cloudflare R2

Used for object and asset storage, including website assets that should not be embedded directly into project records.

## Publishing model

At a high level:

```text
Panderr Project
      ↓
Prepare Website Output
      ↓
Assets + Project Data
      ↓
Cloudflare-backed Deployment
      ↓
Published Website
```

The goal is to make publishing feel like the natural final step of website migration rather than a separate infrastructure task for the customer.

## Customer and agency use cases

Cloudflare infrastructure also aligns with Panderr's longer-term support for businesses, web professionals, and agencies managing multiple website projects.

Potential platform capabilities include centralized deployment workflows, custom-domain publishing, project isolation, performance services, and security features supplied by Cloudflare.

## Security and implementation details

Exact infrastructure configuration, account architecture, credentials, internal API routes, deployment automation, and security-sensitive implementation details are intentionally excluded from this public repository.

For product information, visit [panderr.com](https://panderr.com).
