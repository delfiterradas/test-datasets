# ![nfcore/test-datasets](docs/images/test-datasets_logo.png)

Test data to be used for automated testing with the nf-core pipelines

> ⚠️ **Do not merge your test data to `master`! Each pipeline has a dedicated branch (and a special one for modules)**

## Introduction

nf-core is a collection of high quality Nextflow pipelines. This repository contains various files for CI and unit testing of nf-core pipelines and infrastructure.

The principle for nf-core test data is as small as possible, as large as necessary. Please see the [guidelines](https://nf-co.re/docs/contributing/test_data_guidelines) for more detailed information. Always ask for guidance on the [nf-core slack](https://nf-co.re/join) before adding new test data.

## Documentation

nf-core/test-datasets comes with documentation in the `docs/` directory:

1.  [Add a new test dataset](https://github.com/nf-core/test-datasets/blob/master/docs/ADD_NEW_DATA.md)
2.  [Use an existing test dataset](https://github.com/nf-core/test-datasets/blob/master/docs/USE_EXISTING_DATA.md)

## Downloading test data

Due the large number of large files in this repository for each pipeline, we highly recommend cloning only the branches you would use.

```bash
git clone <url> --single-branch --branch <pipeline/modules/branch_name>
```

To subsequently clone other branches[^1]

```bash
git remote set-branches --add origin [remote-branch]
git fetch
```

## Genomic interval files

The `modules` branch contains the following interval files for scatter-gather testing (e.g., GATK applyBQSR):

| File | Content | Purpose |
|------|---------|---------|
| `data/genomics/homo_sapiens/genome/genome.bed` | Single interval | Basic interval testing |
| `data/genomics/homo_sapiens/genome/genome.multi_intervals.bed` | Two intervals | Testing multi-interval processing |
| `data/genomics/homo_sapiens/genome/genome.intervals1_multi.bed` | First interval from `genome.multi_intervals.bed` | Testing scatter-gather with individual intervals |
| `data/genomics/homo_sapiens/genome/genome.intervals2_multi.bed` | Second interval from `genome.multi_intervals.bed` | Testing scatter-gather with individual intervals |

## Support

For further information or help, don't hesitate to get in touch on our [Slack organisation](https://nf-co.re/join/slack) (a tool for instant messaging).

[^1]: From [stackoverflow](https://stackoverflow.com/a/60846265/11502856)
