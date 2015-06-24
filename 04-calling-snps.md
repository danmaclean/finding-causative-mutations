---
layout: page
title: Finding Causative Mutations With A Candidate SNP Approach
subtitle: Finding SNPs With An Alignment
minutes: 25
---

> ## Learning Objectives {.objectives}
> * Understanding Pileups and VCFs
> * Calling reliable SNPs
> * Annotating SNPs with SNPEff
>

Single Nucleotide Polymorphisms can be identified

Many different programs can be used to call SNPs, including SAMTools, Picard, GATK and VarScan. Some of these programs use the BAM alignment file directly, some use an MPileup file. MPileups and VCF files are both used to represent SNPs and associated scores.  

The MPileup format is a per-line base-by-base representation of the alignment. It provides a much more coherent way of viewing the alignment than the SAM file. 

Here's a sample: 

~~~ {.output}

chloroplast	526	C	4	,.,.	GEGF	153,90,68,20	3	,.^].	?.>	57,46,44,26,1
chloroplast	527	T	4	,.,.	DDGF	154,91,69,21	5	.,...	;.@5>	58,47,45,27,2
chloroplast	528	A	4	,.,.	HHGG	155,92,70,22	4	,...	>2?;	59,48,46,28,3
chloroplast	529	C	2	,,	HG	156,93,71,23	3	...	8><	60,49,47,29,4
chloroplast	530	T	4	,.,.	HIGH	157,94,72,24	5	.,...	D?D59	61,50,48,30,5
chloroplast	531	G	4	,.,.	FGFH	158,95,73,25	4	.,..	?@?;	62,51,49,31,6

~~~

Each line represents a single nucleotide in the reference. The first three columns represent the reference name, position on the reference and the reference nucleotide. 

The next three columns are about the bases piled-up over that position, so are total read depth, read bases, and base qualities. 

At the read base column,

 * a dot = a match to the reference base on the forward
 * a comma = match on the reverse strand
 * any of 'ACGTN' = a mismatch on the forward strand 
 * any of 'acgtn' = mismatch on the reverse strand
 
The rest of the information is useful too  information about it can be found here ...


The related VCF file takes a slightly different approach and looks like this:



challenge: run mpileup (no genotype calling)
challenge: run varscan 
challenge: what would heterozygous SNP look like in PileUP, in VCF?

> ##ToDo
> Make a decent BAM file for a good coverage pileup, with some SNPs in
> 
