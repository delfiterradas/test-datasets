# Test data folder

This folder contains the following files:

- `samplesheet_full.csv`: Samplesheet with the path to the public output directory produced by the nf-core `demultiplex` pipeline, and the paths to the two checksum files.
- `checksum_md5.tsv`: Md5sum calculated for each file inside the directory listed in `samplesheet_full.csv`.
- `checksum_sha.tsv`: Shasum calculated for each file inside the directory listed in `samplesheet_full.csv`.
- `samplesheet.csv`: Samplesheet with paths to an `igenomes` folder, a `.fastq.gz` file, and a `.bed` file hosted in google cloud, as well as the paths to their respective md5sum file.
- `BWAIndex_md5.tsv`: Md5sum calculated for each file inside the `igenomes` directory listed in `samplesheet.csv`.
- `bed_md5.tsv`: Md5sum calculated for the `.bed` file listed in `samplesheet.csv`.
- `test2_1.fastq.gz`: Test `.fastq.gz` file used in `samplesheet.csv`.
- `test2_1_fastq_md5.tsv`: Md5sum calculated for the `.fastq.gz` file listed in `samplesheet.csv`.
