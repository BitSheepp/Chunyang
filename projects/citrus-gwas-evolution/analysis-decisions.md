# Analysis decisions and thresholds

This document records the methodological decisions that most strongly affect interpretation. It is intended to make the analysis auditable even while raw data and full scripts remain restricted.

## 1. Resequencing and variant processing

- Raw reads were quality controlled before alignment.
- Reads were aligned to the pummelo reference genome.
- Only uniquely mapped, non-duplicate reads were retained for downstream variant discovery.
- SNPs were filtered for basic quality, missingness, and minor-allele frequency.
- The final GWAS dataset contained **802,212 high-confidence SNPs**.

## 2. Association design

- The study population contained 51 hybrid progeny; 23 phenotypic extremes were selected for the reported GWAS.
- EMMAX was used to account for relatedness through a kinship matrix.
- Candidate-associated SNPs were retained at **P < 1.0e-3** for regional prioritization rather than presented as conventional genome-wide-significant discoveries.
- The lead association was interpreted together with local LD and expression evidence; no single evidence layer was treated as sufficient by itself.

## 3. Linkage disequilibrium and candidate prioritization

- LD was evaluated around the lead association interval.
- Candidate genes were prioritized by combining genomic position, LD structure, annotation, and expression differences in contrasting materials.
- This multi-evidence strategy was used because the mapping population was modest and statistical power was limited.

## 4. Population-differentiation analysis

- Population variation data comprised 115 Citrus and Citrus-related accessions.
- Each Atalantia-versus-Citrus comparison was constructed as a **pair-specific VCF dataset**.
- FST and nucleotide diversity were therefore estimated within the variant-site background of each pair and were not treated as directly interchangeable across independently constructed datasets.

## 5. Promoter-focused windows

- Weir-Cockerham FST and nucleotide diversity were calculated using **100-bp windows with a 25-bp step**.
- Nucleotide-diversity difference was defined as the absolute difference between populations.
- Candidate windows had to exceed the **90th percentile** for both FST and nucleotide-diversity difference.
- Adjacent candidate windows separated by no more than **200 bp** were merged.
- Candidate identification was restricted to a predefined promoter region rather than interpreted as a genome-wide selection scan.

## 6. Inference versus visualization

- Thresholds and candidate intervals were calculated from **unsmoothed statistics**.
- A three-point centered moving average was used **only for visualization**.
- This separation prevents smoothing from creating or shifting statistical peaks used for inference.

## 7. Important limitations

- The GWAS used a small number of phenotypic extremes and is best viewed as candidate localization supported by independent evidence, not a definitive population-scale association study.
- Pair-specific VCF construction can produce small differences in available SNP backgrounds across comparisons.
- Functional causality depends on experimental evidence from promoter and gene-function assays conducted by collaborators.
