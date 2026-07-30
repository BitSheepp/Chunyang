# Limitations and interpretation boundaries

## 1. Sample size

The eQTL analysis uses 43 progeny with matched genotype and mature-fruit transcriptome data. This is valuable for generating genetic-regulation evidence in a perennial crop, but it limits power, effect-size stability, and detection of weak or rare associations.

## 2. High-dimensional candidate selection

Expression traits and candidate genes greatly outnumber biological samples. Co-expression, machine-learning, differential-expression, and penalized-regression steps therefore function primarily as complementary prioritization tools rather than definitive model-selection procedures.

## 3. Network edges are not automatically causal

WGCNA estimates co-expression, graphical models estimate conditional dependence, and feature-importance methods rank predictive contributions. None of these alone demonstrates a direct regulatory relationship or its direction.

The project is described as a **genetically informed candidate regulatory network** because eQTL adds an inherited-variation anchor and selected genes are tested experimentally. This does not mean every edge in the inferred network is experimentally proven.

## 4. Cis/trans classification is operational

Cis and trans labels depend on a predefined genomic-distance window. A local eQTL may act through several molecular mechanisms, and a distant association may reflect indirect regulation, linkage, or limited sample size.

## 5. Potential eQTL hotspots

Vertical signal clusters can suggest loci associated with expression variation in many genes, but hotspots require careful validation because population structure, mapping artifacts, and broad linkage can produce similar patterns.

## 6. Generalization

The analysis is based on one hybrid population and mature-fruit transcriptomes. Regulatory effects may vary across developmental stages, tissues, genetic backgrounds, years, and environments.

## 7. Functional validation

Promoter assays, heterologous expression, mutants, complementation, and metabolite measurements can support individual candidate functions. They do not by themselves validate the full topology of the inferred network.

## Planned improvements

- increase matched genotype-transcriptome sample size;
- test regulatory effects across developmental stages and environments;
- evaluate allele-specific expression where informative;
- integrate metabolite and longitudinal phenotype data;
- use resampling and external populations to assess candidate stability;
- release sanitized, executable examples after collaborator approval.