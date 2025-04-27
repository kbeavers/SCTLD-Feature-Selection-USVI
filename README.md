# SCTLD Feature Selection - USVI

This repository contains the code and supporting files for characterizing gene expression profiles of various tissue states in stony coral tissue loss disease (SCTLD) using [SigFeature](https://www.frontiersin.org/journals/genetics/articles/10.3389/fgene.2020.00247/full), a feature selection algorithm. 

## Repository Overview

This repository contains an end-to-end workflow for analyzing RNA-seq data from healthy and SCTLD-affected corals (*Montastraea cavernosa*) and their dominant algal symbiont (Genus: *Cladocopium*).

## Data Availability

The raw sequencing data from this study is available in the NCBI BioProject database under accession number [PRJNA1062758](https://www.ncbi.nlm.nih.gov/bioproject/PRJNA1062758/).

### Key Files

#### Command Line Processing
- **`McavStudy_CommandLineCode.Rmd`**: Contains all command line code for:
  - Raw read preprocessing (FastP)
  - De novo *M. cavernosa* transcriptome assembly (Trinity)
  - Transcriptome filtering and annotation
  - Read mapping and quantification

#### Gene Expression Analyses
- **`SCTLD-Field-Study-HOST.Rmd`**: Analysis of host (*M. cavernosa*) gene expression
- **`SCTLD-Field-Study-SYMBIONT.Rmd`**: Analysis of symbiont (*C. goreaui*) gene expression

#### Supporting Files
- **`host_files/`**: Contains reference files for host analysis:
  - `final_mcav_reference_transcriptome.fa.gz`: Host reference transcriptome
  - `annotated_final_mcav_reference_transcriptome.txt`: BLAST annotations for host transcriptome
  - `mcav_tx2tx.csv`: Transcript mapping file
  - `mcav_samples.csv`: List of host quant files used for Tximport

- **`symbiont_files/`**: Contains reference files for symbiont analysis:
  - `final_SymbC_transcriptome.fa.gz`: Symbiont reference transcriptome (from [Davies et al. 2018](https://www.frontiersin.org/journals/marine-science/articles/10.3389/fmars.2018.00150/full)), following additional processing steps
  - `annotated_final_SymbC_transcriptome.txt`: BLAST annotations
  - `SymbC_tx2tx.csv`: Transcript mapping file
  - `SymbC_samples.csv`: List of symbiont quant files used for Tximport

- **`mcav_metaData.csv`**: Sample metadata for expression analyses
- **`Colony Information.xlsx`**: Additional information about coral colonies sampled

For questions or concerns, please contact: kbeavers@tacc.utexas.edu
