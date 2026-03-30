# Dean Lab Resources Handbook Design

## Goal

Turn the existing `Lab Resources` area of the Sphinx site into a public-facing, wiki-like handbook for lab members, using the current Word handbook as the source while removing funding-account specifics and other budget-code details.

## Approved Constraints

- Keep the work inside the existing Sphinx reStructuredText site.
- Use `Lab Resources` as the handbook entry point.
- Omit funding-account specifics.
- Keep practical workflows, room numbers, shipping instructions, and access procedures when they are useful to lab members.
- Update meeting information:
  - Whole-team meeting: Mondays at 1:00 PM
  - No focus group meetings
  - Dean Lab meeting: Mondays at 3:00 PM

## Information Architecture

The `Lab Resources` landing page becomes a short hub page with links to focused handbook pages:

- `onboarding`
- `policies`
- `meetings`
- `digital-tools`
- `working-at-utsw`
- `data-management`
- `equipment`
- `protocols`
- `departure`

## Content Boundaries

- `onboarding`: first-week setup, key contacts, access checklist, required systems
- `policies`: stable lab expectations and links to subpages
- `meetings`: recurring meetings, attendance expectations, presentation formats
- `digital-tools`: email, Slack, Outlook, GitHub, LabArchives, BioHPC, work computers
- `working-at-utsw`: institutional logistics, HR/IR, badge access, VPN, shipping, travel, training, benefits, IP
- `data-management`: storage expectations plus microscopy image-display guidance
- `departure`: offboarding and notice expectations

## Compatibility Decisions

- Keep `equipment` and `protocols` as standalone resource pages.
- Leave compatibility pages for legacy policy URLs that now point readers to the new top-level pages.
- Avoid "internal only" framing because this site is intended to be public-facing.

