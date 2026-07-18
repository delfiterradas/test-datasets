# Test data folder

This folder contains the following files:

- `samplesheet_full.csv`: Samplesheet with the path to the public output directory produced by the nf-core `demultiplex` pipeline, and the paths to the two checksum files.
- `checksum_md5.tsv`: Md5sum calculated for each file inside the directory listed in `samplesheet_full.csv`.
- `checksum_sha.tsv`: Shasum calculated for each file inside the directory listed in `samplesheet_full.csv`.
- `samplesheet.csv`: Samplesheet with paths to an `igenomes` folder, a `.fastq.gz` file, and a `.bed` file hosted in google cloud, as well as the paths to their respective md5sum file.
- `Illumina_annotation_md5.tsv`: Md5sum calculated for each file inside the `igenomes` directory listed in `samplesheet.csv`.
- `samplesheet_edge.csv`: Samplesheet with four `Illumina_annotation` edge cases for checksum validation and destination-state checks: missing checksum/file references, incorrect md5 hashes, a SHA-only incorrect-hash sample, and a pre-populated destination.
- `Illumina_annotation_missing_md5.tsv`: Md5sum file based on `Illumina_annotation_md5.tsv` with `refGene.txt` checksum rows removed and one nonexistent file reference added.
- `Illumina_annotation_incorrect_md5.tsv`: Md5sum file based on `Illumina_annotation_md5.tsv` with incorrect md5 hashes for `refGene.txt` rows.
- `Illumina_annotation_incorrect_sha.tsv`: SHA256 checksum file based on the `Illumina_annotation` paths with incorrect hashes.
- `Illumina_annotation_existing_destination/`: Fixed destination for testing `RCLONE_CHECK` behaviour. It contains copied `Illumina_annotation` files with one modified same-path file, one omitted source-path file, and one destination-only extra file.
- `bed_md5.tsv`: Md5sum calculated for the `.bed` file listed in `samplesheet.csv`.
- `test2_1.fastq.gz`: Test `.fastq.gz` file used in `samplesheet.csv`.
- `test2_1_fastq_md5.tsv`: Md5sum calculated for the `.fastq.gz` file listed in `samplesheet.csv`.
