# open-launcher project guide

This document captures the shared purpose, principles, and product context for open-launcher. It is intended to travel with future application repositories. Add application-specific architecture, installation, configuration, and support details in each app's own documentation.

## Purpose

open-launcher is an open-source project creating independent alternatives to software offered by large technology platforms. The project exists to make useful tools that people can inspect, adapt, self-host, and improve in public.

The goal is an ecosystem of practical open-source applications. This is not a claim that every planned product has shipped, shares one technical stack, or has the same readiness. Each app is responsible for describing its real capabilities and requirements.

## Project principles

### Open source by default

Publish application source code, license terms, and contribution paths in the relevant public repository. Be clear about any components or services that are not open source.

### Free to self-host

Self-hosting the open-source software is intended to remain free. Users supply and operate their chosen infrastructure, which can carry separate costs. Hosted offerings may provide another way to use an app, but they must not be presented as necessary to use or self-host its open-source edition.

### User agency and portability

Build toward user control. Product teams should document where data lives, what leaves the user’s environment, how it can be exported or backed up, and what happens when a hosted service or external dependency is unavailable. Do not make privacy, security, or portability guarantees that have not been verified for the specific app.

### Useful, understandable software

Open alternatives should meet everyday needs with clear setup, usable interfaces, and maintainable code. Explain the tradeoffs and current limitations instead of implying feature parity with another product.

### Build in public

Share decisions, releases, and changes through the product’s public repository. Distinguish shipped behavior from plans, prototypes, and ideas.

## Product portfolio and status

The only named planned application currently documented is **open-notion**. This is a working name for an open-source workspace alternative inspired by Notion; replace the working name when a final product name is chosen. The application itself is not included in this repository, and no release or product repository is identified here.

Other applications remain unnamed. Do not create product names, release claims, timelines, or feature descriptions on behalf of the project until they are confirmed by the people building them.

Use status labels consistently:

- **Planned:** an idea or product direction; there may be no usable code yet.
- **In development:** active implementation exists, but the product is not presented as ready for general use.
- **Released:** a public, usable version is available with installation instructions and a license.
- **Maintained:** a released app has an identified support policy and an active maintenance path.

Only use the strongest status that the public repository and release artifacts support. Include a version or release link when calling an app released.

## Product and brand language

- Write the organization name as **open-launcher**: lowercase, with a hyphen.
- Keep product names exactly as their maintainers choose them. Treat `open-notion` as temporary until it is renamed.
- When explaining a product’s inspiration, use neutral language such as “an alternative inspired by [product].” Do not imply affiliation, endorsement, or compatibility unless it is true and documented.
- Describe the project as an independent open-source effort. Avoid unsupported claims about market share, customer use, feature parity, privacy, or security.
- State whether a capability is released, in development, or planned. Do not turn aspirations into product promises.

## Funding and pricing

The project intends to keep self-hosting free. Hosted plans are planned, but no prices, features, limits, regions, support commitments, or launch dates have been set in the project materials reviewed for this guide.

When hosted plans are defined, document them separately from the self-hosted option. Be explicit about what is paid, what remains free, what the user operates, and any limits or data-handling differences. Never publish placeholder prices as real offers.

## Guidance for application repositories

Each application should have its own README as the primary user guide. At minimum, it should explain:

1. What the app does, who it is for, and its current status.
2. Supported platforms and prerequisites.
3. How to install, configure, update, back up, and remove it.
4. Where it stores data, which services it contacts, and how to export user data.
5. Known limitations, security reporting, support status, contribution steps, and license.

Application-specific documentation should reflect the implementation rather than copy generic claims from this guide. Record the actual language, frameworks, services, deployment model, and supported versions in the app repository when known. open-launcher does not currently mandate a shared application stack.

## Contributions and maintenance

Use each app’s own issue tracker and contribution instructions for implementation-specific questions. For project-wide decisions, use the public open-launcher repositories and discussions. Before accepting a new application into the project, confirm its maintainers, repository, license, product status, self-hosting story, and support expectations.

Keep this guide current when the mission, funding commitments, product portfolio, or cross-project policies change. App maintainers should link to this document for shared context and keep their own README focused on helping people use that app.

## Licensing and security

The open-launcher website and project materials repository currently uses the MIT License. Each application repository must include an explicit license of its own; do not assume the materials repository license automatically applies to separate app code.

Every released application should publish a security reporting route and a truthful supported-version policy. Do not copy a generic version table into an app repository. The organization-level `SECURITY.md` should be updated to reflect the actual products and reporting process before it is treated as a release-support commitment.
