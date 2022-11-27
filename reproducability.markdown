---
layout: page
title: Reproducability
permalink: /reproducability/
---

# Workflow Overview

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

# Data

**FASTQ** files are deposited on ENA and you can access them using the button bellow (N.B *data will be released upon publication*):

[PRJEB51942](https://www.ebi.ac.uk/ena/browser/view/PRJEB51944){: .btn .btn-purple }

Reference genome can be obtained from here:

[FASTA][fasta-link]{: .btn .btn-purple }

Genome annotation files can be obtained from here:

[GFF3][gff3-link]{: .btn .btn-purple }

[GTF][gtf-link]{: .btn .btn-purple }


# Dependencies

{: .highlight }
> Before being able to create the Conda environment you will need to install conda for your specific OS.
>
> You can install Miniconda for your specific platform from [HERE][conda-link]




[fasta-link]: ftp://ftp.ensemblgenomes.org/pub/bacteria/release-46/fasta/bacteria_3_collection/clostridium_beijerinckii_ncimb_8052/dna/Clostridium_beijerinckii_ncimb_8052.ASM1696v1.dna_sm.toplevel.fa.gz


[gff3-link]: ftp://ftp.ensemblgenomes.org/pub/bacteria/release-46/gff3/bacteria_3_collection/clostridium_beijerinckii_ncimb_8052/Clostridium_beijerinckii_ncimb_8052.ASM1696v1.46.gff3.gz


[gtf-link]: ftp://ftp.ensemblgenomes.org/pub/bacteria/release-46/gtf/bacteria_3_collection/clostridium_beijerinckii_ncimb_8052/Clostridium_beijerinckii_ncimb_8052.ASM1696v1.46.gtf.gz

[conda-link]: https://docs.conda.io/en/latest/miniconda.html
