


# **Telomere-to-Telomere consortium fly project**

T2T-fly is a project of the [Telomere-to-Telomere consortium](https://sites.google.com/ucsc.edu/t2tworkinggroup/), led by several leaders in fly satellite and heterochromatin.  The project seeks to finish complete, diploid assemblies for key fly genomes and important cell lines to the community. Following the approach of the human [T2T-CHM13](https://github.com/marbl/CHM13) project, all genomes aim to have high-coverage PacBio HiFi and Oxford Nanopore ultra-long 100 kb+ sequencing reads. Hi-C data was generated for haplotype phasing for all genomes.  \
 \
Phase one of the project focused on completing the ISO-1 (sourced from embryos, 12-hr), A2  (sourced from embryos, 12-hr), and S2 cell lines (sourced from Patrick Heun’s laboratory) (v1 release), and phase two focused on finishing additional drosophila genomes and species (v2 release). Data, assemblies, and associated publications and analyses will be released below:


## **Data reuse and license**

All data is released to the public domain ([CC0](https://creativecommons.org/publicdomain/zero/1.0/)) and we encourage its reuse. However, we are in the process of finishing and analyzing these genomes, so to avoid duplicating effort, we encourage you to contact us if you are interested in contributing. The following working groups have been formed: assembly, annotation, sex chromosomes, comparative and evolutionary genomics, segmental duplications, acrocentric chromosomes and rDNAs, satellite DNAs, mobile elements, and pangenomics.


## HiFi Data 


**ISO1**

Four Sequel II flowcells for a total of 86Gb (gigabase) of HiFi data.  HiFi reads are available in fastq and bam format.  Subreads are also available. 

**A2**

One Revio flowcell with 98Gb of HiFi data.  HiFi reads are available in bam format.

## Oxford Nanopore Data

**ISO1**

Three nanopore flowcells.  Data is available in bam and fastq format.  Raw fast5 data are also available.

**A2**  

Four Nanopore flowcells for a total of 320Gb of data.  Data is available in bam format.  Raw fast5 or pod5 data are also available.


## HiC data 



## **Downloads**

All generated sequencing data and assemblies are available for browsing and download from [GenomeArk](https://www.genomeark.org/)


ISO1: [S3 File Index](https://genomeark.s3.amazonaws.com/index.html?prefix=species/Drosophila_melanogaster/idDroMela1/) &nbsp; &nbsp; [S3 Interactive Viewer](https://42basepairs.com/browse/s3/genomeark/species/Drosophila_melanogaster/idDroMela1) 

A2: &nbsp; [S3 File Index](https://genomeark.s3.amazonaws.com/index.html?prefix=species/Drosophila_melanogaster/idDroMela2/) &nbsp; &nbsp; [S3 Interactive Viewer](https://42basepairs.com/browse/s3/genomeark/species/Drosophila_melanogaster/idDroMela2) 



## **A2 ONT Sample preparation**

**Simplex** High molecular weight DNA was extracted from A2 embryos (15-18hr) using a protocol adapted from methods provided by the Karpen Lab at UC Berkeley and Inswasti Cahyani et al. (dx.doi.org/10.17504/protocols.io.bxgnpjve). Embryos were homogenized with a pellet pestle in a homogenization buffer (30mM Tris-HCl pH 8, 100mM NaCl, 10mM EDTA, 0.5% Triton x-100). The homogenate was centrifuged, and the pellet was resuspended in Tris Lysis Buffer (100 mM NaCl, 10 mM Tris-HCl, pH 8, 25 mM EDTA, pH 8, 0.5% (w/v) SDS) and treated with Proteinase K and RNase A. DNA was then extracted using phenol-chloroform extraction method. Precipitation of DNA was achieved with 3 volumes of ethanol, along with a final concentration of 100 mM NaCl and 500 mM NaAc. Wide-bore pipet tips were used for all steps in the protocol to reduce DNA shearing. Nanodrop and Qubit measurements were taken to assess quality and quantity of DNA respectively. Small DNA fragments were removed from the sample using PacBio SRE kit (SKU 102-208-300) and the size of DNA fragments were analyzed on Agilent Femto Pulse System using genomic DNA 165 kb kit (FP-1002-0275).

**Duplex** High molecular weight DNA was extracted from A2 embryos using the protocol described for simplex sample preparation listed previously. Isolated DNA was then sheared using Diagenode Megaruptor 3, DNA fluid+ kit (E07020001). The size of sheared DNA fragments were analyzed on Agilent Femto Pulse System using genomic DNA 165 kb kit (FP-1002-0275). Fragment size distribution of post-sheared DNA had peak at approximately 50kb. Small DNA fragments were removed from the sample using PacBio SRE kit (SKU 102-208-300). 

## **A2 ONT Sequencing Protocols**

**Simplex** Initial libraries were prepared using ONT Ultra Long library kit (SQK-ULK114) but resulted in low pore occupancy and yields. To improve throughput, library preparation was carried out using Oxford Nanopore Technologies (ONT) ligation sequencing kit V14 (SQK-LSK114) and sequenced on R10.4.1 flow cells. Three libraries were prepared per flow cell. Flow cells were washed using ONT wash kit (EXP-WSH004) and reloaded with a fresh library every 24 hours for a total sequencing runtime of 72 hours. Basecalling was done with using [dorado](https://github.com/nanoporetech/dorado) v0.7.3 and the super accurate (sup) model v5.0.0.  5mCG_5hmCG methylation was also called.  Calling modifications does not affect basecalling and can be ignored or dropped if not needed.  

**Duplex** Library preparation was carried out using Oxford Nanopore Technologies (ONT) ligation sequencing kit V14 (SQK-LSK114). PromethION high duplex flow cells were provided by ONT for sequencing on PromethION 48 sequencer. Three libraries were prepared per flow cell. Flow cells were washed using ONT wash kit (EXP-WSH004) and reloaded with fresh library every 24 hours for a total sequencing runtime of 72 hours. Basecalling was done with using [dorado](https://github.com/nanoporetech/dorado) v0.4.3 and the super accurate model (sup) v4.2.0.  Reads were then split into duplex and simplex based on [dx tag](https://github.com/nanoporetech/dorado?tab=readme-ov-file#duplex).  


### **Notes on downloading files**

Please reference the GenomeArk [aws cli primer](https://www.genomeark.org/documentation/aws-cli-primer.html) for help with downloads.  Access/permission issues may be resolved with the `--no-sign-request` option.


## **Contact**

For any problems related to this dataset, please raise [issues](https://github.com/ucsc-seqtech/t2t-fly/issues) on this GitHub repository. For general questions regarding the project, please contact [Ivo Violich](mailto:iviolich@ucsc.edu) . More information about our consortium can be found on the [T2T homepage](https://sites.google.com/ucsc.edu/t2tworkinggroup/).


## **History**




