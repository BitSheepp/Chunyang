# eQTL design and analysis logic

## Objective

Add an inherited-regulation layer to a multi-omics candidate-prioritization framework by identifying expression traits associated with genomic variation while controlling for population structure and relatedness.

## Inputs

- genotype data from a citrus hybrid population;
- mature-fruit transcriptomes for 43 hybrid progeny;
- an expression matrix filtered to genes with sufficient abundance and sample coverage;
- 18,533 genes retained after quality filtering and normalization.

## Workflow

1. **Genotype preparation**  
   Convert and transpose genotype files into formats required by downstream tools; retain quality-controlled biallelic variants.

2. **Population structure**  
   Calculate principal components from genotype data and include the leading components as covariates.

3. **Relatedness control**  
   Construct a kinship matrix to model non-independence among hybrid progeny.

4. **Expression preparation**  
   Filter lowly expressed genes and normalize gene-level expression traits before association testing.

5. **Mixed-model mapping**  
   Test genome-wide SNP-expression associations with a mixed linear model that includes population-structure covariates and the kinship matrix.

6. **Significance filtering**  
   Apply a multiple-testing threshold derived for the genotype dataset rather than relying on an arbitrary nominal P value.

7. **LD consolidation**  
   Consolidate correlated significant variants into LD-supported signals to avoid counting clusters of linked SNPs as fully independent events.

8. **Regulatory-distance classification**  
   Classify significant SNP-gene pairs as cis when the variant is within the predefined local window around the target gene and as trans otherwise.

9. **Genome-wide interpretation**  
   Visualize the chromosomal distribution of signals and the relationship between eSNP and eGene positions to distinguish local diagonals, distal associations, and potential regulatory hotspots.

## Output

- 3,051 eGenes among 18,533 tested expression traits;
- cis- and trans-eQTL classifications;
- LD-consolidated genetic signals;
- an independent source of evidence for prioritizing genes emerging from collaborator-led co-expression, feature-ranking, differential-expression, penalized-regression, and network analyses.

## Reproducibility plan

A future sanitized release will use simulated phenotype, genotype, and expression matrices to demonstrate:

- file preparation;
- covariate construction;
- mixed-model command structure;
- LD consolidation;
- cis/trans annotation;
- summary visualization.

No unpublished biological data or collaborator-owned outputs will be included.