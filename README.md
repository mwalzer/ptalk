# ptalk: Nextflow pipeline to analyze DDA proteomics data

The *P*roteomics analysis pipeline (ptalk) can be used to perform different data analysis steps on Data Dependent Acquisition (DDA) experiments.

![](https://github.com/bigbio/ptalk/raw/master/docs/workflow.png)

---
**NOTE**

Please if you update the pipeline logic or want to change the pipeline logic use the document (https://github.com/bigbio/ptalk/blob/master/docs/workflow.pptx).

---

## Pipeline aims:

- Provide a DDA analysis pipeline that can automatically process sdrf [experimental design files](https://github.com/PRIDE-Archive/pride-metadata-standard/).
- A standardized pipeline that can be use to reanalyze PRIDE experiments to provide peptide/protein evidences to Uniprot/ENSEMBL resources.
- A standardized pipeline that can be use to reanalyze PTM PRIDE experiments to provide PTM evidences to UNIPROT/ENSEMBL resources.

## Architecture:

We will use [Nextflow](https://www.nextflow.io/) and [BioContainers](https://biocontainers.pro/) to build the pipeline. Every tool should be deposited in BioContainers (we recommended to provide the tools via Conda packages -> BioContainers).

Two main profiles will defined the way the pipeline will be used in production:

 - Kubernetes (Cloud infrastructure)
 - LSF (HPC EBI)

Datasets:

- NCI60: Three different PX datasets related with the following manuscript (PMID: 23933261). https://github.com/PRIDE-Archive/pride-metadata-standard/blob/master/experimental-design/examples/NCI60/sdrf.tsv

- PXD010154: A deep proteome and transcriptome abundance atlas of 29 healthy human tissues (PMID: 30777892). https://github.com/PRIDE-Archive/pride-metadata-standard/blob/master/experimental-design/examples/PXD010154/sdrf.tsv

- PXD000612 (Phospho proteomics experiment): Ultra-deep human phosphoproteome reveals different regulatory nature of Tyr and Ser/Thr-based signaling (PMID: 25159151). https://github.com/PRIDE-Archive/pride-metadata-standard/blob/master/experimental-design/examples/PXD000612/sdrf.tsv


## Contributing:

Whether you want to make your use ptalk or contribute to the development of the pipeline, you are most welcome. This is a community-driven project, that means everyone has a voice.

Here are some general ideas:

- Browse our list of issues and propose your idea.
- Test the pipeline with your own data.
- Propose new tool to replace exiting tools.