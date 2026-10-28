# Contributing

Found a wrong date, a missing condition or a project we should add? Open an issue or send a pull request. Project teams and independent readers use the same process.

Please include:

1. The project and the specific claim you want to change.
2. A primary source: release notes, deployment details, governance records, an algorithm specification or code pinned to a commit.
3. The network, software version and deployment status. Specify whether the feature is live on mainnet, on a testnet, demonstrated, planned or opt-in.
4. What the evidence establishes, and any remaining limit.

For a new project, include its name, ticker, website/repository, consensus mechanism, milestone, cryptographic scheme and protection scope. Explain any classical fallback or external dependency. Do not submit seed phrases, private keys, private infrastructure details or personal contact information.

Edit `data/projects.json`, `data/signature-sizes.json` or `data/sources.json`, then run:

```sh
python3 scripts/export.py
python3 scripts/validate.py
```

Include the regenerated CSV files and tables in the same pull request. Keep `last_reviewed` tied to the claims you actually checked. A source lookup or code change is not a mainnet activation record.

Maintainers review evidence before merging. Promotional copy, price targets and unsupported whole-chain security labels will not be added. Source disagreement is useful information; describe it rather than hiding it.

Contributions to data, charts and prose follow CC BY 4.0; script contributions follow MIT, as described in [LICENSE](LICENSE). Submit only work you have the right to contribute. Linked third-party material keeps its own license.
