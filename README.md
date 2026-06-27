# odmlib_snippets

One-off, vendor-specific, and older [odmlib](https://github.com/swhume/odmlib) code that is
useful to keep around but does not belong in the curated
[odmlib_examples](https://github.com/swhume/odmlib_examples) repository.

This repo serves three purposes:

1. **Archive** of narrow, request-specific snippets (e.g. vendor extensions) and older programs.
2. **Test corpus** — varied, real odmlib usage that exercises many code paths.
3. **Reference material for generative AI** — concrete, working examples to learn odmlib patterns from.

> These snippets are not all maintained against the latest odmlib release. Several target older
> odmlib versions (v0.1.x) or the deprecated Define-XML v2.0 model. For current, supported examples
> on odmlib v0.2.0, see [odmlib_examples](https://github.com/swhume/odmlib_examples).

## Contents

### `snippets/` — one-off and vendor-extension scripts

| File | Description | odmlib model |
|------|-------------|--------------|
| `simple_create_odm.py` | Build a minimal ODM v1.3.2 document from scratch and serialize it. | `odm_1_3_2` |
| `odmlib_first_define.py` | Create a Define-XML v2.1 `ItemGroupDef`, validate, and round-trip (PHUSE US Connect 2022). | `define_2_1` |
| `github_issue_import.py` | Minimal Define-XML v2.1 load via the loader. | `define_2_1` |
| `validate_odm.py` | ODM v1.3.2 validation: schema, OID refs, element-order check + reorder. | `odm_1_3_2` |
| `validate_define.py` | Define-XML v2.1 validation: schema, OID, conformance, element order. | `define_2_1` |
| `convert_veeva_odm.py` | Convert a Veeva proprietary model to an ODM v1.3.2 extension. | `veeva_1_0` (local) |
| `veeva_write_odm.py` | Write an ODM-like document with the Veeva draft exchange model. | `veeva_1_0` (local) |
| `osb_odm.py` | Load and display an OSB ODM v1.3 extension document. | `osb_odm_1_0` (local) |
| `veeva_1_0/`, `veeva_odm_1_0/`, `osb_odm_1_0/` | Local extension model packages supporting the vendor snippets. | — |
| `data/` | Sample XML/JSON inputs for the snippets above. | — |

### `notebooks/` — early (v0.1-era) tutorial notebooks

| Notebook | Description |
|----------|-------------|
| `first_odm.ipynb` | Introductory ODM v1.3.2 read/create walkthrough. |
| `first_define.ipynb` | Introductory Define-XML v2.1 walkthrough. |

> Superseded by the v0.2 notebooks in `odmlib_examples/notebooks/`.

## Running

Each script expects to be run from its own directory so the relative `data/` paths resolve, e.g.:

```bash
cd snippets
python simple_create_odm.py
```

Install odmlib first (`pip install odmlib`); the vendor and deprecated examples may require an older
odmlib release.
