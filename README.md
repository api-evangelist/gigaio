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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
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
