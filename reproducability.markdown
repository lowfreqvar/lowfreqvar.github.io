---
layout: page
title: Reproducability
permalink: /reproducability/
---

# Workflow Overview

```mermaid
graph LR;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

# Data

Raw reads  are deposited on ENA and can be accessed using the link below (N.B *data will be released upon publication*):

<span style="align-items: center; justify-content: center; display: flex; padding: 10px">
[PRJEB51942](https://www.ebi.ac.uk/ena/browser/view/PRJEB51944){: .btn .btn-purple }
</span>

Reference genome and annotation files can be obtained from the links below:

<span style="align-items: center; justify-content: center; display: flex; padding: 10px;">
[FASTA][fasta-link]{: .btn .btn-purple .mr-2}
[GFF3][gff3-link]{: .btn .btn-purple .mr-2}
[GTF][gtf-link]{: .btn .btn-purple .mr-2}
</span>


# Dependencies

{: .important }
> Before being able to create the Conda environment you will need to install conda for your specific OS.
>
> You can install Miniconda for your specific platform from [HERE][conda-link]


Copy the content of the box below into a file named `lowfreqvar.yml`:

```yaml
name: lowfreqvar
channels:
  - conda-forge
  - bioconda
  - defaults
dependencies:
  - bioconda::cutadapt=2.10
  - bioconda::bcftools=1.10.2
  - bioconda::bwa-mem=0.7.17
  - bioconda::freebayes=1.3.2
  - bioconda::lofreq=2.1.5
  - bioconda::rustynuc=0.3.0
```

to create the environment containing all the dependencies run:

```bash
conda env create -f lowfreqvar.yml
```

and to activate the environment run:

```bash
conda activate lowfreqvar
```

[fasta-link]: ftp://ftp.ensemblgenomes.org/pub/bacteria/release-46/fasta/bacteria_3_collection/clostridium_beijerinckii_ncimb_8052/dna/Clostridium_beijerinckii_ncimb_8052.ASM1696v1.dna_sm.toplevel.fa.gz


[gff3-link]: ftp://ftp.ensemblgenomes.org/pub/bacteria/release-46/gff3/bacteria_3_collection/clostridium_beijerinckii_ncimb_8052/Clostridium_beijerinckii_ncimb_8052.ASM1696v1.46.gff3.gz


[gtf-link]: ftp://ftp.ensemblgenomes.org/pub/bacteria/release-46/gtf/bacteria_3_collection/clostridium_beijerinckii_ncimb_8052/Clostridium_beijerinckii_ncimb_8052.ASM1696v1.46.gtf.gz

[conda-link]: https://docs.conda.io/en/latest/miniconda.html
