# Multi-omics dissection of citrus fruit sugar-acid regulatory networks

**Status:** ongoing collaborative M.Sc. research  
**Role:** eQTL lead, candidate-integration contributor, and functional-validation contributor  
**Public-data status:** workflow and contribution summary only

## Scientific question

How can inherited expression regulation and complementary multi-omics evidence be integrated to identify robust regulators of soluble sugar and titratable acid accumulation in a perennial fruit crop?

## Why a network-level approach is needed

Sugar and acid accumulation are quantitative traits controlled by many interacting genes and physiological processes. Co-expression and differential-expression analyses can identify trait-associated genes, but they often leave large candidate sets and cannot by themselves establish whether expression differences are linked to inherited genomic variation.

This project therefore uses eQTL mapping as a genetic-regulation layer within a broader collaborative framework. The goal is not to claim that every network edge is causal, but to prioritize a small number of genetically supported and experimentally testable regulators.

## Data layers

- fruit soluble-sugar and titratable-acid phenotypes from a citrus hybrid population;
- genome-wide genotype data;
- mature-fruit transcriptomes from 43 hybrid progeny;
- 18,533 expressed genes retained for eQTL mapping after filtering and normalization.

## Collaborative analytical framework

1. co-expression modules and module-trait associations;
2. machine-learning-based feature importance;
3. weighted candidate ranking;
4. differential-expression filtering;
5. penalized-regression-based feature reduction;
6. eQTL mapping to identify genetically regulated expression traits;
7. network construction and centrality analysis;
8. integration of evidence to prioritize candidate hubs;
9. promoter, allele, expression, and functional validation.

## My independent computational contribution

I completed the eQTL component from input preparation to interpretation:

- prepared and transformed genotype inputs;
- generated principal-component covariates;
- constructed a kinship matrix;
- prepared and normalized the expression matrix;
- ran mixed-model genome-wide eQTL mapping;
- applied significance filtering and LD-based signal consolidation;
- classified cis- and trans-eQTL relationships;
- generated genome-wide distribution and eSNP-eGene visualizations;
- identified 3,051 eGenes among 18,533 tested genes.

See [eQTL design](eqtl-design.md) for the analysis logic.

## My collaborative contribution

- participated in intersecting eQTL-supported genes with candidate sets produced by collaborators;
- contributed to extended discussion and prioritization of four regulatory hubs;
- am conducting promoter-activity and downstream functional-validation experiments;
- help interpret whether experimental results support, contradict, or refine the network predictions.

The exact division of labor is documented in [contribution boundary](contribution-boundary.md).

## Biological interpretation

The prioritized hubs span processes including cell-wall xylan metabolism, membrane transport, and central carbon metabolism. One public case study is [IRX10](../irx10-regulatory-genomics/), which is treated as a representative network-derived candidate rather than the scientific scope of the entire project.

The broader hypothesis is that inherited regulatory variation can reshape molecular networks connecting cell-wall carbon allocation, transport, and fruit sugar-acid balance.

## Methodological caution

This portfolio uses the phrase **genetically informed candidate regulatory network**, not a fully proven causal network. Co-expression, feature ranking, penalized regression, and graphical models support candidate prioritization, while eQTL provides a genetic anchor and functional experiments test selected genes individually.

See [limitations](limitations.md).

## Reproducibility and confidentiality

The repository does not contain unpublished raw genotypes, expression matrices, collaborator-owned candidate tables, manuscript figures, or unreleased functional results. Sanitized scripts and simulated examples may be released after manuscript planning and collaborator approval.