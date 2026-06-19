# Test data folder

This folder contains three files:

- `samplesheet.csv`
- `checksum_md5.tsv`
- `checksum_sha.tsv`

## Description

The `samplesheet.csv` file contains:

- the path to the public output directory produced by the nf-core `demultiplex` pipeline, and
- the paths to the two checksum files.

The `checksum_md5.tsv` and `checksum_sha.tsv` files contain checksums calculated for each file inside the directory listed in the sample sheet.

