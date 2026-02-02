# Topic 2 — Licensing & Copyright (Revision Notes)

## What a software license is
- A **legal instrument** that governs the **use** and **redistribution** of software.
- Software (source and object code) is generally copyright‑protected automatically.

## License classifications (big picture)
### Public Domain
- Author relinquishes copyright / licensing requirements.
- “No rights reserved” style.

### Permissive licenses
- Allow wide reuse, including in proprietary products.
- Usually require keeping copyright notice and license text.
- Example characteristics: compatible, low restrictions.

### Copyleft (protective) licenses
- Allow use and modification, but **derivative works must remain open** under the same license.
- Prevents “proprietisation” of derivatives.
- Key risk in mixed‑license projects: copyleft obligations can “infect” distribution terms.

### Non‑commercial licenses
- Restrict usage to **non‑commercial** contexts.

### Dual licensing
- Same software is offered under:
  - an open‑source license (for adoption), and
  - a commercial license (for monetisation / enterprise use).

## Common licenses and key traits
- **MIT**: permissive; allows reuse in proprietary software when notices are retained.
- **X11**: MIT‑like with an added clause restricting use of the copyright holder’s name for advertising.
- **Apache**: permissive; allows modification and distribution with explicit statements about usage rights (and commonly discussed with patent‑related clarity in many contexts).
- **GPL**: copyleft; derivatives must be released under GPL when distributed.

## Creative Commons (conceptual)
Core conditions:
- **BY**: attribution required.
- **SA**: derivatives must use the same license.
- **NC**: non‑commercial only.
- **ND**: no derivative works.
- **CC0**: “No rights reserved” / public domain‑like dedication.

## License compatibility
- Not all licenses can be combined safely.
- Mixing components can create conflicts that make a distribution legally unusable.
- Practical rule: check compatibility before integrating dependencies into a distributed product.

## Compliance and supply chain
- **SPDX**: a standard for expressing license information / software bill of materials (SBOM) to support compliance and supply‑chain security processes.

## Using third‑party assets
- Logos, images, and other assets still require **permission** (license purchase/royalties/explicit rights).
- “It’s on the internet” is not permission.

## Legal/regulatory themes referenced in the materials
- Accessibility requirements: inclusive products and accessible web design principles.
- Data protection: personal data processing obligations can carry major penalties.

## Cases / scenarios style questions
Be prepared to reason about:
- Whether reselling software is allowed when the license prohibits transfer.
- Whether scraping publicly available data is legal if you don’t bypass technical barriers.
- Fair use arguments in “transformative” contexts vs direct competition / substitution.

## Professor revision-style prompt patterns
- Mixed license scenario (e.g., MIT + GPL) and intended proprietary distribution: identify the issue and the safest conclusion.
- Identify which CC term matches a description (BY/SA/NC/ND/CC0).
