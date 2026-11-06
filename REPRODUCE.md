# Reproducing this repository

Input: the Parquet files listed below, revision `fecc2c971945cacd914c63b54ee22db9149e58c9` of the `voilaj/swiss-caselaw` dataset
(`https://huggingface.co/datasets/voilaj/swiss-caselaw/resolve/fecc2c971945cacd914c63b54ee22db9149e58c9/<file>`), plus `graph/statute_references.parquet`
from the same revision, and lexifina/switzerland-law `main` for the overlay's `law_commit`.

```
python tools/build.py sg <cache with data/ and graph/> <empty folder> --today 2026-11-06
```

Needs Python 3 and `duckdb`. Gives 15,344 decision commits and one documentation commit, hash for hash.

## SHA-256 of the input files

```
0aaf3d9b6f1f9efdb56f5f48b0ffc49f94e5311ca594da254cc585f734690d94 *sg_gerichte.parquet
85e1ac95b95651f36cc0d266beb01bc6b44e9319489e5535aaf5d6b0b70f23f3 *sg_handelsgericht.parquet
4270da83108cdb2f105cd8819b0a11ee91f0d966862023aeb41967ccaaad4bde *sg_kantonsgericht.parquet
010a683cdcb217c8f0f045240b75103322703238691f6ed5d1d80942d55cb160 *sg_publikationen.parquet
412205f6524945288e0163166c83f9c68ac416814e000999f394d2813a5d024c *sg_versicherungsgericht.parquet
55345689870f1c4203864dab476d43106f52d9f02aecb3ed23458473c5448951 *sg_verwaltungsgericht.parquet
9cde8d321fcc7e0fc5765a79a5011fa5a8b886a7c2215eab5a91ea3007b3f13a *sg_verwaltungsrekurskommission.parquet
```
