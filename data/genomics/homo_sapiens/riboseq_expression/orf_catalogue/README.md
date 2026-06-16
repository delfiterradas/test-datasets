# orf_catalogue

Minimal crafted ORF catalogue used as input to the `custom/orfcollapse` module
test. The real chr20 data does not contain the case orfcollapse handles (the
same micropeptide encoded at distinct, non-overlapping loci), so this small
fixture is hand-built to exercise it: two identical-peptide smORFs on opposite
strands/loci, one canonical CDS and one unique smORF.

- `cohort.catalogue.{bed12,tsv}`, `cohort.orf_to_gene.tsv`, `cohort.catalogue.mqc.tsv`: orfmerge-shaped catalogue.
- `cohort.catalogue.aa.fasta`: catalogue peptides (headers carry the `(+)/(-)` suffix bedtools getfasta -nameOnly -s emits).
- `cohort_cluster.tsv`: MMseqs2 cluster TSV grouping the two identical smORFs.
