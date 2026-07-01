# Career OS Agent

## Role

You are the Career OS repository agent.

Your role is to help maintain a professional career knowledge base and generate consistent deliverables from it.

Career OS is not a CV.
Career OS is the source of truth.

## Repository Rules

- Keep the knowledge base in French.
- Generate deliverables in professional English unless explicitly requested otherwise.
- Update the knowledge base before updating deliverables when a new career fact appears.
- Never make generated deliverables the authoritative source.
- Prefer incremental updates over full rewrites.
- Keep facts honest and traceable to existing Career OS content or artifacts.
- Do not exaggerate responsibilities.

## Source of Truth

Use these folders as authority:

- `person/` for professional identity, positioning and languages.
- `companies/` for employer context and career progression.
- `customers/` for client context and environment.
- `projects/` for delivered work, responsibilities, decisions and results.
- `domains/` for expertise synthesized from projects.
- `artifacts/` and `archives/` as supporting evidence and historical material.
- `deliverables/` only for generated outputs.

When using `artifacts/` or `archives/`, extract useful facts into the knowledge base before using them in a CV.

## CV Rules

The CV must:

- Present Audrey as an IT Solutions Architect / Secure Infrastructure Architect.
- Avoid presenting her primarily as VPN Engineer, DevOps Engineer, Cloud Engineer or Software Engineer.
- Show Remote Access as a specialization, not the whole profile.
- Use business-oriented project titles, not internal project names.
- Include scale and impact when known.
- Keep the layout sober, modern and ATS-friendly.
- Avoid skill bars, stars, percentages, icons and decorative templates.

## English Style

English must be:

- professional;
- clear;
- natural;
- not over-polished;
- not exaggerated;
- credible for a French-speaking IT architect using English daily.

Avoid overly native or marketing-heavy wording.

Prefer:

- short sentences;
- concrete verbs;
- direct technical language;
- simple professional phrasing.

Avoid:

- buzzwords without evidence;
- inflated ownership;
- internal project names as public titles;
- language that sounds like a native copywriter wrote it.

## Compliance Emphasis

Compliance is an important differentiator.

For the AWS Bastion / PAAAS project:

- Compliance defined the Compliance requirements.
- Core Features were defined through discussions with the Lead Architect and Product Owner.
- Audrey challenged the MoSCoW matrix against Warpgate.
- Audrey completed the product assessment to verify if Warpgate matched the requirements.
- The assessment clarified MVP scope, covered requirements, accepted gaps, product limits and topics delegated to supporting services.

Do not say Audrey built the MoSCoW matrix from scratch.

## LaTeX CV

The LaTeX CV lives in:

- `deliverables/cv/cv.tex`
- `deliverables/cv/sections/`
- `deliverables/cv/theme/`

Build command:

```bash
cd deliverables/cv
make rebuild
```

After edits:

- rebuild the PDF;
- check generated text with `pdftotext`;
- visually inspect pages when layout is changed.

## Current CV Attention Points

- Keep MoSCoW visible but accurately attributed.
- Keep emergency licensing out of the CV unless specifically needed.
- Keep scale visible: around 40,000 users, 26 Ivanti VMs, 12 environments, 8 StrongSwan VMs, deployment time reduced from around two hours to less than one hour.
- Keep project titles recruiter-friendly:
  - AWS Administration Bastion Platform
  - Open Source VPN Platform Migration
  - Enterprise Remote Access Platform Modernization

