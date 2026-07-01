# AI_HANDOVER.md

> **Purpose**
>
> This document allows any AI assistant (Codex, ChatGPT, Claude, Gemini, etc.) to immediately understand the Career OS project, its philosophy, its architecture and the current state of the work without reading previous conversations.

---

# Project Overview

## Name

Career OS

## Goal

Career OS is a personal knowledge base describing my professional career.

It is **not** a CV.

It is the **single source of truth** from which every professional deliverable is generated.

Examples:

- CV
- LinkedIn profile
- Cover letters
- Professional biography
- Interview preparation
- Technical portfolio
- Career timeline

Deliverables are generated artifacts.

Career OS remains the only source of truth.

---

# Guiding Principles

## Single Source of Truth

Information must exist only once.

Generated documents must never become authoritative.

Always update Career OS first.

---

## Single Responsibility

Every folder answers one question.

### person/

Who am I professionally?

Contains:

- professional identity
- positioning
- objectives
- languages

Does NOT contain:

- projects
- technologies
- employer history

---

### companies/

Who employed me?

Contains:

- employer
- career progression
- overall responsibilities
- context

Does NOT describe projects.

---

### customers/

For whom did I work?

Contains:

- customer context
- organization
- business constraints
- stakeholders
- teams

Does NOT describe implementations.

---

### projects/

What have I delivered?

Contains:

- context
- problem
- architecture
- decisions
- implementation
- responsibilities
- impact
- lessons learned

Projects are the primary source for CV generation.

---

### domains/

What do I know?

Contains:

- concepts
- technologies
- methodologies
- platforms
- protocols

Knowledge only.

No storytelling.

---

### deliverables/

Generated artifacts.

Examples:

- CV
- LinkedIn
- Portfolio
- Biography

Never edit manually unless the goal is formatting.

---

# Current Professional Positioning

## Current Title

IT Solutions Architect

---

## Positioning

The profile should be presented as:

- IT Solutions Architect
- Secure Infrastructure Architect
- Infrastructure Architect
- Solution Architect

Never position the profile primarily as:

- VPN Engineer
- DevOps Engineer
- Cloud Engineer

Remote Access is a specialization.

Secure Infrastructure is the overall positioning.

---

# Career Summary

Current employer:

NTT DATA

Historical progression:

Dimension Data

↓

NTT Ltd.

↓

NTT DATA

Customer:

European Commission

Duration:

Nearly 10 years

Career evolution:

Network Security Engineer

↓

Primary / Technical Reference (Remote Access)

↓

IT Solutions Architect

Official architect title since 2024.

Architecture responsibilities started earlier.

---

# Engineering Background

This is a key differentiator.

Do NOT reduce the profile to Remote Access.

The architecture experience is built upon several years of operational Network Security.

Main operational domains:

- Firewalling
- Reverse Proxy
- Proxy
- DNS
- Load Balancing
- WAF
- Remote Access

The candidate continued supporting these technologies even after specializing in Remote Access.

This operational background explains today's architectural decisions.

---

# Main Areas of Expertise

Current specialization:

- Secure Infrastructure
- Remote Access
- Infrastructure Automation
- DevSecOps
- Open Source Infrastructure
- AWS Administration Platforms

Strong engineering knowledge:

- Linux
- Windows
- VMware
- PKI
- DNS
- Load Balancing
- Network Security

Programming remains a supporting skill.

The profile is NOT a Software Engineer.

---

# Technical Stack

## Infrastructure

- Linux
- Windows
- macOS
- VMware
- AWS

---

## Network Security

- Cisco ASA
- Pulse Secure
- Ivanti Connect Secure
- StrongSwan
- Warpgate

---

## Automation

- Ansible
- AWX
- GitLab CI/CD
- Node-RED

---

## Development

- Python
- Go
- Bash

Development exists to automate infrastructure.

---

# Design Principles

The following principles repeatedly appear throughout the career.

They should naturally emerge in generated documents.

- Automation
- Standardization
- Simplicity
- Open Source
- Compliance
- Security by Design
- Compliance by Design
- Documentation
- Maintainability
- Pragmatism

These principles describe the architect's mindset.

---

# Main Projects

Career OS keeps internal names.

Generated CVs should use business-oriented titles.

---

## Enterprise Remote Access Platform Modernization

Internal name:

Remote Access Platform Evolution

Purpose:

Modernization of the historical VPN platform.

Main topics:

- virtualization
- capacity planning
- automation
- security hardening
- compliance
- segregation
- documentation

---

## Migration to an Open Source Remote Access Platform

Internal name:

Pulse Away

Purpose:

Replace Pulse Secure IPsec because of licensing costs and recurring security vulnerabilities.

Technology:

StrongSwan

Main topics:

- architecture
- NetBox
- AWX
- GitLab
- CI/CD
- migration
- automation

---

## AWS Privileged Access Platform

Internal names:

AWS Bastion Platform

PAAAS

Purpose:

Secure privileged SSH access to AWS environments.

Main topics:

- Warpgate
- Vault
- AWS
- automation
- compliance
- CI/CD
- Go
- Prometheus exporter

---

# CV Generation Rules

The CV should tell one story.

Network Security Engineer

↓

Technical Reference

↓

IT Solutions Architect

Avoid technology-driven storytelling.

Prefer achievement-driven storytelling.

Every project should explain:

- Business problem
- Architectural solution
- Responsibilities
- Impact
- Technologies

in this order.

---

# Project Naming Rules

Never expose internal project names as primary titles.

Prefer:

Enterprise Remote Access Platform Modernization

instead of

Remote Access Platform Evolution

---

Prefer:

Migration to an Open Source Remote Access Platform

instead of

Pulse Away

---

Prefer:

AWS Privileged Access Platform

instead of

PAAAS

Internal names may appear only inside descriptions.

---

# CV Style Guidelines

Target audience:

- Microsoft
- AWS
- Red Hat
- HashiCorp
- Consulting companies
- European Institutions

Tone:

Senior Architect

Professional

Technical

Confident

Never exaggerated.

---

# Layout Guidelines

Preferred:

- clean typography
- white space
- minimalist
- ATS compatible
- modern hierarchy

Avoid:

- skill bars
- stars
- percentages
- unnecessary icons
- Canva-like templates

---

# Reviewer Feedback

Current feedback received:

- descriptions are too short
- more impact is needed
- more measurable results are needed
- add contact information
- project titles should be business-oriented
- internal project names should disappear
- add business context
- explain the reason behind each project
- architecture should appear more clearly
- premium visual design expected

---

# Workflow

When updating Career OS:

1. Update Career OS.
2. Review.
3. Commit.
4. Regenerate deliverables.

Never edit generated documents as the source of truth.

---

# Current Status

Career OS is sufficiently complete to generate:

- CV
- LinkedIn profile
- Biography
- Interview preparation

Future improvements should enrich Career OS rather than generated documents.

---

# Long-Term Vision

Career OS should become a reusable professional operating system capable of generating consistent, high-quality professional documents while preserving a single source of truth.

Any AI assistant should be able to resume work using only this repository and this document.
