# Post-Quantum Crypto Map

Compare where crypto projects use post-quantum cryptography: transaction signing, optional accounts, spending locks and validity proofs.

**[Browse the projects](docs/projects.md)** · **[Compare signature sizes](docs/signature-sizes.md)** · **[Download CSV](data/projects.csv)** · **[Report a correction](https://github.com/Balance0014/post-quantum-crypto-map/issues/new/choose)**

The dataset covers 17 projects, with deployment milestones, consensus mechanisms, signing schemes, upgrade options and source links. It grew out of two maps I published on X. I'm opening the data so people can check the claims, reuse the work and help keep it accurate.

**Snapshot: October 23, 2026. First open-data release: October 28, 2026.** These are the data behind the dated charts below. [Release-day checks](docs/release-review.md) are listed separately; this is not a live feed or a security ranking.

Maintained by **Balance Zhao · [@balance0014](https://x.com/balance0014)**. [中文说明](README.zh-CN.md)

## Start here

| If you want to… | Open… |
| --- | --- |
| See what each project has deployed, and what remains optional or experimental | [Project comparison](docs/projects.md) |
| Check a claim against its source | The source links under each [project entry](docs/projects.md) |
| Compare public-key and signature sizes | [Reference sizes and encoding notes](docs/signature-sizes.md) |
| Build your own table or visualization | [Projects JSON](data/projects.json), [sizes JSON](data/signature-sizes.json), or the CSV files in [data/](data/) |
| Add a project or correct a detail | [Contribution guide](CONTRIBUTING.md) |

## The two maps

### Deployment timeline

The year marks the milestone written on each card. It may be a chain launch, a later cryptographic upgrade or a public testnet announcement. It does **not** mean every feature on that card existed in that year.

[Download the full-resolution timeline](charts/deployment-timeline-2026-10-23.png).

![Deployment timeline showing 17 crypto projects, their consensus mechanisms, signing schemes and limits, as of October 23, 2026.](charts/deployment-timeline-2026-10-23.png)

### Algorithm map

Projects can appear under more than one scheme. Account demonstrations, fallback paths, testnets and opt-in features are labeled. Validity proofs and key-encapsulation mechanisms have separate roles.

[Download the full-resolution algorithm map](charts/algorithm-map-2026-10-23.png).

![Algorithm map grouping projects by cryptographic use, with a log-log comparison of reference public-key and signature sizes and application notes.](charts/algorithm-map-2026-10-23.png)

## A few details that matter

- **Mochimo:** the snapshot records PoS after its October 2026 transition, not its historical PoW consensus.
- **QANplatform:** included as a public testnet. The existence of the QANX token is not evidence of a native mainnet launch.
- **Starknet:** the 2021 milestone is L2 Mainnet Alpha. The independent-L1 vote supported research; it did not approve a move.
- **Raqcoin:** the 2018 date refers to its ABCMint predecessor. It does not date the deployment of UOV. A published attack breaks the legacy Rainbow parameters; newer configurations need their own analysis.
- **Quantus and qtcchain:** both use QTC, but they are separate chains. Use the project ID and source links, not the ticker alone.

## What the data can tell you

It helps answer **what is used, where, under which conditions, and according to which source**. An optional post-quantum spending lock changes how spending is authorized for funds placed under that lock. It does not automatically change old accounts, consensus keys or bridges.

The size table describes specific algorithm parameters and encodings. Its numbers are not complete transaction sizes, fee estimates, throughput measurements or a ranking of cryptographic security. The UOV examples are not measurements of Raqcoin transactions.

The source list separates project documentation, pinned code, block explorers and standards. A project document supports an attributed description; it is not an independent audit. The maps are a selected comparison, not a complete list of every post-quantum project. See [methodology](docs/methodology.md) for the inclusion criteria and limits.

## Reuse or contribute

Download the data, cite the snapshot date and link back to this repository. If you change it, say what changed. Original data compilation, charts and prose are available under **CC BY 4.0**; scripts are **MIT**. Linked third-party material keeps its own terms. See [LICENSE](LICENSE).

To suggest an update, send the specific claim, a primary source and the network/version it applies to. Project teams are welcome to contribute; changes are reviewed against the same evidence standard. [Open a correction or project request](https://github.com/Balance0014/post-quantum-crypto-map/issues/new/choose).

With Python 3.10 or later, you can check the files and regenerate the readable tables without installing packages:

```sh
python3 scripts/validate.py
python3 scripts/export.py
```

The original PNGs are preserved release artifacts. The export script rebuilds tables and CSV files, not those PNGs.

[Follow the research on X](https://x.com/balance0014) · [Changelog](CHANGELOG.md) · [How to cite](CITATION.cff)
