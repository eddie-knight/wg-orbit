# ORBIT Definitions SIG Parent Charter

A Special Interest Group (SIG) and Technical Initiative of the [OpenSSF ORBIT Working Group](../../CHARTER.md).

- **SIG Lead:** Eddie Knight, Revanite (Interim Only)

## 1. Mission & Technical Scope

The Definitions SIG develops and maintains a portfolio of definition artifacts — specifications, criteria sets, and supporting vocabularies — that open source projects and their consumers can adopt to describe and improve security posture. Artifacts are developed in parallel with a quick decision cycle that captures broad stakeholder input.

**In scope:**

- Development, publication, and maintenance of definition artifacts (see §2), including their criteria, tiers, and supporting definitions
- Documentation, mappings to external frameworks, and Gemara-compliant representations of each artifact
- Guidance for projects adopting the artifacts

**Out of scope:**

- Certification, accreditation, or attestation of specific projects against any artifact
- User-facing software, such as enforcement or scanning tooling

## 2. Artifact Lifecycle

The SIG is organized to collate useful security guidance into clear definitions. These artifacts may be aimed at different processes, roles (e.g. producer vs consumer), or software areas. The SIG must maintain and enforce policies surrounding the lifecycle of all ORBIT Definitions development efforts, published artifacts, and releases.

Every artifact passes through three stages: it begins as a **development effort** (§2.1), becomes a **published artifact** (§2.2), and is then **maintained** until retirement (§2.3).

- A **development effort** is work hosted within the SIG to produce a definition that the SIG has not yet accepted for publication. It is not an official ORBIT Definitions artifact.
- A **published artifact** is a definition the SIG has accepted for publication. It is an official ORBIT Definitions artifact and makes versioned **releases** under §2.2.

A new definition may be proposed from within the group or by a new contributor.

### 2.1 Development Efforts

1. The SIG must maintain and publish a clear process for proposing a new development effort, and clear acceptance criteria that an effort must meet to become a published artifact under §2.2.
2. Development efforts may be initiated under the SIG prior to publication, but must clearly delineate their audience and scope to avoid conflict with other development efforts.
3. Guidance produced by a development effort must be clearly labelled as "draft", must not be presented as final or complete, and must not be announced or publicized as an ORBIT artifact prior to formal SIG acceptance for publication.
4. A list of all ORBIT Definitions development efforts and published artifacts must be prominently displayed in the SIG documentation, with the current stage of each clearly indicated.

> [!IMPORTANT]
> The ORBIT Working Group TSC formally recommends that the SIG seek to limit the number of definitions that it accepts, to reduce maintenance overhead and reader confusion.

### 2.2 Publication & Releases

1. The SIG must maintain a process under which a development effort is evaluated against the acceptance criteria in §2.1.1 and, if accepted, becomes a published artifact. Upon acceptance its stage in the table in §3 is updated, and the ORBIT TSC is notified.
2. The SIG must maintain a process and release criteria for published artifacts to make official releases.
3. Any release that has not met the release criteria must be clearly marked as a pre-release asset.
4. The SIG must maintain shared release tools that are used by all similar or related artifacts.
5. Where relevant, the SIG must ensure that development efforts and published artifacts utilize cross-referencing, mapping, extension, or inheritance.

### 2.3 Maintenance & Retirement

1. Published artifacts are maintained by their designated maintainers (§3) under the delegated autonomy in §4.
2. The SIG must provide a mechanism for the public to understand the usability of each published artifact, and the relationship between different artifacts under the SIG.
3. Outdated, archived, or superseded artifacts must clearly present their current state in the source repository and, where possible, other release and distribution assets.
4. Artifacts that are no longer receiving updates must have this stated prominently in any references where it is possible to do so.

## 3. Maintainers & Contributor Ladder

The SIG supports multiple development efforts in parallel. Maintainership is assigned **per development effort** from the effort's inception and carries through publication: each effort has its own designated maintainers, and maintainer status on one effort confers no authority over another. The SIG Lead coordinates across efforts but does not override effort-level decisions except through the escalation path in §4.4.

| Effort | Stage | Repository | Maintainers |
|--------|-------|------------|-------------|
| Open Source Project Security Baseline (OSPS Baseline) | Published | [`ossf/security-baseline`](https://github.com/ossf/security-baseline) | [list](https://github.com/ossf/security-baseline/blob/main/governance/MAINTAINERS.md) |

New development efforts are adopted into this table by decision of the SIG under §2.1, with notice to the ORBIT TSC. An effort's stage is updated when it is accepted for publication under §2.2.

### 3.1 Contributor Ladder

1. The SIG is responsible for defining roles and appointment processes in the form of a contributor ladder.
2. All roles must have enforceable start and end dates, with terms of no more than 1 year, ensuring that other community members have ample opportunity to advance on a contributor ladder.
3. When three or more maintainers are active in the SIG, all decisions must follow a documented decision-making process.

## 4. Governance

The Definitions SIG is subject to the general OpenSSF and ORBIT Working Group policies. Within those policies (enumerated below), the maintainers of each development effort or published artifact are expressly authorized to self-govern it, including:

- **Decision-making:** internal processes such as lazy consensus and 51% maintainer-consensus with a ~2-business-day review window (66% for local governance revisions)
- **Contributor ladder:** maintainer nomination criteria (e.g., sustained contribution or committee sponsorship), roles, and emeritus policies for that artifact
- **Releases:** cadence and versioning of artifact editions, within the release criteria in §2.2
- **Operations:** repository layout, review requirements beyond the WG minimum, meeting cadence, and creation of sub-project repositories within the scope of §1 (with notice to the ORBIT TSC)

Local governance must be published in the artifact's repositories, and must include the following non-negotiable OpenSSF and ORBIT WG policies (by reference). Local governance may not override the parent WG policies.

### 4.1 Code of Conduct

All participants are subject to the [OpenSSF Code of Conduct](https://openssf.org/community/code-of-conduct/). Maintainers must address reported violations promptly; reports involving a maintainer are escalated past that maintainer. Unresolved or serious incidents escalate to the ORBIT TSC Chair and, where appropriate, the OpenSSF CoC reporting process.

### 4.2 Intellectual Property & Licensing

Per WG charter §7: all inbound and outbound code is licensed **Apache-2.0**; prose is **CC-BY-4.0**; data is **CDLA-Permissive-1.0**. Every commit must carry a **Developer Certificate of Origin sign-off** (`git commit -s`). Files should carry SPDX identifiers. License exceptions require WG-charter-level approval and may not be granted locally.

### 4.3 Supremacy Clause

This charter, and the ORBIT WG charter above it, take precedence over all local Definitions SIG governance documents. Where a local policy conflicts with this charter, this charter governs and the local policy is void to the extent of the conflict.

### 4.4 Escalation Path

1. Artifact maintainers attempt resolution under local governance (including lazy consensus and formal votes).
2. Unresolved maintainer deadlocks go to the SIG Lead. **While the Lead position is vacant, this step is skipped and escalation proceeds directly to step 3.**
3. Any maintainer may escalate to the **ORBIT TSC Chair**; the TSC may decide the matter per WG charter §4.
4. TSC deadlocks may be referred to the OpenSSF TAC per WG charter §4.f.

### 4.5 Sub-Project Inheritance Header

Each Definitions SIG sub-project must include the following block at the top of its local `GOVERNANCE.md`:

```markdown
> **Governance Notice:** This repository is a sub-project of the **ORBIT Definitions SIG**,
> a SIG and Technical Initiative of the
> [OpenSSF ORBIT Working Group](https://github.com/ossf/wg-orbit/blob/main/CHARTER.md),
> and is governed by the [Definitions SIG Parent Charter](https://github.com/ossf/wg-orbit/blob/main/technical-initiatives/sigs/definitions-sig-charter.md).
> The Parent Charter's non-negotiable guardrails — the OpenSSF Code of Conduct,
> Apache-2.0/DCO licensing compliance, and escalation of unresolved disputes to the
> ORBIT TSC — apply here. In any conflict between this document and the Parent
> Charter, the Parent Charter prevails; all other matters are governed locally below.
```
