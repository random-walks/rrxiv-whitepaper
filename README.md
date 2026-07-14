# rrxiv whitepaper

The genesis paper of the rrxiv protocol — *rrxiv: An Open Protocol for Research Preprints in the Era of Human–Agent Coproduction*.

This is the first paper published on rrxiv, and it describes the protocol that publishes it. Built using the [`rrxiv-paper-template`](https://github.com/random-walks/rrxiv-paper-template) layout.

## Build

```sh
./scripts/build.sh        # tectonic → build/main.pdf
./scripts/extract-cir.sh  # build/main.cir.json
./scripts/verify.sh       # ajv / jsonschema validation
```

CI in `.github/workflows/build.yml` runs all three on every push and attaches the artifacts to each run.

The rrxiv reference client (parser + CLI + SDK) is on PyPI:

```sh
pip install 'rrxiv>=0.2.1'
rrxiv parse paper/main.tex --output build/main.cir.json
```

(The RRP-0030 claim keys used from v7 on need a >=0.2 parser — hence the version floor.)

## Status

- **Version**: v7 draft — `\rrxivversion` in `paper/main.tex` is authoritative; the live instance's head is v6 until the v7 submission lands; full lineage in `rrxiv-meta.json`'s `versions[]`
- **Protocol version**: 0.1.0
- **Licence**: CC-BY-4.0 (content) + MIT (build code)
- **Canonical id**: [`rrxiv:2605.00001`](https://rrxiv.com/papers/rrxiv:2605.00001) — live on the canonical instance

## History

The drafts that produced this version live in the `papers/whitepaper-iteration/` directory of [`random-walks/rrxiv-dev-workspace`](https://github.com/random-walks/rrxiv-dev-workspace) (private). Drafts there use the pre-rename `rrvix-*` file names and are preserved as a historical record.

## Citation

```bibtex
@misc{rrxiv-whitepaper,
  title  = {{rrxiv}: An Open Protocol for Research Preprints in the Era of Human--Agent Coproduction},
  author = {Albis-Burdige, Blaise},
  year   = {2026},
  url    = {https://rrxiv.com/papers/rrxiv:2605.00001},
  note   = {Whitepaper v6, protocol v0.1.0}
}
```

See `CITATION.cff` for the GitHub-native citation file.
