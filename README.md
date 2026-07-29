# Computational Plant Biology Portfolio

I am a master's researcher at Huazhong Agricultural University studying how genetic, regulatory, and environmental variation shapes complex traits in perennial crops. Citrus is my primary biological system.

My work connects four layers of evidence:

1. **Genetic mapping** - whole-genome resequencing, GWAS, linkage disequilibrium, and candidate prioritization.
2. **Regulatory and evolutionary genomics** - eQTL, gene regulatory networks, promoter variation, population differentiation, and nucleotide diversity.
3. **Phenotype acquisition** - multi-site field phenotyping and biologically validated image-derived traits.
4. **Experimental interpretation** - designing computational analyses that generate testable candidates for functional collaborators.

## Evidence map

| Project | Scientific question | My primary contribution | Status |
|---|---|---|---|
| [Citrus taste-metabolite GWAS and promoter evolution](projects/citrus-gwas-evolution/) | How did genetic and regulatory variation shape limonin and citric-acid accumulation? | Resequencing QC, alignment, variant calling/filtering, GWAS, LD, FST, nucleotide diversity, and promoter-evolution analysis | Third-listed co-first-author manuscript under review |
| [IRX10 regulatory genomics](projects/irx10-regulatory-genomics/) | Does lineage-associated promoter variation contribute to expression and fruit-quality differences? | eQTL analysis, candidate prioritization, comparative promoter and expression analysis | Ongoing M.Sc. research |
| PhenoCitrus | How can citrus fruit morphology be measured reproducibly and at scale? | Imaging implementation, data acquisition, phenotype definition, statistical validation, biological interpretation, and writing | Published, co-first author |
| Multi-environment citrus phenotyping | How stable are flowering and fruit-quality traits across regions and years? | Field sampling, trait measurement, hierarchical data curation, and study design | Longitudinal resource in progress |

## Featured computational evidence

The featured project documents the analytical logic behind a citrus fruit-quality study using:

- 802,212 high-confidence SNPs after resequencing processing;
- GWAS and LD analysis in a pummelo hybrid population;
- population differentiation and nucleotide-diversity analysis across 115 Citrus and Aurantioideae accessions;
- explicit separation of statistics used for inference from smoothing used only for visualization.

See the [project overview](projects/citrus-gwas-evolution/) and [analysis decisions](projects/citrus-gwas-evolution/analysis-decisions.md).

## Reproducibility and confidentiality

Some analyses support manuscripts that are under review or ongoing. This repository therefore publishes the **research question, workflow structure, parameter decisions, provenance, and my individual contribution**, but not unpublished raw data, collaborator-owned materials, or manuscript figures. The boundary and planned sanitized releases are documented in [Reproducibility and confidentiality](docs/reproducibility-and-confidentiality.md).

## Links

- [Academic website](https://bitsheepp.github.io/)
- [Google Scholar](https://scholar.google.com/citations?user=7eGT0hAAAAAJ)
- Email: cyhe@webmail.hzau.edu.cn
