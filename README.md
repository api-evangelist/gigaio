# GigaIO

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

GigaIO is a Carlsbad, California hardware and software company building datacenter-class
computing for the edge. Its current product line is **Gryf** — a carry-on suitcase-sized,
ruggedized, field-serviceable AI supercomputer built from hot-swappable Accelerator,
Compute, Network and Storage sleds — plus **Manticore**. The company was founded around
**FabreX**, a PCIe/CXL composable memory fabric that disaggregates GPUs, FPGAs, NVMe and
DRAM into dynamically composed clusters, managed with DMTF Redfish RESTful APIs and a
FabreX CLI. In April 2026 GigaIO sold its datacenter technology and assets — including
SuperNODE and FabreX — to d-Matrix and refocused on edge AI inferencing.

- https://gigaio.com/

## What GigaIO publishes

GigaIO has **no public developer portal, API reference, or machine-readable
specification**. The API documentation and knowledge base sit behind an Atlassian Jira
Service Management customer portal, and the FabreX CLI page directs readers to
"CONTACT US for details on APIs".

It does, however, run a **remote Model Context Protocol server on its own host** at
`https://gigaio.com/wp-json/mcp/mcp-oauth-server`, protected by OAuth 2.0 with PKCE and
advertised through RFC 8414 and RFC 9728 discovery documents (both captured verbatim in
`well-known/`). The tool list is auth-gated and was not introspected.

| Artifact | What it records |
|---|---|
| `well-known/` | The two OAuth discovery documents GigaIO serves, verbatim, plus every path that 404s |
| `mcp/` | The remote MCP endpoint, its OAuth posture, and why the tool list could not be read |
| `authentication/`, `scopes/` | The OAuth 2.0 profile and the single published scope, `mcp` |
| `conformance/` | RFC 6749/7009/7636/8414/9728 + MCP conformance; DMTF Redfish recorded as claimed-but-unverifiable |
| `lifecycle/` | No status page, no deprecation policy; the d-Matrix divestiture as the lifecycle event |
| `cli/`, `packages/` | A documented-but-unspecified FabreX CLI; zero client libraries in any registry |
| `plans/`, `rate-limits/` | Measured zeros — no pricing page, no published limits |
| `conventions/` | Runtime semantics, mostly honest nulls; reversibility is `na` with the reason stated |
| `llms/` | A generated llms.txt (GigaIO serves none) including a list of what is confirmed absent |
